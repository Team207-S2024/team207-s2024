<style>
table, th, td {
  border: 2px solid black;
  border-collapse: collapse;
  margin: 10px;
  padding: 5px;
}
th, td {
  border-color: #666666;
  background-color: #FFFFFF;
  text-align: left;
}
th {
  background-color: #D5D5D5;
}
</style>

# Microcontroller Selection

The project team embarked on a rigorous selection process to identify the optimal microcontroller, commencing with a comprehensive analysis of project-specific requisites derived from meticulous problem definition and block diagram assessment. With a keen emphasis on critical factors such as GPIO pins, ADC channels, PWM channels, and communication interfaces encompassing I2C, SPI, and UART, the team prioritized ensuring seamless compatibility with the project's intricate needs.

Subsequently, the team engaged in an exhaustive research and evaluation phase, meticulously scrutinizing three potential microcontroller options: PIC18LF26K22, PIC16F18124, and PIC16F18855. Leveraging a comprehensive array of resources including datasheets, product pages, application notes, code examples, and external references, each microcontroller underwent rigorous assessment. Key considerations such as production unit cost, supply voltage range, maximum current, architecture, available IC packages, and programming capabilities were meticulously weighed.

## Microcontroller Selection Table
***
### 1. Project Specific Requirments and Datasheet Specifications

<table>
<thead>
<tr>
<th><strong>Design Considerations</strong></th>
<th><strong>Team Project Requirements</strong></th>
<th><strong>PIC Option 1</strong></th>
<th><strong>PIC Option 2</strong></th>
<th><strong>PIC Option 3</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><em>How many GPIO Pins?</em></td>
<td>6 (debug leds) minimum</td>
<td>28</td>
<td>2</td>
<td>24</td>
</tr>
<tr>
<td><em>Built-in Analog to Digital Converter? How many?</em></td>
<td>0 (shouldn’t need any for sensors picked)</td>
<td>0</td>
<td>1</td>
<td>24</td>
</tr>
<tr>
<td><em>Built-in Hardware PWM? How many?</em></td>
<td>Need at least 1</td>
<td>2</td>
<td>2</td>
<td>2</td>
</tr>
<tr>
<td><em>Built-in I2C? SPI? How many?</em></td>
<td>Need at least 2 I2C and 1 SPI</td>
<td>(2,2)</td>
<td>(2,2)</td>
<td>(2,2)</td>
</tr>
<tr>
<td><em>Built-in UART? How many?</em></td>
<td>Need at least 1 pin (ESP32)</td>
<td>2</td>
<td>1</td>
<td>2</td>
</tr>
<tr>
<td><em>Additional considerations specific to your project specifications (optional)</em></td>
<td>Since our project will be outside it must be able to operate from 0C-45C minimum</td>
<td>-40℃ to 85℃</td>
<td>-40℃ to 85℃</td>
<td>-40℃ to 85℃</td>
</tr>
</tbody>
</table>


***

### 2. Microcontroller Information and Part Details

<table>
<thead>
<tr>
<th><strong>Microcontroller Considerations</strong></th>
<th>Instructions</th>
<th><strong>PIC Option 1</strong></th>
<th><strong>PIC Option 2</strong></th>
<th><strong>PIC Option 3</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><em>Part Number</em></td>
<td>Entire Part Number</td>
<td>PIC18F25J11</td>
<td>PIC18F46Q24</td>
<td>PIC18F26K40</td>
</tr>
<tr>
<td><em>Link (URL) to Product Page</em></td>
<td>Clean Links</td>
<td><a href="https://www.microchip.com/en-us/product/PIC18F25J11">Link</a></td>
<td><a href="https://www.microchip.com/en-us/product/PIC18F46Q24#document-table">Link</a></td>
<td><a href="https://www.microchip.com/en-us/product/pic18f26k40">Link</a></td>
</tr>
<tr>
<td><em>Link (URL) to Data Sheets</em></td>
<td></td>
<td><a href="https://ww1.microchip.com/downloads/aemDocuments/documents/OTH/ProductDocuments/DataSheets/39932D.pdfl">Link</a></td>
<td><a href="https://ww1.microchip.com/downloads/aemDocuments/documents/MCU08/ProductDocuments/DataSheets/PIC18F26-45-46-55-56Q24-Microcontroller-Data-Sheet-XLP-DS40002503.pdf">Link</a></td>
<td><a href="https://ww1.microchip.com/downloads/en/DeviceDoc/PIC18LF26-45-46K40-Data-Sheet-DS40001816F.pdf">Link</a></td>
</tr>
<tr>
<td><em>Link (URL) to Application Notes</em></td>
<td></td>
<td><a href="https://www.microchip.com/en-us/application-notes/an1267.html">Link</a></td>
<td><a href="https://www.microchip.com/en-us/application-notes/tb2669">Link</a></td>
<td><a href="https://ww1.microchip.com/downloads/aemDocuments/documents/MCU08/ApplicationNotes/ApplicationNotes/TB3261-Technical-Brief-DS90003261A.pdf">Link</a></td>
</tr>
<tr>
<td><em>Link (URL) to Code Examples</em></td>
<td></td>
<td><a href="https://ww1.microchip.com/downloads/en/DeviceDoc/30009687F.pdf">Link</a></td>
<td>N/A</td>
<td>N/A</td>
</tr>
<tr>
<td><em>Production Unit Cost</em></td>
<td>Find in the Microchip online store, or Digikey</td>
<td>$3.49</td>
<td>$2.16</td>
<td>$1.88</td>
</tr>
<tr>
<td><em>Supply Voltage Range</em></td>
<td>Find in the Microcontroller Datasheet</td>
<td>2.0V to 3.6V</td>
<td>1.8V to 5.5V</td>
<td>1.8V to 5.5V</td>
</tr>
<tr>
<td><em>Absolute Maximum Current for Entire IC</em></td>
<td>Find in the Microcontroller Datasheet</td>
<td>300mA</td>
<td>300mA</td>
<td>350mA</td>
</tr>
<tr>
<td><em>Maximum GPIO Pin Current</em></td>
<td>Find in the Microcontroller Datasheet</td>
<td>25mA</td>
<td>25mA</td>
<td>50mA</td>
</tr>
<tr>
<td><em>8-bit or 16-bit Architecture</em></td>
<td>Find in the Microcontroller Datasheet</td>
<td>8-bit</td>
<td>8-bit</td>
<td>8-bit</td>
</tr>
<tr>
<td><em>Available IC Packages/Footprints</em></td>
<td>Find in the microcontroller datasheet. Choose a microcontroller with both surface mount and DIP/through-hole packages available. See Most Common Mistakes below for requirements to improve manufacturing reliability.</td>
<td>SOIC (SM)</td>
<td>SOIC (SM)</td>
<td>SOIC (SM)</td>
</tr>
<tr>
<td><em>Supports External Interupts?</em></td>
<td>Find in the Microcontroller Datasheet</td>
<td>4</td>
<td>3</td>
<td>3</td>
</tr>
<tr>
<td><em>In-System Programming Capability and Type</em></td>
<td>Allows for programming the microcontroller without removing it from the PCB. Find in the microcontroller datasheet.</td>
<td>ICSP</td>
<td>PDID</td>
<td>ICSP</td>
</tr>
<tr>
<td><em>Programming Hardware, Cost, and URL</em></td>
<td>Find on the Microcontroller Product Page</td>
<td><a href="https://www.microchip.com/en-us/development-tool/PG164100">SnapDebug</a></td>
<td><a href="https://www.microchip.com/en-us/development-tool/PG164100">SnapDebug</a></td>
<td><a href="https://www.microchip.com/en-us/development-tool/PG164100">SnapDebug</a></td>
</tr>
<tr>
<td><em>Works with MPLAB® X Integrated Development Environment (IDE)?</em></td>
<td>Required</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
</tr>
<tr>
<td><em>Works with Microchip Code Configurator?</em></td>
<td>Required</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
</tr>
</tbody>
</table>


***

### 3. Overall Pros, Cons, and Rankings for chosen Microcontrollers 

<table>
<thead>
<tr>
<th><strong>Overall Pros, Cons, and Rankings</strong></th>
<th><strong>Two for Each</strong></th>
<th><strong>PIC Option 1</strong></th>
<th><strong>PIC Option 2</strong></th>
<th><strong>PIC Option 3</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><em>Overall Pros</em></td>
<td>Two Each</td>
<td>1. Has both I2C and SPI pins so we can use both at the same time. 2. In depth Datasheet.</td>
<td>1. Meets all requirements with redundancy on necessary features. 2. Cost-effective</td>
<td>1. Has an ample amount of I/O pins 2. Enhanced core features with multiple PWM and EUSART modules for serial communication. 3. Used in Previous Assignments.</td>
</tr>
<tr>
<td><em>Overall Cons</em></td>
<td>Two Each</td>
<td>1. No External ADC. 2. Few/Limited code examples</td>
<td>1. No External ADC. 2. Only one extra EUSART Port.</td>
<td>1. Limited GPIO ports. 2. Less pins equates to fewer functions and features.</td>
</tr>
<tr>
<td><em>Rankings</em></td>
<td>First Choice = 1, Second Choice = 2, Third Choice = 3</td>
<td>2</td>
<td>3</td>
<td>1</td>
</tr>
</tbody>
</table>


***

### 4. Final Microcontroller Choice and Rationale

**Choice:** Option 1

**Rationale:**
The selection of the PIC18F26K40 was guided by its rich array of features, comprehensive documentation, and the esteemed reputation of its microcontroller family. This choice embodies a strategic decision aimed at optimizing project success.

The PIC18F26K40 offers a wide range of options, providing flexibility to accommodate diverse project requirements. Its extensive documentation further facilitates smooth integration and development, ensuring clarity and efficiency throughout the process. Moreover, the well-established quality associated with the PIC18F series instills confidence in its reliability and performance.

Ease of soldering also factored into the decision, ensuring practicality and convenience during assembly and manufacturing processes.

While challenges may arise in the future, the PIC18F26K40 stands as the most promising choice for achieving success within the group's current scope. Its robust features, ample documentation, and ease of soldering collectively position it as the optimal solution for driving the project forward with confidence and efficiency.

[Back to Home Page](/team207-s2024)

[Back to Report](report)
