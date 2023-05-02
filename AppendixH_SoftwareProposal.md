---
Title: Appendix H Software Implementation
---

## Appendix H: Final Software Implementation

MQTT Topic Table

![image caption](https://cdn.discordapp.com/attachments/1062096006642147503/1102845523557351454/image.png)

MCC Configuration

![image caption](https://cdn.discordapp.com/attachments/1062096006642147503/1102845136242741248/image.png)

C++ Code
Full code can be found at our team's [Github Repository](https://github.com/egr314-team207/Embeded-Code)
```
// Definitions 
#define TC74_ADDRESS 0x4c // TC74A4-3.3VCT ADDRESS IS 0b1001100
#define TEMPERATURE_READ 0x00 //TC74 TEMPERATURE (C) READ REGISTER 
#define AS5600_ADDRESS 0x36 //AS5600 ADDRESS IS 0b0110110
#define AS_ANGLE1 0x0C //AS5600 ANGLE 11:8 Bits Register
#define AS_ANGLE2 0x0D //AS5600 ANGLE 7:0 Bits Register
#define ANGLE_CHECK 400
#define DEGREES 360 // Degrees in a circle
#define ANGLE_DIVISONS 1024; // Counts per Rev
#define RPM_S 0.10; //Seconds between measurements used for RPM calculations
#define BUFFER_SIZE 256 //Size of UART Message Buffer
#define MOTOR_RUN_TIME_S 2 //Time to run motor
#define MS 1000 //Miliseconds in a second
#define MOTORCW 0b11101111 //Command to run motor foreward
#define MOTORCCW 0b11101101 //Command to run motor backwards
#define MOTORDISABLE 0b11000000 //Command to disable motor
#define SENSOR_PERIOD_S 1 //Frequency of reading sensor measurments

//Global Variables
//Temperature Variables
int8_t temperature;
int8_t temperatureCompare = 30;
//Hall Effect Variables
uint16_t angle;
uint16_t startingAngle = 0;
uint16_t endingAngle = 0;
uint16_t deltaAngle = 0;
uint16_t angleDivs = ANGLE_DIVISONS;
float processedAngle;
float angleConversionMultiplier = (float)1024/(float)360;
float angleStartTime = 0;
float angleTimer = RPM_S;
float angleEndingTime;
float angleDeltaTime;
float angleCountsPerTimeInterval = 0;
float rpm = 0;
//Motor Driver Variables
uint8_t motorDirection = 0; // 0 - Forward, 1 - Backward
float motorStartTime = 0; // Time motor started running
bool clockwise = true;
bool enableMotor = false;
//bool timerOverflowFlag = false;
//uint32_t motorStartTime = 0;
//Timer Variables
uint16_t timer_ms = 0;
uint16_t timer_s = 0;
float time = 0.0;
float loopRunningTime = 0.0;
float loopStartTime = 0.0;
float sensorUpdateTimer = 0.25;
//Message Variables
char ESP32RxBuffer[BUFFER_SIZE];
char ESP32TxBuffer[BUFFER_SIZE];
char rxByte;
uint8_t rxIndex = 0;
bool ESPrxComplete = false; // Message Complete Flag
uint8_t endingIndex = 0;
uint8_t startingIndex = 0;
uint8_t lengthMessage = 0;
//Flags
bool loopNotStarted = true;
bool readSensors = true;
bool sensorsDone = false;
bool noStartingAngle = true;
bool noEndingAngle = true;
bool txSensors = true;
bool cwflag = true; // Motor Direction Flag
bool doorOpened = false;
bool motorStart = false;
bool motorComplete = false;
bool tempThresholdCrossed = false;
bool angleThresholdCrossed = false;
bool lowTemp = true;
bool hasMotorStarted = false;
bool rpmChanged = false;



//Function Declarations
void runMotorForDuration(bool enable, bool cw, uint16_t seconds);
void timer2InterruptHandler(void);
void UART2ISR(void); // Connected to ESP32 Via RX RC0 and TX RC1
int8_t readTemperature(void); // Must be run after i2c is initialized
uint16_t readAngle(void); // Must be run after i2c is initialized
void processMessage(char msg[]); // Process message in char array
void sendMotorCommand(uint8_t commmand); // Send Command to run on SPI Motor

void main(void)
{
    // Initialize the device
    SYSTEM_Initialize();
    TMR2_Initialize();
    I2C1_Initialize();
    PIN_MANAGER_Initialize();

    // Custom Interrupt Handler Declarations
    EUSART2_SetRxInterruptHandler(* UART2ISR);
    TMR2_SetInterruptHandler(* timer2InterruptHandler);
    
    // If using interrupts in PIC18 High/Low Priority Mode you need to enable the Global High and Low Interrupts
    // If using interrupts in PIC Mid-Range Compatibility Mode you need to enable the Global and Peripheral Interrupts
    // Use the following macros to:

    // Enable the Global Interrupts
    INTERRUPT_GlobalInterruptEnable();

    // Disable the Global Interrupts
    //INTERRUPT_GlobalInterruptDisable();

    // Enable the Peripheral Interrupts
    INTERRUPT_PeripheralInterruptEnable();

    // Disable the Peripheral Interrupts
    //INTERRUPT_PeripheralInterruptDisable();

    SPI2_Open(SPI2_DEFAULT); //SPI activation
    TMR2_StartTimer();
    SSP2CON1bits.CKP = 0; // Clock Polarity (CPOL)
    SSP2STATbits.CKE = 0; // Clock Edge (CPHA)
    
    while (1)
    {
        if(loopNotStarted){
            //Reset all flags to start of loop states
            readSensors = true;
            noStartingAngle = true;
            noEndingAngle = true;
            rpmChanged = false;
            loopStartTime = time;
            sensorsDone = false;
            loopNotStarted = false;
        }
        while(readSensors){
            loopRunningTime = time - loopStartTime;
            if(sensorsDone){
                break;
            }
            if(noStartingAngle){
                startingAngle = readAngle();
                noStartingAngle = false;
            }
            if(loopRunningTime >= angleTimer && noEndingAngle){
                endingAngle = readAngle();
                angleEndingTime = time;
                noEndingAngle = false;
            }
            temperature = readTemperature();
            if(temperature < temperatureCompare){
                //closePlanter = true;
                //break;
            }
            if(startingAngle > endingAngle && !noEndingAngle){
                // Rotated past 0 correction
                endingAngle += ANGLE_DIVISONS;
            }
            deltaAngle = endingAngle - startingAngle;
            if(deltaAngle > angleDivs){
                deltaAngle -= ANGLE_DIVISONS;
            }
            if(!noStartingAngle && !noEndingAngle){
                angleDeltaTime = angleEndingTime - loopStartTime;
                angleCountsPerTimeInterval = (float) deltaAngle / angleDeltaTime;
                sensorsDone = true;
                txSensors = true;
            }   
        }

        angle = readAngle();
        processedAngle = (float)angle / angleConversionMultiplier;
        if(sensorsDone && txSensors){
            txSensors = false;
            printf("Temp:%iC Angle Speed:%f\n",temperature,angleCountsPerTimeInterval);
        }

         if(temperature >= temperatureCompare || angleCountsPerTimeInterval >0){
             if(lowTemp){
                 lowTemp = false;
                 hasMotorStarted = false;
             }
             clockwise = true;
             enableMotor = true; 
         }
         if(temperature < temperatureCompare && angleCountsPerTimeInterval == 0){
             if(!lowTemp){
                 lowTemp = true;
                 hasMotorStarted = false;
             }
             clockwise = false;
             enableMotor = true;
         }
         runMotorForDuration(enableMotor,clockwise,2);
        //__delay_ms(50);
        if(ESPrxComplete){
            printf("%s",ESP32RxBuffer);
            ESPrxComplete = false;
        }
        // printf("test message\n");
         if(loopRunningTime >= sensorUpdateTimer){
             loopNotStarted = true;
         }
    }
    SPI2_Close();
}

/*void motorControl(uint8_t enable) {
    uint8_t command;
    uint16_t duration_s = MOTOR_RUN_TIME_S;
    if (enable) {
        command = motorDirection ? MOTORCCW : MOTORCW; // Enable motor with direction control
    } else {
        command = MOTORDISABLE; // Disable motor
    }
    sendMotorCommand(command);
    if (enable) {
        motorStartTime = time; // Save the current time
        while (time - motorStartTime < duration_s) {
            // Wait for the motor to run for the specified duration
        }
        sendMotorCommand(command);
    }
}*/

void runMotorForDuration(bool enable, bool cw, uint16_t seconds) {
    uint8_t command;
    if(!hasMotorStarted){
        motorStartTime = time;
        hasMotorStarted = true;
    }
    if(cw){
        command = MOTORCW;
    }else{
        command = MOTORCCW;
    }
    if(!enable){
        command = MOTORDISABLE;
    }
    if(hasMotorStarted && enable){
        if(time - motorStartTime > seconds){
            command = MOTORDISABLE;
        } 
    }
    sendMotorCommand(command);
}

void sendMotorCommand(uint8_t commandSend){
    SPI2_SS_SetLow(); // Set SS (RB1) low to start communication
    __delay_us(50);
    SPI2_WriteByte(commandSend); // Send the command 
    __delay_us(50); // Add a small delay between sending commands
    SPI2_SS_SetHigh(); // Set SS (RB1) high to end communication
    __delay_us(50);  // Add a small delay between sending commands
}

void timer2InterruptHandler(void) {
    timer_ms += 1;
    if(timer_ms >= 1000){
        timer_ms -= 1000;
        timer_s += 1;
    }
    time = timer_s + (float)timer_ms/MS;
}



void UART2ISR(void){
    EUSART2_Receive_ISR();
    if(EUSART2_is_rx_ready()){
        rxByte = EUSART2_Read();
    }
    ESP32RxBuffer[rxIndex] = rxByte;
    if(rxByte == ';'){
        ESPrxComplete = true;
        ESP32RxBuffer[rxIndex + 1] = '\n';
        rxIndex = 0;
    }
    if(rxIndex >= 255){
        rxIndex = 0;
    }
    else{
        rxIndex++;
    }
    DEBUG_LED_Toggle();
}

int8_t readTemperature(void){
    int8_t temperatureValue = 0;
    temperatureValue = I2C1_Read1ByteRegister(TC74_ADDRESS,TEMPERATURE_READ);
    return temperatureValue;
}

uint16_t readAngle(void){
    uint16_t angleOutput;
    uint8_t angle0to7;
    uint8_t angle11to8;
    angle0to7 = I2C1_Read1ByteRegister(AS5600_ADDRESS,AS_ANGLE2);
    angle11to8 = I2C1_Read1ByteRegister(AS5600_ADDRESS,AS_ANGLE1);
    angleOutput = angle11to8 << 8;
    angleOutput += angle0to7;
    angleOutput = angleOutput >> 2;
    return angleOutput;
}

void processMessage(char msg[]){
    
}
```

[Back to Final Software Implementation](SoftwareProposal.md)

[Back to Project Overview](index.md)
