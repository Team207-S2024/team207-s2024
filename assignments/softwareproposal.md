# Software Proposal

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/157151171/28a8e842-8534-4c73-9b45-f04b8580a899" />
</p>


<p align="center">
  <i>Figure 1: Full Picture of the Software Proposal</i>
</p>

Shown in the figure above is a diagram of our software proposal. The diagram will provide an ample outline of our software design and what we wish to accomplish with each subsystem. The rest of the page will be dedicted to going more in-depth with each subsystem. 

[Microcontroller](#microcontroller)

[Humidity/Temperature Sensors](#humidity-and-temperature-sensors)

## Microcontroller  

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/157151171/140d4266-cc05-446d-b7d4-ed13b9fd61fb" />
</p>

<p align="center">
  <i>Figure 2: The Main Loop</i>
</p>

This is our main software design for the microcontroller. Our main loop will consist of receiving data from all 3 subsystems, the humidity sensor, the motor driver, and the temperature sensor. The microcontroller will then use this data to make its next decision. It will keep this cycle going until a decision is made or the device is turned off. 

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/157151171/bfa35d21-f6aa-48fc-b736-0673d750a493" />
</p>


<p align="center">
  <i>Figure 3: The Interrupts</i>
</p>

This figure goes into more detail about the specifics of the microcontroller function. The section on the right details how our microcontroller will decide when the motor driver has reached the optimal temperature spot that was determined previously. The middle two sections detail how we converge the data into I2C and use I2C to communicate with the motor driver. 

[Link to main](#software-proposal)

## Humidity and Temperature Sensors

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/157151171/003d0f2e-2936-4e06-9024-af9bdbed61ee" />
</p>

<p align="center">
  <i>Figure 4: The Logic Checks </i>
</p>

Our humidity and temperature sensors will be the microcontroller's main factors in deciding which action to take next. The temperature sensor will be scanning the nearby area for hotspots. If a hotspot is found, then a signal will be sent to the Microcontroller. The Microcontroller will then use this information and send it to the motor driver, signaling it to rotate the pot facing this hotspot. Our logic is that where a hotspot is located, that's the spot receiving the most sunlight. 

The humidity sensor will be our way of implementing wi-fi capability into this project. If the humidity sensor detects soil humidity that is too low based on the specific information provided by the user, then it will alert the user that the plants require water. 

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/157151171/5b2fb5da-69f8-48ce-ba2a-9701ce869a34" />
</p>


<p align="center">
  <i>Figure 5: The Motor </i>
</p>

The diagram above displays the main way the motor driver receives information and processes them. The data from the humidity and temp sensors will be converted to EUSART. The EUSART data will then be read by the microcontroller and sent to the motor driver, which will inform it of which direction to move and how far.  

[Link to main](#software-proposal)

[Back to Home Page](/team207-s2024)

[Back to Report](report)







