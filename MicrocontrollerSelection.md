---
Title: Microcontroller Selection
---

## Temperature Sensor Module

| Design Considerations | Team Project-Specific Requirements<br>from Problem Definition and Block Diagram | PIC<br>Option1 | PIC<br>Option2 | PIC<br>Option3 |
| --- | --- | :---: | :---: | :---: |
| How many GPIO Pins? | 13 (3 LED, 1 Button, 3 CS SPI, 2 SPI, 2 I2C, 2 UART) | 25 | 16 | 25 |
| Built-in Analog to Digital Converter?<br>How many? | 0 | 25 | 16 | 25 |
| Built-in Hardware PWM?<br>How many? | 0 | 25 | 16 | 25 |
| Built-in I2C? SPI? How many? | 13 (3 LED, 1 Button, 3 CS SPI, 2 SPI, 2 I2C, 2 UART) | 25 | 16 | 25 |
| Built-in UART? How many? | 13 (3 LED, 1 Button, 3 CS SPI, 2 SPI, 2 I2C, 2 UART) | 25 | 16 | 25 |
| Other Required Built-In Features? (optional) | 13 (3 LED, 1 Button, 3 CS SPI, 2 SPI, 2 I2C, 2 UART) | 25 | 16 | 25 |
| Additional considerations specific<br>to your project specifications (optional) | 13 (3 LED, 1 Button, 3 CS SPI, 2 SPI, 2 I2C, 2 UART) | 25 | 16 | 25 |

Choice: Option 1

Rationale: One reason why we choose this sensor is because of the output type, we need either SPI or I2C. In addition to this, we will be working with Option 1 in class, this will make it easier on the team to apply this sensor to our product.

## Hall Effect Sensor

| Solutions     | Pros          | Cons  |
| :---: | --- | ---|
| Option 1. Sensor Rotary 360deg SMD<br>MLX90316EDC-BDG-100-TU-ND<br>$6.97/each<br>[link to product](/https://www.digikey.com/short/44z2bv5z) | *SPI output<br>*Surface mount | *supply voltage 4.5-5.5V<br>*Least varying operating temperature -40C-85C |
| Option 2. Sensor Angle 360deg SMD<br>AS5600-ASOM<br>$3.46/each<br>[Link to product](/https://www.digikey.com/short/jd4n23vq) | *Least expensive<br>*Supply voltage 3.3V, 5V<br>*Surface mount | *Analog voltage for output |
|Option 3. Hall Effect Sensor Rotary Position External Magnet<br>AS5047U-HTSM<br>$13.01/each<br>[Link to product](/https://www.digikey.com/short/2twd9t7v) | *Supply voltage 3-3V-6V, 4.5V-5.5V<br>*SPI & PWM output<br>*Surface mount | *Most expensive<br>*TSSOP packaging |

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
