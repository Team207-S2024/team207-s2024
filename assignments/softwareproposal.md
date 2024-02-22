# Software Proposal
  ![07-Software-Proposal drawio](https://github.com/Team207-S2024/team207-s2024/assets/157151171/1cf9c85b-175a-42b8-bdc6-fe0351766d09)

Shown in the figure above is a diagram of our software proposal. The diagram will provide an ample outline of our software design and what we wish to accomplish with each subsystem. The rest of the page will be dedicted to going more in-depth with each subsystem. 

[Microcontroller](##Microcontroller)

[Humidity/Temperature Sensors](##humidity_and_temperature_sensors)

## Microcontroller  
![Software main true](https://github.com/Team207-S2024/team207-s2024/assets/157151171/140d4266-cc05-446d-b7d4-ed13b9fd61fb)

This is our main software desing for the microcontroller. Our main loop will conssit of receiving data from all 3 subsystems, the humidity sensor, the motor driver, and the temeperature sensor. THe microcontroller will then use this data to decide its next decision. It will keep this cycle going until a decision is made or the device is turned off. 

[Link to main](#Software_proposal)

## Humidity and Temperature Sensors

![SoftwareTempHum](https://github.com/Team207-S2024/team207-s2024/assets/157151171/55ac3fb3-a595-4835-aec8-be3be23cc7d1)

Our humidity and temperature sensors will be the microcontrollers main factors in deciding which action to take next. The temperature sensor will be scanning the nearby area for hotspots. If a hotspot is found, then a signal will be sent to the Microcontroller. The Microcontroller will then use this information and send it to the motor driver, signaling it to roate the pot facing this hotspot. Our logic is that where a hotspot is located, thats the spot receiving the most sunlight. 

The humidity sensor will be our way of implementing wi-fi capability into this project. IF the humidity sensor detects a soil humidity that is too low based on the specific information provided by the user, then it will alert the user that the plants requires water. 
![MotorTempSoft](https://github.com/Team207-S2024/team207-s2024/assets/157151171/e592f06f-c8c3-42c5-b11e-07ef7782149e)


The diagram above displays the main way the motor driver recieves information and processes them. The data from the humidity and temp sensors will be converted to EUSART. The EUSART data will then be read by the microcontroller and sent to the motor driver, which will inform it of which direction to move and how far.  



[Link to main](#Sofware_proposal)





