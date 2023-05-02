---
Title: Software Proposal
---

# Software Proposal

* Code starts off by initializing our program which includes EUSART, TIMER, I2C, and SPI. 

* Then Sensors start reading data continuing until power is cut off

* As sensors read data this is telling the motor which way to rotate, either retracting or extenting the cover. If wind speed is above 15MPH or temperature is below 32 degrees F, motor extends cover. As long as wind speed is below 15MPH and temperature is above 32 degrees, cover will be retracted.


![image caption](https://cdn.discordapp.com/attachments/1062096006642147503/1100165876713529494/Software_Proposal.drawio.JPG)

## Biggest Changes:

1) Implimented Interrupts into how the motor will be controlled
2) Made it so hall effect sensor and temp sensor are on a constant loop to constantly read values
3) Edited how systems being initialized

## Improvements:

* Impliment sensors to control far the motor extends and retracts
* Made the hall effect sensor change the motor on higher Rev/min

[Back to Appendix H: Software Proposal](AppendixH_SoftwareProposal.md)

[Back to Project Overview](index.md)
