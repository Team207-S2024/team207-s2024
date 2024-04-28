# Block Diagram

## Block Diagram Picture

The team constructed a Block Diagram that provides an ample overview of how we want our project to function.

![BlockDiagram](https://github.com/Team207-S2024/team207-s2024/assets/152089525/1afb00d2-32d5-43ba-bf59-3c1db267d4e1)

_Figure 1: Block Diagram of our Flower Pot_

## Overview of Each Section

### Microcontroller
![BlockDiagram Microcontroller](https://github.com/Team207-S2024/team207-s2024/assets/152089525/f1619ad7-2013-472d-91ab-15c4dad73b37)

_Figure 2: The PIC18LF26K40_

This is the most important part of our project, the Microcontroller. The Microcontroller that we have decided to work with is the PIC18LF26K40. We chose it mainly for its small amount of pins which helps with keeping our project simple and easy to manage. It also contains 2 MSSP ports. This is advantageous for us as it will allow us to run both SPI and I2C.

### Temperature Sensor
![BlockDiagram Temp](https://github.com/Team207-S2024/team207-s2024/assets/152089525/7023ac8d-8633-4e55-8bba-719a3fe40e27)

_Figure 3: The Temperature Sensor_

The temperature sensor is one of the subsystems we decided to work with. We plan on utilizing the temperature sensor to detect where the highest temperature in the surrounding area is. This information will then be utilized by the microcontroller and will send this data to the motor. THe motor will then rotate the flower pot to face the direction of the highest tmeperature. 

### Motor Driver

![BlockDiagram Motor](https://github.com/Team207-S2024/team207-s2024/assets/152089525/bcd235ba-eb89-4bd4-a68d-7227c8c0c474)

_Figure 4: The Motor Driver/Actuator_

The motor driver is what will rotate the flower pot to face the sun. This device is meant to be placed on a windowsill or outside area and will rotate the pot to face the sun. The motor driver will determine where the sun is located based on where it detects the highest temperatures point near it. 

### Humidity Sensor

![BlockDiagram Humidity](https://github.com/Team207-S2024/team207-s2024/assets/152089525/7d407237-c929-4fe0-83a2-43b559c05d77)

_Figure 5: Humidity Sensor_

The humidity sensor will be our main way of communicating with the ESP32 Wifi module. The humidity sensor will be constanly tracking the humidity of the soil in the flower pot. If the sensor detects that the humidity is too low, it will send an alert to your phone notfiying you that the plant requires water.

[Back to Home Page](/team207-s2024)

[Back to Report](report)

