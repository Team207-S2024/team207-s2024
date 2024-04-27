# Software Proposal

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/8b84c7f2-362e-4973-926b-3156ad32424d" />
</p>


<p align="center">
  <i>Figure 1: Full Picture of the Software Proposal</i>
</p>

Shown in the figure above is a diagram of our software proposal. The diagram will give us an outline of our software design and what we would like to accomplish with each subsystem. The rest of the page will be dedicated to going more in-depth with each subsystem. 

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/33bf9d78-d385-4362-b317-615dc874cb9c" />
</p>

<p align="center">
  <i>Figure 2: The Main Loop</i>
</p>

This is the main loop of the system. It goes over all the steps of the loop and showcases what is and isn't meant to be an interrupt. It initializes everything, including enabling interrupts, and then goes into the infinite loop. It first checks for temperature and humidity, then prints alert/home status to the ESP32, and then transfers that data to the MQTT. It will then continuously go through this loop infinitely unless an error occurs. 

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/d7090c55-e8d6-444a-84fd-04a7082b39dc" />
</p>

<p align="center">
  <i>Figure 4: The Humidity and Temperature Reads</i>
</p>

These are two of the three interrupts. They consist of reading and converting the data from the humidity and temperature sensors, then continuously print that data to the ESP32/MQTT server. 

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/6967764a-ae32-4fc6-98e1-c420724b97fa" />
</p>

<p align="center">
  <i>Figure 5: The Check for Manual Action Interrupt</i>
</p>

This is the third and final interrupt. It consists of reading the EUSART data from the MQTT to the ESP32 to the PIC microcontroller, and depending on that data it will change the action it does. H makes it go home and O makes it go outside. One thing to note is that does have to make a check whether it's home/outside first before making the movement, otherwise it will cause issues such as dragging the platform out of position and potentially cause damage to the system. 1 and 0 make it move manually so you can attempt to configure it properly according to your needs. 

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/6967764a-ae32-4fc6-98e1-c420724b97fa" />
</p>

<p align="center">
  <i>Figure 6: The Initialize System Action</i>
</p>
This is the first action the system takes. It initializes all variables used in the system and sets them to specific values. It also establishes communication between the ESP32 and the PIC microcontroller. 

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/a566cb06-7fa1-4c70-8947-d00d5137d645" />
</p>

<p align="center">
  <i>Figure 7: The Check Temperature Action </i>
</p>

This is the first major 'check' that will move things in the system. It checks if the tempData it gained from the temperature sensor is under a certain value, and depending on if it is it'll go further down the tree, moving either in or out of 'home.' Home in this case is the shelter that will keep the plant in the shade. 

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/a5575a37-5515-45ec-8b08-33b397c96d3b" />
</p>

<p align="center">
  <i>Figure 8: The Check Humidity Action </i>
</p>

This is the second major 'check.' It will check the humData it gained from the humidity sensor is under a certain value, and depending on if it is or isn't will change the variable 'alert' accordingly. 

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/43162e56-2531-4adf-ba5f-b3c71b59c26e" />
</p>

<p align="center">
  <i>Figure 9: The Motor Movements </i>
</p>

These are the two significant motor movements that happen. They are equivocal other than the direction they move the motor. The motor driver itself works best when used in tandem with delays, which is why it's set up the way it is. 

# MQTT Table

Here is the MQTT Topic Table we used to determine how best to go about developing our ESP32 Code: 

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/0ea8b264-448c-4806-b154-7555bd1155ee" />
</p>

<p align="center">
  <i>Figure 18: MQTT Table </i>
</p>

# MPLAB X Configuration



# Code



[Back to Home Page](/team207-s2024)

[Back to Report](report)
