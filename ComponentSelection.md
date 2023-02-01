---
Title: Component Selection
---

## Temperature Sensor Module

| Solutions     | Pros          | Cons  |
| :---: | --- | ---|
| Option 1. TC74A4-3.3VCTTR<br>$1.09/each<br>Link to Product | *Surface Mount<br>*Cheap<br>*Range: -40 to 125 C<br>*Digital output<br>*Voltage: 2.7 to 5.5 V<br>*Standby modeI2C output | *Small and difficult to solder<br>*2 degree accuracy |
| Option 2. TMP126DCKR<br>$3.01/each<br>Link to Product | *Digital output<br>Range: -55 - 175 C<br>*Voltage: 1.62 - 5.5 V<br>*One-shot, Shutdown mode, Sleep mode<br>*.3 degree accuracy<br>*Surface mount | *Expensive compared to others<br>*Voltage Output |
| Option 3. TMP126NDCKR<br>$2.03 /each<br>Link to Product | *Digital Output<br>*Range: -55 - 150 C<br>*Voltage 1.62 - 5.5 V<br>*One-shot, Shutdown mode, Sleep mode<br>*.8 degree Accuracy<br>*SPI output |  |

Choice: Option 1

Rationale: One reason why we choose this sensor is because of the output type, we need either SPI or I2C. In addition to this, we will be working with Option 1 in class, this will make it easier on the team to apply this sensor to our product.

## Hall Effect Sensor

| Solutions     | Pros          | Cons  |
| :---: | --- | ---|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

Choice: Option 2: AS5600-ASOM

Rationale: This option seemed most rational because it contains most of the pros with the least amount of cons. Also able to work with different voltages and in a wide range of temperatures. This chip is also one we have worked with in the past so there's less of a learning curve.

## Motor Module

| Solutions     | Pros          | Cons  |
| :---: | --- | ---|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

Choice: Option 1: L9958

Rationale: The L9958 offers the most in terms of flexibility and power controls for our device. The chip is the most expensive option, but it also has the most robust SPI interface options. It also has a very high amperage output potential, allowing the team to use more powerful motors. 

## Motor

| Solutions     | Pros          | Cons  |
| :---: | --- | ---|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

Rationale: For the purposes of the team’s design, the added complexity and precision 

Choice: Option 3. Pololu 4798 Brushed Gearmotorfrom the alternative motor options is not necessary. This motor fits the needs of the design as a high torque motor, and is both affordable and in high availability.

## Power Source

| Solutions     | Pros          | Cons  |
| :---: | --- | ---|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

Choice: Option 1

Rationale: The team opted to use the AC/DC 12V power supply due to its ease of use and consistent 12V supply. The loss of portability is made up for by the convenience of not needing to replace batteries after repeated usage.

## Voltage Regulator

| Solutions     | Pros          | Cons  |
| :---: | --- | ---|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

Choice: Option 1

Rationale: Option 1 has a wide voltage input which would work for our components and is available for an affordable price. By being a positive fixed type we will avoid having to use external components.

[Appendix E: Component Selection](AppendixD_ComponentSelection.md)

[Back to Project Overview](index.md)
