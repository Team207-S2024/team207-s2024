# Block Diagram

## Block Diagram Picture

The team constructed a Block Diagram that provides an ample overview of how we want our project to function.

![BlockDiagram.drawio.png](main/images/blockdiagram/BlockDiagram.drawio.png)

Figure 1: Block Diagram of our Flower Pot

## Overview of Each Section

### Microcontroller

![BlockMicro.png](https://github.com/Team207-S2024/team207-s2024/blob/main/images/blockdiagram/BlockMicro.png)

The PIC18LF26K40

This is the most important part of our project, the Microcontroller. The Microcontroller that we have decided to work with is the PIC18LF26K40. We chose it mainly for its small amount of pins which helps with keeping our project simple and easy to manage. It also contains 2 MSSP ports. This is advantageous for us as it will allow us to run both SPI and I2C.

### Temperature Sensor
![BlockTemp.png](https://github.com/Team207-S2024/team207-s2024/blob/main/images/blockdiagram/BlockTemp.png)

The Temperature Sensor

The temperature sensor is one of the subsystems we decided to work with. We plan on utilizing the temperature sensor to detect where the highest temperature in the surrounding area is. This information will then be utilized by the microcontroller and will send this data to the motor. THe motor will then rotate the flower pot to face the direction of the highest tmeperature. 


