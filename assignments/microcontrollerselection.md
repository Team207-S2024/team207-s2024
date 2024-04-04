# Microcontroller Selection

The project team embarked on a rigorous selection process to identify the optimal microcontroller, commencing with a comprehensive analysis of project-specific requisites derived from meticulous problem definition and block diagram assessment. With a keen emphasis on critical factors such as GPIO pins, ADC channels, PWM channels, and communication interfaces encompassing I2C, SPI, and UART, the team prioritized ensuring seamless compatibility with the project's intricate needs.

Subsequently, the team engaged in an exhaustive research and evaluation phase, meticulously scrutinizing three potential microcontroller options: PIC18LF26K22, PIC16F18124, and PIC16F18855. Leveraging a comprehensive array of resources including datasheets, product pages, application notes, code examples, and external references, each microcontroller underwent rigorous assessment. Key considerations such as production unit cost, supply voltage range, maximum current, architecture, available IC packages, and programming capabilities were meticulously weighed.

## Microcontroller Selection Table
***
### 1. Project Specific Requirments and Datasheet Specifications

| Design Considerations  | Team Project Requirments | PIC Option 1 | PIC Option 2 | PIC Option 3 |
| ---------------------- | ------------------------ | ------------ | ------------ | ------------ |
| How many GPIO Pins?  | 6 (debug leds) minimum  | 28 | 2 | 24 |
| Built-in Analog to Digital Converter? How many?  | 0 (shouldn’t need any for sensors picked)  | 0 | 1 | 24 |
| Built-in Hardware PWM? How many? | Need at least 1 | 2 | 2 | 2 |
|Built-in I2C? SPI? How many? | Need at least 2 I2C and 1 SPI | (2,2) | (2,2) | (2,2) |
| Built-in UART? How many? | Need at least 1 pin (ESP32) | 2 | 1 | 2 |
|Additional considerations specific to your project specifications (optional)| Since our project will be outside it must be able to operate from 0C-45C minimum | -40℃ to 85℃ | -40℃ to 85℃ | -40℃ to 85℃ |

***

### 2. Microcontroller Information and Part Details

| Microcontroller Considerations  | Instructions | PIC Option 1 | PIC Option 2 | PIC Option 3 |
| ------------------------------- | ------------ | ------------ | ------------ | ------------ |
| Part Number | Entire Part Number | PIC18F25J11 | PIC18F46Q24 | PIC18F26K40 |
| Link (URL) to Product Page | Do not paste links directly into the table. Instead, like them using a short URL command | [Link](https://www.microchip.com/en-us/product/PIC18F25J11) | [Link](https://www.microchip.com/en-us/product/PIC18F46Q24#document-table) | [Link](https://www.microchip.com/en-us/product/pic18f26k40) |
| Link (URL) to Data Sheets |  | [Link](https://ww1.microchip.com/downloads/aemDocuments/documents/OTH/ProductDocuments/DataSheets/39932D.pdfl) | [Link](https://ww1.microchip.com/downloads/aemDocuments/documents/MCU08/ProductDocuments/DataSheets/PIC18F26-45-46-55-56Q24-Microcontroller-Data-Sheet-XLP-DS40002503.pdf) | [Link](https://ww1.microchip.com/downloads/en/DeviceDoc/PIC18LF26-45-46K40-Data-Sheet-DS40001816F.pdf) |
| Link (URL) to Application Notes |  | [Link](https://www.microchip.com/en-us/application-notes/an1267.html) | [Link](https://www.microchip.com/en-us/application-notes/tb2669) | [Link](https://ww1.microchip.com/downloads/aemDocuments/documents/MCU08/ApplicationNotes/ApplicationNotes/TB3261-Technical-Brief-DS90003261A.pdf) | 
| Link (URL) to Code Examples |  | [Link](https://ww1.microchip.com/downloads/en/DeviceDoc/30009687F.pdf) | N/A | N/A |
| Production Unit Cost | Find in the Microchip online store, or Digikey | $3.49 | $2.16 | $1.88 |
| Supply Voltage Range | Find in the Microcontroller Datasheet | 2.0V to 3.6V | 1.8V to 5.5V | 1.8V to 5.5V |
| Absolute Maximum Current for entire IC | Find in the Microcontroller Datasheet | 300mA | 300mA | 350mA |
| Maximum GPIO Pin Current | Find in the Microcontroller Datasheet | 25mA | 25mA | 50mA |
| 8-bit or 16-bit Architecture | Find in the Microcontroller Datasheet | 8-bit | 8-bit | 8-bit |
| Available IC Packages/Footprints | Find in the microcontroller datasheet. Choose a microcontroller with both surface mount and DIP/through-hole packages available. See Most Common Mistakes below for requirements to improve manufacturing reliability. | SOIC (SM) | SOIC (SM) | SOIC (SM) |
| Supports External Interupts? | Find in the Microcontroller Datasheet | 4 | 3 | 3 |
| In-System Programming Capability and Type | Allows for programming the microcontroller without removing it from the PCB. Find in the microcontroller datasheet. | ICSP | PDID | ICSP |
| Programming Hardware, Cost, and URL | Find on the Microcontroller Product Page | [SnapDebug](https://www.microchip.com/en-us/development-tool/PG164100) | [SnapDebug](https://www.microchip.com/en-us/development-tool/PG164100) | [SnapDebug]([https://www.microchip.com/en-us/development-tool/dv244140](https://www.microchip.com/en-us/development-tool/PG164100)) |
| Works with MPLAB® X Integrated Development Environment (IDE)? | Required | Yes | Yes | Yes |
| Works with Microchip Code Configurator? | Required | Yes | Yes | Yes |

***

### 3. Overall Pros, Cons, and Rankings for chosen Microcontrollers 

| Overall Pros, Cons, and Rankings | Two for each | PIC Option 1 | PIC Option 2 | PIC Option 3 |
| -------------------------------- | -------------| -------------| -------------| -------------|
| Overall Pros                     | Two Each     | 1. Has both I2C and SPI pins so we can use both at the same time. 2. In depth Datasheet. | 1. Meets all requirements with redundancy on necessary features. 2. Cost-effective | 1. Has an ample amount of I/O pins 2. Enhanced core features with multiple PWM and EUSART modules for serial communication. 3. Used in Previous Assignments. |
| Overall Cons                     | Two Each     | 1. No External ADC. 2. Few/Limited code examples | 1. No External ADC. 2. Only one extra EUSART Port. | 1. Limited GPIO ports. 2. Less pins equates to fewer functions and features. |
| Rankings                         | First Choice = 2, Second Choice = 3, Third Choice = 1 | 2 | 3 | 1 |

***

### 4. Final Microcontroller Choice and Rationale

**Choice:** Option 1

**Rationale:**
Throughout this discerning evaluation process, each microcontroller was subjected to a comprehensive analysis of its strengths and weaknesses. Prospective advantages such as comprehensive code examples and ample I/O pins were carefully juxtaposed against potential limitations, including constraints such as limited program memory or processing power.

Upon meticulous deliberation and discernment, the team methodically ranked the options based on their alignment with the project's intricate requirements. Ultimately, following careful consideration, the team arrived at the definitive selection of the PIC18F26K40 microcontroller as the most fitting choice. This decision reflects a strategic alignment with the project's multifaceted needs and embodies a commitment to leveraging advanced technology to realize project objectives with unparalleled efficiency and effectiveness.
