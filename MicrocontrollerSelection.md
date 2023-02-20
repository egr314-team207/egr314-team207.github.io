---
Title: Microcontroller Selection
---

## Temperature Sensor Module

| Design Considerations | Team Project-Specific Requirements<br>from Problem Definition and Block Diagram | PIC<br>Option1 | PIC<br>Option2 | PIC<br>Option3 |
| --- | --- | :---: | :---: | :---: |
| How many GPIO Pins? | 13 (3 LED, 1 Button, 3 CS SPI, 2 SPI, 2 I2C, 2 UART) | 25 | 16 | 25 |
| Built-in Analog to Digital Converter?<br>How many? | 0 | 1 | 1 | 1 |
| Built-in Hardware PWM?<br>How many? | 0 | 2 | 0 | 2 |
| Built-in I2C? SPI? How many? | 1 I2C 1 SPI  | 1 I2C<br>1 SPI | 2 | 2 |
| Built-in UART? How many? | 13 (3 LED, 1 Button, 3 CS SPI, 2 SPI, 2 I2C, 2 UART) | 2 | 2 | 2 |
| Other Required Built-In Features? (optional) | --- | --- | --- | --- |
| Additional considerations specific<br>to your project specifications (optional) | --- | --- | --- | --- |

Choice: Option 1

Rationale: One reason why we choose this sensor is because of the output type, we need either SPI or I2C. In addition to this, we will be working with Option 1 in class, this will make it easier on the team to apply this sensor to our product.

## Microcontrollers information

| Microcontroller Considerations | PIC<br>Option1 | PIC<br>Option2 | PIC<br>Option3 |
| --- | :---: | :---: | :---: |
| Part Number | PIC18F26K40 | PIC18F27J53 | PIC18F27K40 |
| Links (URL) to Data Sheets | [Link](https://www.microchip.com/en-us/product/PIC18F26K40) | [Link](https://www.microchip.com/en-us/product/PIC18F27J53) | [Link](https://www.microchip.com/en-us/product/PIC18F27K40) |
| Links (URL) to Data Sheets | [Link](https://ww1.microchip.com/downloads/aemDocuments/documents/OTH/ProductDocuments/DataSheets/PIC18LF26-45-46K40-Data-Sheet-DS40001816F.pdf) | [Link](https://ww1.microchip.com/downloads/aemDocuments/documents/OTH/ProductDocuments/DataSheets/30009964C.pdf) | [Link](https://ww1.microchip.com/downloads/aemDocuments/documents/OTH/ProductDocuments/DataSheets/PIC18LF27_47K40-Data-Sheet-40001844E.pdf) |
| Links (URL) to Application<br>Notes | [Link](https://ww1.microchip.com/downloads/en/Appnotes/Getting-Started-With-SPI-Using-MSSP-on-PIC18-90003265B.pdf) | [Link](https://ww1.microchip.com/downloads/en/Appnotes/00001267b.pdf) | [Link](https://ww1.microchip.com/downloads/en/Appnotes/Getting-Started-With-SPI-Using-MSSP-on-PIC18-90003265B.pdf) |
| Links (URL) to Code Examples | [Link](https://github.com/microchip-pic-avr-examples/pic18f27k42-curiosity-hpc-labs) | --- | [Link](https://github.com/microchip-pic-avr-examples/pic18f27k42-curiosity-hpc-labs) |
| Links (URL) to External Resources |  --- | --- | [Link](https://electronics.stackexchange.com/questions/282913/spi-library-for-pic18f27k40) |
| Production Unit Cost | $2.44 | $4.99 | $2.08 |
| Supply Voltage Range | 2.3-5.5 | 2.15-3.6 | 1.8-3.6 |
| Absolute Maximum Current for entire IC) | 250mA | 200mA | 250mA |
| Maximum GPIO Pin Current | 50mA | 25mA | 50mA |
| 8-bit or 16-bit Architecture | 8 bit | 8 bit | 8 bit |
| Available IC Packages / Footprints | SPDIP<br>SOIC<br>SSOP | SPDIP<br>SOIC<br>SSOP | SPDIP<br>SOIC<br>SSOP |
| Supports External Interrupts? | Yes | Yes | Yes |
| In-System Programming<br>Capability and Type | ICSP | ICSP | ICSP |
| Programming Hardware, Cost,<br>and URL | $76.99<br>[link](https://www.microchip.com/en-us/development-tool/PG164140) | $76.99<br>[link](https://www.microchip.com/en-us/development-tool/PG164140) | $76.99 [link](https://www.microchip.com/en-us/development-tool/PG164100)<br>$76.99 [link](https://www.microchip.com/en-us/development-tool/PG164140) |
| Works with [MPLAB® X Integrated Development Environment](https://www.microchip.com/mplab/mplab-x-ide) (IDE)? | Yes | Yes | Yes |
| Works with [Microchip Code Configurator](https://www.microchip.com/mplab/mplab-code-configurator)? | Yes | Yes | Yes |

Choice: Option 2: AS5600-ASOM

Rationale: This option seemed most rational because it contains most of the pros with the least amount of cons. Also able to work with different voltages and in a wide range of temperatures. This chip is also one we have worked with in the past so there's less of a learning curve.

## Microcontrollers Options

| Design Conciderations | Team Project-Specific Requirements<br>from Problem Definition and Block Diagram | Pic<br>Option1 | Pic<br>Option2 | Pic<br>Option3 |
| --- | --- | :---: | :---: | :---: |
| How many GPIO Pins? | 13 (3 LED, 1 Button, 3 CS SPI, 2 SPI, 2 I2C, 2 UART) | 25 | 16 | 25 |
| Built-in Analog to Digital Converter? <br>How many? | 0 | 1 | 1 | 1 |
| Built-in Hardware PWM? How many? | 0 | 2 | 0 | 2 |
| Built-in I2C? SPI? How many? | 1 I2C 1 SPI  | 1 I2C<br>1 SPI | 2 | 2 |
| Built-in UART? How many? | 1 | 2 | 2 | 2 |
| Other Required Built-In Features? (optional) | --- | --- | --- | --- |
| Additional considerations specific to<br>your project specifications (optional) | --- | --- | --- | --- |

Choice: Option 1: L9958

Rationale: The L9958 offers the most in terms of flexibility and power controls for our device. The chip is the most expensive option, but it also has the most robust SPI interface options. It also has a very high amperage output potential, allowing the team to use more powerful motors. 

## Motor

| Solutions     | Pros          | Cons  |
| :---: | --- | ---|
| Option 1. Pololu 99:1 Gear motor<br>$48/each<br>[datasheet](/https://www.pololu.com/file/0J1829/pololu-25d-metal-gearmotors.pdf) | *High torque<br>*Wide range of operating voltages<br>*Highly available<br>*Affordable<br>*More precise control | *Encoder adds design complexity<br>*High Power Requirements |
| Option 2. Nidel Copal ROB-09238<br>$19/each<br>[datasheet](/https://www.sparkfun.com/datasheets/Robotics/SM-42BYG011-25.pdf) | *Stepper motor gives more precise control<br>*Affordable<br>*High torque<br>*Available from reputable sources | *Little documentation on this device<br>*Extra complexity due to stepper motor features<br>*High power requirements |
| Option 3. Pololu 4798 Brushed Gearmotor<br>$22/each<br>[datasheet](/https://www.pololu.com/product-info-merged/4798)ements<br>*Does not have precise motor control options |

Rationale: For the purposes of the team’s design, the added complexity and precision 

Choice: Option 3. Pololu 4798 Brushed Gearmotorfrom the alternative motor options is not necessary. This motor fits the needs of the design as a high torque motor, and is both affordable and in high availability.

## Power Source

| Solutions     | Pros          | Cons  |
| :---: | --- | ---|
| Option 1. KS-0930 9V<br>$15.42 Each<br>[Link to Product](/https://www.amazon.com/9V-Adapter-Charger-HD500X-Supply/dp/B07G282CBQ/ref=sr_1_3?c=ts&keywords=AC+Adapters&m=A33NHAKGS6YV9K&qid=1669658808&refinements=p_6%3AA33NHAKGS6YV9K&s=electronics&sr=1-3&ts_id=10967101) | *Continuous source of 12V<br>*No need to replace components over time<br>*Outputs up to 3 Amps | *Requires a direct connection<br>*Wired connection can be tedious to manage<br>*Limits portability of design |
| Option 2. EN22<br>$2.59/each<br>[Link to product](/https://www.digikey.com/en/products/detail/energizer-battery-company/EN22/704825) | *Affordable<br>*Can withstand high temperatures<br>*Many in stock (digikey) | *Unstable<br>*Output voltage dips from 9V to 5V after a day of use (Constant Output) |
| Option 3. A 1604 BK210J<br>$2.16/each<br>[Link to product](/https://www.digikey.com/en/products/detail/energizer-battery-company/A1604-BK210J/11615674) | *Affordable<br>*Highest max power | *Expensive<br>*Few in stock<br>*Highest minimum current and voltage requirements |

Choice: Option 1

Rationale: The team opted to use the AC/DC 12V power supply due to its ease of use and consistent 12V supply. The loss of portability is made up for by the convenience of not needing to replace batteries after repeated usage.

## Voltage Regulator

| Solutions     | Pros          | Cons  |
| :---: | --- | ---|
| Option 1. MIC5156-5.0YM<br>$4.04 Each<br>[Link to Product](/https://www.digikey.com/en/products/detail/microchip-technology/MIC5156-5-0YM/1030138) | *Input: 3 - 36V<br>*Surface Mount<br>*Affordable<br>*Positive fixed | *Few in stock |
| Option 2. RT9194GE<br>$0.68/each<br>[Link to Product](/https://www.digikey.com/en/products/detail/richtek-usa-inc/RT9194GE/2546985) | *Cheap<br>*Surface Mount<br>*Input: 4.5 - 13.5V | *Positive Adjustable |
| Option 3. LT1575CS8-3.3#PBF<br>$7.44/each<br>[Link to Product](https://www.digikey.com/en/products/detail/analog-devices-inc/LT1575CS8-3-3-PBF/889248) | *Surface Mount<br>*Input: 10 - 20V<br>*Positive fixed | *Most Expensive<br>*Few in Stock |

Choice: Option 1

Rationale: Option 1 has a wide voltage input which would work for our components and is available for an affordable price. By being a positive fixed type we will avoid having to use external components.

[Appendix F: Microcontroller Selection](AppendixF_MicrocontrollerSelection.md)

[Back to Project Overview](index.md)
