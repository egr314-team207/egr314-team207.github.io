---
Title: Component Selection
---

## Temperature Sensor Module

| Solutions     | Pros          | Cons  |
| :---: | --- | ---|
| Option 1. TC74A4-3.3VCTTR<br>$1.09/each<br>[Link to Product](/https://www.digikey.com/en/products/detail/microchip-technology/TC74A4-3-3VCTTR/443268) | *Surface Mount<br>*Cheap<br>*Range: -40 to 125 C<br>*Digital output<br>*Voltage: 2.7 to 5.5 V<br>*Standby mode<br>*I2C output | *Small and difficult to solder<br>*2 degree accuracy |
| Option 2. TMP126DCKR<br>$3.01/each<br>[Link to Product](/https://www.digikey.com/en/products/detail/texas-instruments/TMP126DCKR/16602359struments/TMP236A4DCKT/9692559) | *Digital output<br>Range: -55 - 175 C<br>*Voltage: 1.62 - 5.5 V<br>*One-shot, Shutdown mode, Sleep mode<br>*.3 degree accuracy<br>*Surface mount | *Expensive compared to others<br>*Voltage Output |
| Option 3. TMP126NDCKR<br>$2.03 /each<br>[Link to Product](/https://www.digikey.com/en/products/detail/texas-instruments/TMP126NDCKR/16602367) | *Digital Output<br>*Range: -55 - 150 C<br>*Voltage 1.62 - 5.5 V<br>*One-shot, Shutdown mode, Sleep mode<br>*.8 degree Accuracy<br>*SPI output |  |

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

## Motor Module

| Solutions     | Pros          | Cons  |
| :---: | --- | ---|
| Option 1. L9929 SPI Controlled Half Bridge<br>$8/each<br>[Datasheet](/https://aliot.com.ua/pdf/l9929.pdf) | *High voltage draw options<br>*Highest amperage output option<br>*Highest power draw options<br>*SPI compatible | *No heat sink<br>*Low documentation<br>*Not available from reputable resources |
| Option 2. DRV8823-Q1 4-Bridge Serial Interface Motor Driver<br>$6.5/each<br>[Datasheet](/https://www.ti.com/lit/ds/symlink/drv8823-q1.pdf?ts=1675110821912&ref_url=https%253A%252F%252Fwww.google.com%252F) | *Significantly more interface options than alternatives<br>*Built in 3.3V reference<br>*Protected against under/over voltage | *More complex than other devices<br>*More pins means more complex circuit design<br>*High voltage requirements |
| Option 3. IFX9201SGAUMA1 Half Bridge Motor Driver<br>$4.88/each<br>[Datasheet](https://www.mouser.com/datasheet/2/389/l9958-1849672.pdf) | *Various power package options<br>*3.3V Compatible<br>*16 bit SPI interface<br>*Up to 20 Khz operating frequency<br>*High power flexibility | *Less documentation than other options<br>*Low maximum voltage relative to alternatives |

Choice: Option 13: IFX9201SGAUMA1

Rationale: The IFX9201SGAUMA1 offers the most in terms of flexibility and power controls for our device. The chip is the most expensive option, but it also has the most robust SPI interface options. It also has a very high amperage output potential, allowing the team to use more powerful motors. 

## Motor

| Solutions     | Pros          | Cons  |
| :---: | --- | ---|
| Option 1. Pololu 99:1 Gear motor<br>$48/each<br>[datasheet](/https://www.pololu.com/file/0J1829/pololu-25d-metal-gearmotors.pdf) | *High torque<br>*Wide range of operating voltages<br>*Highly available<br>*Affordable<br>*More precise control | *Encoder adds design complexity<br>*High Power Requirements |
| Option 2. Nidel Copal ROB-09238<br>$19/each<br>[datasheet](/https://www.sparkfun.com/datasheets/Robotics/SM-42BYG011-25.pdf) | *Stepper motor gives more precise control<br>*Affordable<br>*High torque<br>*Available from reputable sources | *Little documentation on this device<br>*Extra complexity due to stepper motor features<br>*High power requirements |
| Option 3. Pololu 4798 Brushed Gearmotor<br>$22/each<br>[datasheet](/https://www.pololu.com/product-info-merged/4798) | *Reputable supplier<br>D*low complexity<br>*affordable<br>*high torque<br>*12V Operating Voltage<br>*Good documentation<br> |*Low features<br>*High power requirements<br>*Does not have precise motor control options |

Rationale: For the purposes of the team’s design, the added complexity and precision 

Choice: Option 3. Pololu 4798 Brushed Gearmotorfrom the alternative motor options is not necessary. This motor fits the needs of the design as a high torque motor, and is both affordable and in high availability.

## Power Source

| Solutions     | Pros          | Cons  |
| :---: | --- | ---|
| Option 1. GSM36U12-P1J<br>$20.20 Each<br>[Link to Product](https://www.digikey.com/en/products/detail/mean-well-usa-inc./GSM36U12-P1J/7703544?utm_adgroup=AC%20DC%20Desktop%2C%20Wall%20Adapters&utm_source=google&utm_medium=cpc&utm_campaign=Shopping_Product_Power%20Supplies%20-%20External%2FInternal%20%28Off-Board%29_NEW&utm_term=&utm_content=AC%20DC%20Desktop%2C%20Wall%20Adapters&gclid=Cj0KCQiAorKfBhC0ARIsAHDzsluGIUD1bnuHfUYoWT965rR30j1H4i-8diDKktkW-ko1YF1rsKBDN98aAvoIEALw_wcB) | *Continuous source of 12V<br>*No need to replace components over time<br>*Outputs up to 3 Amps | *Requires a direct connection<br>*Wired connection can be tedious to manage<br>*Limits portability of design |
| Option 2. EN22<br>$2.59/each<br>[Link to product](/https://www.digikey.com/en/products/detail/energizer-battery-company/EN22/704825) | *Affordable<br>*Can withstand high temperatures<br>*Many in stock (digikey) | *Unstable<br>*Output voltage dips from 9V to 5V after a day of use (Constant Output) |
| Option 3. WSU120-1000<br>$13.89/each<br>[Link to product](https://www.digikey.com/en/products/detail/triad-magnetics/WSU120-1000/3094981?utm_adgroup=AC%20DC%20Desktop%2C%20Wall%20Adapters&utm_source=google&utm_medium=cpc&utm_campaign=Shopping_Product_Power%20Supplies%20-%20External%2FInternal%20%28Off-Board%29_NEW&utm_term=&utm_content=AC%20DC%20Desktop%2C%20Wall%20Adapters&gclid=Cj0KCQiAo-yfBhD_ARIsANr56g5ZdsC5GU4-hMFXJSEWiwOSsTKAzypLfcu2jUbFl-nmYrALiw3usm0aArzvEALw_wcB) | *Affordable<br>*12 V output<br>*No need of replacement<br> | *1 Amp output<br> *Limits portability<br>*Power: 12 W<br> |

Choice: Option 1

Rationale: The team opted to use the GSM36U12-P1J power supply due to its ease of use and consistent 12V supply. The loss of portability is made up for by the convenience of not needing to replace batteries after repeated usage.

## Voltage Regulator

| Solutions     | Pros          | Cons  |
| :---: | --- | ---|
| Option 1. MIC5156-5.0YM<br>$4.04 Each<br>[Link to Product](/https://www.digikey.com/en/products/detail/microchip-technology/MIC5156-5-0YM/1030138) | *Input: 3 - 36V<br>*Surface Mount<br>*Affordable<br>*Positive fixed | *Few in stock |
| Option 2. RT9194GE<br>$0.68/each<br>[Link to Product](/https://www.digikey.com/en/products/detail/richtek-usa-inc/RT9194GE/2546985) | *Cheap<br>*Surface Mount<br>*Input: 4.5 - 13.5V | *Positive Adjustable |
| Option 3. LM2575D2T-3.3R4G<br>$2.37/each<br>[Link to Product](https://www.mouser.com/ProductDetail/onsemi/LM2575D2T-3.3R4G?qs=2OtswVQKCOFhf1pTPfoNzA%3D%3D) | *Surface Mount<br>*Switching Voltage Regulator<br>*Input: 4.75 - 40V<br>*3.3V output |  |

Choice: Option 1

Rationale: Option 1 has a wide voltage input which would work for our components and is available for an affordable price. By being a positive fixed type we will avoid having to use external components.

## Power Budget

![image caption](https://cdn.discordapp.com/attachments/1062096006642147503/1079540354677756045/image.png)

[Appendix F: Component Selection](AppendixF_ComponentSelection.md)

[Back to Project Overview](index.md)
