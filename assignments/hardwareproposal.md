# Hardware Proposal

## Current Schematic

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/35e53270-3269-4ff1-bcc7-de6780c168e8" />
</p>

<p align="center">
  <i>Figure 1: Picture of the Full Schematic</i>
</p>

Here is the current iteration of the team's hardware proposal. Each major part was made separately according to each subsystem and then put together with one another in the final schematic. Many of the components were able to be imported from sites like Ultra Librarian, which helped to speed up the process, but some required custom symbols and footprints. 

An in-depth look at each part of the schematic will be shown below. 

### Power Supply

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/a355064f-b398-4bc1-82af-38ed8e6aaf2a" />
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
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/00458cd9-c30d-41ca-a94f-15b3d3ee700d" />
</p>

<p align="center">
  <i>Figure 3: The Microcontroller Subcircuit </i>
</p>

The microcontroller is where every other part of the circuit communicates with one another, it's next on the list. Here, it's shown where each other part connects to it through the many ports shown. The programmer that the group will be utilizing will be connecting through a 5-pin header, as can be seen at the top. Also, note another bypass capacitor to further protect the circuit. One final note, although RB0 is ported, that is an error due to a previous iteration of this schematic having it connected to a header pin. Please ignore it, as it was a mistake to keep it on the schematic. 

### MCLR 

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/34626180-2637-4ac3-b88f-43444438cb71" />
</p>

<p align="center">
  <i>Figure 3: The MCLR Subcircuit </i>
</p>

The purpose of the MCLR circuit is to help reset the device without having to turn the entire device off by unplugging or disconnecting the power source. The subcircuit is directly from the microcontroller's datasheet. Rather than a switch, a jumper was used because when the programming is finalized, it won't be necessary to turn it on or off. 

### Debugging LEDs

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/d40d4481-5e78-4330-b2ff-6f46fd722d41" />
</p>

<p align="center">
  <i>Figure 4: The Debugging LEDs Subcircuit </i>
</p>

For the sake of debugging, and seeing a visual cue as to when certain things are done, debugging LEDs were considered necessary for this project. The group decided on 1 set of RGB LEDs, and an extra green LED. In likelihood, each set of lights being on will be a signal for certain triggers (or lack thereof). They each connect to a different GPIO pin on the microcontroller and have a ballast resistor to help in not burning up. 

### ESP32

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/af26bcc2-62c0-428a-a3a7-de9590d6e595" />
</p>

<p align="center">
  <i>Figure 5: The ESP32 Subcircuit </i>
</p>

The ESP32 is how the device will be connecting to WiFi. It will be transmitting and receiving data from the microcontroller through the pins shown, as well as showing data through an OLED, the pins of which can be seen at the top. 

### Motor Driver

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/cf909e8f-e225-42d3-a776-2e4af7331ebf" />
</p>

<p align="center">
  <i>Figure 5: The Motor Driver Subcircuit </i>
</p>

The motor driver is responsible for transmitting data about the motor, as well as receiving data from the microcontroller to move the motor in a certain way. It is an SPI-based motor driver and utilizes the pins necessary for that method of serial communication. The circuit was found in the datasheet.

### Humidity Sensor

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/3d8fe90c-e65a-412b-8a9b-1501cffc16ad" />
</p>

<p align="center">
  <i>Figure 6: The Humidity Sensor Subcircuit </i>
</p>

The humidity sensor will transmit data that it gets from the soil to the microcontroller. It will be using I2C communication. The circuit was obtained from the datasheet.

### Temperature Sensor

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/8f2b63e9-ec32-437d-bbe8-6d3a80174c3a" />
</p>

<p align="center">
  <i>Figure 6: The Temperature Sensor Subcircuit </i>
</p>

The temperature sensor will transmit data that it gets from the area to the microcontroller. It will be using I2C communication. The circuit was obtained from the datasheet. 

## Bill of Materials

[Back](/team207-s2024)

