---
Title: Appendix F Microcontroller Selection
---

## Microcontroller Options

| Design Considerations | Team Project-Specific Requirements<br>from Problem Definition and Block Diagram | PIC<br>Option1 | PIC<br>Option2 | PIC<br>Option3 |
| --- | --- | :---: | :---: | :---: |
| How many GPIO Pins? | 13 (3 LED, 1 Button, 3 CS SPI, 2 SPI, 2 I2C, 2 UART) | 25 | 16 | 25 |
| Built-in Analog to Digital Converter?<br>How many? | 0 | 1 | 1 | 1 |
| Built-in Hardware PWM?<br>How many? | 0 | 2 | 0 | 2 |
| Built-in I2C? SPI? How many? | 1 I2C 1 SPI  | 1 I2C<br>1 SPI | 2 | 2 |
| Built-in UART? How many? | 13 (3 LED, 1 Button, 3 CS SPI, 2 SPI, 2 I2C, 2 UART) | 2 | 2 | 2 |
| Other Required Built-In Features? (optional) | --- | --- | --- | --- |
| Additional considerations specific<br>to your project specifications (optional) | --- | --- | --- | --- |

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

## Microcontrollers pros and cons
| --- | PIC18F26K40 | PIC18F27J53 | PIC18F27K40 |
| --- | :---: | :---: | :---: |
| Overall Pros | *Low Power<br><br> *In Circuit Debug | *Large memory<br><br> *Sleep mode | *Large memory<br><br> *Low Power |
| Overall Cons | *Less memory which may cause issues while developing code<br><br> *Higher Voltage Requirement | *High unit cost for functionality that is not useful for project <br><br> *Missing features that might help with debugging the code | *Support for many features may make debugging more difficult<br><br> *Currently Available PDIP and Surface mount parts have different voltage ranges |
| Ranking | 2 | 3 | 1 |

## Final Microcontroller Choice: PIC18F27K40

Rationale: The PIC18F27K40 Has both I2C and SPI support giving the team the most flexibility for sensors. The PIC also has a large amount of program memory available which will assist during development as less time will be spent optimizing for storage space. This PIC is also available in both Through hole and Surface mount from microchip currently. The PIC also has a development board available for it giving the team more options for development of the team's software. This PIC is also supported in MCC Melody. There are also many application notes about using the PIC on the Microchip website. 

[Back to Microcontroller Selection](MicrocontrollerSelection.md)

[Back to Project Overview](index.md)
