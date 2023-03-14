---
Title: Component Selection
---

## Temperature Sensor Module

The team selected the TC74A4-3.3VCTTR to use for our temperature sensor. We selected this because it meets the course requirements for a serial sensor. This sensor uses I2C and has an address of 1001101b which is compatible with the other I2C sensor we are planning on using. In addition to these factors this sensor was used earlier in the class which is beneficial to the team as it means the team has some experience with it and it will be easier to get help from the teaching team if we run into issues during the development process. The datasheet can be found [here](https://www.digikey.com/en/htmldatasheets/production/48489/0/0/1/tc74.html) and purchasing information is [here](https://www.digikey.com/en/products/detail/microchip-technology/TC74A4-3-3VCTTR/443268) 

![image caption](https://media.digikey.com/Renders/Microchip%20Tech%20Renders/150~C04-091~CT,%20OT~5.JPG)

## Hall Effect Sensor

The team selected the AS5600-ASOM to use for our hall effect sensor. This sensor meets the course requirements for a second serial sensor. This sensor is also I2C and has an address of 0110110b, which is compatible with the address of the temperature sensor we are using. This is also a sensor that was used in an earlier class activity so we have some experience reading the data from this sensor over I2C and we can also easily acquire assistance from the teaching team if we have any problems while developing the project. The datasheet can be found [here](https://ams.com/documents/20143/36005/AS5600_DS000365_5-00.pdf) and purchasing information is [here](https://www.digikey.com/en/products/detail/ams-osram/as5600-asom/4914332) 

![image caption](https://media.digikey.com/Renders/AMS%20Renders/8-SOIC.jpg)

## Motor Driver

The team selected the IFX9201SGAUMA1 to use for our project. This motor driver offers the most in terms of flexibility and power controls for our device. The chip is the most expensive option that we evaluated, but it also has the most robust SPI interface options. It also has a very high amperage output potential, allowing the team to use more powerful motors. The datasheet can be found [here](https://www.infineon.com/dgdl/Infineon-IFX9201SG-DS-v01_01-EN.pdf?fileId=5546d4624cb7f111014d2e8916795dea&ack=t) and the purchasing information can be found [here](https://www.digikey.com/en/products/detail/infineon-technologies/IFX9201SGAUMA1/5415542) 

![image caption](https://media.digikey.com/Renders/Infineon%20Renders/P-PG-DSO-12.jpg)


## Motor

The team selected the Pololu 4798 Brushed Gearmotor. Initial analysis of the intended design showed that a more powerful motor was probably not necessary. This motor fits the needs of the design as a high torque motor, and is both affordable and in high availability. The datasheet can be found [here](https://www.pololu.com/file/0J1487/pololu-micro-metal-gearmotors_rev-5-1.pdf) and purchasing information can be found [here](https://www.pololu.com/product-info-merged/4798)

![image caption](https://a.pololu-files.com/picture/0J10347.600x480.jpg?e7efd719c3e6608dbcd8d5faedd04593)

## Power Source

The team opted to use the GSM36U12-P1J power supply due to its ease of use and consistent 12V supply. The loss of portability is made up for by the convenience of not needing to replace batteries after repeated usage. The datasheet can be found [here](https://www.digikey.com/en/htmldatasheets/production/2488774/0/0/2/gst36u05-p1j.html) and purchasing information can be found [here](https://www.digikey.com/en/products/detail/mean-well-usa-inc/GST36U12-P1J/7703698)

![image caption](https://media.digikey.com/Photos/Mean-Well-USA-Inc/MFG_GST36U.jpg)

## Voltage Regulator

Due to requirements for the course project the team needed to select a switching power regulator. The team opted to select the LM2575D2T-3.3R4G to use. This is a fixed 3.3V regulator. This was an ideal feature for this project as it meant that it would be unlikely for a design miscalculation to send the wrong voltage into the other components of our system. This voltage regulator also has great documentation with full design suggestions and component recommendations for different use cases. The team also worked with the through hole variant of this sensor in class and is familiar with necessary support circuitry to make this regulator work in our project. The datasheet can be found [here](https://www.mouser.com/datasheet/2/308/LM2575_D-1810711.pdf) and purchasing information can be found [here](https://www.mouser.com/ProductDetail/onsemi/LM2575D2T-3.3R4G?qs=2OtswVQKCOFhf1pTPfoNzA%3D%3D) 

![image caption](https://www.mouser.com/images/mouserelectronics/images/D2PAK_5_DSL.jpg)

# Power Budget

![image caption](https://cdn.discordapp.com/attachments/1062096006642147503/1079540354677756045/image.png)

[Appendix E: Component Selection](AppendixE_ComponentSelection.md)

[Back to Project Overview](index.md)
