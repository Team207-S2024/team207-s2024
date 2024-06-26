# Hardware Implementation

## Current Schematic

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/e467231a-3d5f-42f2-8d60-e518621b26a3" />
</p>

<p align="center">
  <i>Figure 1: Picture of the Final Schematic</i>
</p>

Here is team 207's final itteration of the hardware implementation. Each major part was made separately according to each subsystem and then put together with one another in the final schematic. Many of the components were able to be imported from sites like Ultra Librarian, which helped to speed up the process, but some required custom symbols and footprints. 

An in-depth look at each part of the schematic will be shown below. 

### Power Supply

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/7fe77546-292f-4d11-b718-ac96efad69c5" />
</p>

<p align="center">
  <i>Figure 2: The Power Supply Subcircuit </i>
</p>

As the power supply's existence is how every other circuit can function, it stands to reason that it should be discussed first. It will be getting power from a 9 V battery, which will be placed in a battery holder within the product. Then, to protect the circuit, it will first be going through a fuse. Then, it goes through to a bypass capacitor to ground, as well as providing 9 V to the motor. It then goes into our switching voltage regulator, which will regulate it down to 3.3 V for the rest of the circuit. The subcircuit itself is a direct recreation of the typical application circuit found on the datasheet. The group wasn't sure if it was necessary to have a power switch, but that might be a feature later on that is implemented. 

**3.3 V Logic:**

[Microcontroller Subcircuit](#microcontroller)

[MCLR Subcircuit](#mclr)

[ESP32 Subcircuit](#esp32)

[Motor Driver Subcircuit](#motor-driver)

[Humidity Sensor Subcircuit](#humidity-sensor)

[Temperature Sensor Subcircuit](#temperature-sensor)

**9 V Logic:**

[Motor Driver Subcircuit](#motor-driver)

### Microcontroller

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/956c9b56-e793-4c82-850e-57ddc9a2289c" />
</p>

<p align="center">
  <i>Figure 3: The Microcontroller Subcircuit </i>
</p>

The microcontroller is where every other part of the circuit communicates with one another, it's next on the list. Here, it's shown where each other part connects to it through the many ports shown. The programmer that the group will be utilizing will be connecting through a 5-pin header, as can be seen at the top. Also, note another bypass capacitor to further protect the circuit. 

### MCLR 

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/f28e2d18-7b66-4881-8f2f-3b85fb215318" />
</p>

<p align="center">
  <i>Figure 4: The MCLR Subcircuit </i>
</p>

The purpose of the MCLR circuit is to help reset the device without having to turn the entire device off by unplugging or disconnecting the power source. The subcircuit is directly from the microcontroller's datasheet. Rather than a switch, a jumper was used because when the programming is finalized, it won't be necessary to turn it on or off. 

### Debugging LEDs

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/6550d1e3-c768-4073-8adc-2d5983046399" />
</p>

<p align="center">
  <i>Figure 5: The Debugging LEDs Subcircuit </i>
</p>

For the sake of debugging, and seeing a visual cue as to when certain things are done, debugging LEDs were considered necessary for this project. The group decided on 1 set of RGB LEDs, and an extra green LED. In likelihood, each set of lights being on will be a signal for certain triggers (or lack thereof). They each connect to a different GPIO pin on the microcontroller and have a ballast resistor to help in not burning up. 

### ESP32

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/b6357f6a-bd35-44db-934a-0e68c5276003" />
</p>

<p align="center">
  <i>Figure 6: The ESP32 Subcircuit </i>
</p>

The ESP32 is how the device will be connecting to WiFi. It will be transmitting and receiving data from the microcontroller through the pins shown, as well as showing data through an OLED, the pins of which can be seen at the top. 

### Motor Driver

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/5d7841f7-4e6d-4b2c-b929-5082b02e9f58" />
</p>

<p align="center">
  <i>Figure 7: The Motor Driver Subcircuit </i>
</p>

The motor driver is responsible for transmitting data about the motor, as well as receiving data from the microcontroller to move the motor in a certain way. It is an SPI-based motor driver and utilizes the pins necessary for that method of serial communication. The circuit was found in the datasheet.

### Humidity Sensor

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/17a1fc93-692a-43d0-8735-8819036da57a" />
</p>

<p align="center">
  <i>Figure 8: The Humidity Sensor Subcircuit </i>
</p>

The humidity sensor will transmit data that it gets from the soil to the microcontroller. It will be using I2C communication. The circuit was obtained from the datasheet.

### Temperature Sensor

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/blob/main/images/hardwareproposal/mycirc.png?raw=true" />
</p>

<p align="center">
  <i>Figure 9: The Temperature Sensor Subcircuit </i>
</p>

The temperature sensor will transmit data that it gets from the area to the microcontroller. It will be using I2C communication. The circuit was obtained from the datasheet. 

## Bill of Materials

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/1ef5e5f5-9ff8-4b29-bb65-1513908fb523" />
</p>

<p align="center">
  <i>Figure 10: The Bill of Materials </i>
</p>


[Back to Home Page](/team207-s2024)

[Back to Report](report)
