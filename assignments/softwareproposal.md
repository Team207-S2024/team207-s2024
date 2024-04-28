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
  <i>Figure 10: MQTT Table </i>
</p>

# MPLAB X Configuration

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/5da7fe75-e401-4377-a6f4-220474c0e20b" />
</p>

<p align="center">
  <i>Figure 11: System Settings for MCC </i>
</p>

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/4d06d608-f4f9-4bfc-89ae-6b129bbb8b39" />
</p>

<p align="center">
  <i>Figure 12: Picture of Pins on Graph for PIC in MCC </i>
</p>

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/f7282b13-6493-41d9-beb5-88d838ed8063" />
</p>

<p align="center">
  <i>Figure 13: Picture of Pins for PIC in MCC </i>
</p>

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/08b0263f-d6d2-4672-a8b6-afa1fa78003e" />
</p>

<p align="center">
  <i>Figure 14: Picture of Pins on Grid for PIC in MCC </i>
</p>

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/aca0f4d6-d883-494f-a213-4064588934c3" />
</p>

<p align="center">
  <i>Figure 15: Interrupts in MCC </i>
</p>

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/69f54009-33a9-48fd-a65c-d566dcc1afc5" />
</p>

<p align="center">
  <i>Figure 16: EUSART Settings in MCC </i>
</p>

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/e7bc4c90-0e8b-411e-9945-614f5dfe43c2" />
</p>

<p align="center">
  <i>Figure 17: I2C Settings in MCC </i>
</p>

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/b53a5da4-31ff-47c0-abd2-1998361a4a23" />
</p>

<p align="center">
  <i>Figure 18: SPI Settings in MCC </i>
</p>

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/6328085a-ed9f-4e0a-b35d-cdbf0d9927b0" />
</p>

<p align="center">
  <i>Figure 19: Timer Settings in MCC </i>
</p>


# Code

```
/**
  Generated Main Source File

  Company:
    Microchip Technology Inc.

  File Name:
    main.c

  Summary:
    This is the main file generated using PIC10 / PIC12 / PIC16 / PIC18 MCUs

  Description:
    This header file provides implementations for driver APIs for all modules selected in the GUI.
    Generation Information :
        Product Revision  :  PIC10 / PIC12 / PIC16 / PIC18 MCUs - 1.81.8
        Device            :  PIC18LF26K40
        Driver Version    :  2.00
*/

/*
    (c) 2018 Microchip Technology Inc. and its subsidiaries. 
    
    Subject to your compliance with these terms, you may use Microchip software and any 
    derivatives exclusively with Microchip products. It is your responsibility to comply with third party 
    license terms applicable to your use of third party software (including open source software) that 
    may accompany Microchip software.
    
    THIS SOFTWARE IS SUPPLIED BY MICROCHIP "AS IS". NO WARRANTIES, WHETHER 
    EXPRESS, IMPLIED OR STATUTORY, APPLY TO THIS SOFTWARE, INCLUDING ANY 
    IMPLIED WARRANTIES OF NON-INFRINGEMENT, MERCHANTABILITY, AND FITNESS 
    FOR A PARTICULAR PURPOSE.
    
    IN NO EVENT WILL MICROCHIP BE LIABLE FOR ANY INDIRECT, SPECIAL, PUNITIVE, 
    INCIDENTAL OR CONSEQUENTIAL LOSS, DAMAGE, COST OR EXPENSE OF ANY KIND 
    WHATSOEVER RELATED TO THE SOFTWARE, HOWEVER CAUSED, EVEN IF MICROCHIP 
    HAS BEEN ADVISED OF THE POSSIBILITY OR THE DAMAGES ARE FORESEEABLE. TO 
    THE FULLEST EXTENT ALLOWED BY LAW, MICROCHIP'S TOTAL LIABILITY ON ALL 
    CLAIMS IN ANY WAY RELATED TO THIS SOFTWARE WILL NOT EXCEED THE AMOUNT 
    OF FEES, IF ANY, THAT YOU HAVE PAID DIRECTLY TO MICROCHIP FOR THIS 
    SOFTWARE.
*/
#include "mcc_generated_files/mcc.h"
#include "mcc_generated_files/examples/i2c2_master_example.h"
#include "mcc_generated_files/i2c2_master.h" 

#define I2C_SLAVE_ADDR              0b1001100
#define READ_HUM_ADDR               0x27
#define READ_TEMP_ADDR              0x00
#define DIAG_HUM_ADDR               0x07

//void ISR_ManualTurnOff(){
//    char manual;
//    uint8_t motorData;
//    uint8_t stp = 0b11101100;
//    EUSART1_Receive_ISR();
//    
//    if (EUSART1_is_rx_ready()){
//        manual = EUSART1_Read();
//    }
//    if (manual == '0'){
//        // Turn off debugging LED 
//        LEDG1_SetHigh();
//
//        // Turn off debugging LED 
//        LEDR1_SetLow();
//        
//        // Stop the Motor
//        CSN_SetLow();
//        motorData = SPI1_ExchangeByte(stp);
//        CSN_SetHigh();
//    }
//}

void main(void)
{
    // Initialize the device
    SYSTEM_Initialize();
    EUSART1_Initialize();
    I2C2_Initialize();
    SPI1_Initialize();
    //EUSART1_SetRxInterruptHandler(ISR_ManualTurnOff);
    // If using interrupts in PIC18 High/Low Priority Mode you need to enable the Global High and Low Interrupts
    // If using interrupts in PIC Mid-Range Compatibility Mode you need to enable the Global and Peripheral Interrupts
    // Use the following macros to:

    // Enable the Global Interrupts
    INTERRUPT_GlobalInterruptEnable();

    // Disable the Global Interrupts
    //INTERRUPT_GlobalInterruptDisable();

    // Enable the Peripheral Interrupts
    INTERRUPT_PeripheralInterruptEnable();

    // Disable the Peripheral Interrupts
    //INTERRUPT_PeripheralInterruptDisable();
    SPI1_Open(SPI1_DEFAULT);
    
    // Define Serial Data
    uint8_t tempData = 0;
    uint8_t tempDataF = 0;
    uint8_t humData = 0;
    uint8_t motorData = 0;
    
    // Define Checker Data
    uint8_t home = 0;
    uint8_t alert = 0;
    // uint16_t humReadable = 0;
    
    // Define Motor Commands
    uint8_t fwd = 0b11101110;
    uint8_t bwd = 0b11101111;
    uint8_t stp = 0b11101100;
    
    // Define Manual input
    char manual;
    uint8_t man = 3;
    
    while (1){
//        LEDR1_SetLow();
        // Temperature Sensor Read
        tempData = I2C2_Read1ByteRegister(I2C_SLAVE_ADDR, READ_TEMP_ADDR); 
        
        // Temperature Conversion
        tempDataF = (tempData* (9/5)) + 32;
        
        // Humidity Sensor Read
//        __delay_ms(3);
//        I2C2_Write1ByteRegister(READ_HUM_ADDR,0x80,0x0000);
//        __delay_ms(50);
//        humData = I2C2_Read1ByteRegister(I2C_SLAVE_ADDR, READ_HUM_ADDR);
//        __delay_ms(50);
        // humReadable = (humData[0] << 8 | humData[1]);
        // float humPer = (humReadable/16382.0) * 100.0;
        
        // If tempData is greater than 27 C:
        if (tempData >= 27){
            // If the plant isn't at home:
            if (home == 0){
                // Turn on debugging LED (Moving)
                LEDR1_SetHigh();
                
                // Move Motor for 4.55 seconds
                CSN_SetLow();
                motorData = SPI1_ExchangeByte(fwd);
                CSN_SetHigh();
                __delay_ms(3000);
                __delay_ms(100);
                CSN_SetLow();
                motorData = SPI1_ExchangeByte(stp);
                CSN_SetHigh();
                
                // Tell MQTT it's at home
                home = 1;
                
                // Turn on debugging LED (At Home)
                LEDG1_SetHigh();
                
                // Turn off debugging LED (Not Moving)
                LEDR1_SetLow();
                
                __delay_ms(3000);
            }
            else{
                // Nothing
            }
        }
        // If tempData is less than 27 C:        
        if (tempData < 27){
            // If the plant is at home:
            if (home == 1){
                // Turn on debugging LED (Moving)
                LEDR1_SetHigh();
                
                // Move Motor Backward for 4.55 seconds
                CSN_SetLow();
                motorData = SPI1_ExchangeByte(bwd);
                CSN_SetHigh();
                __delay_ms(3000);
                CSN_SetLow();
                motorData = SPI1_ExchangeByte(stp);
                CSN_SetHigh();
                
                // Tell MQTT it's not at home
                home = 0;  
                
                // Turn off debugging LED (Not Home)
                LEDG1_SetLow();
                
                // Turn off debugging LED (Not Moving)
                LEDR1_SetLow();
                        
                __delay_ms(3000);
            }
            else{
                // Nothing
            }
        }
//        if (humData <= 1000){
//            alert = 1;
//        }
//        else{
//            alert = 0;
//        }
        // Print Data: 
        
        printf("-Temp: %u C, %u F\n\r", tempData, tempDataF);
        __delay_ms(100);
        printf("*Humidity: %u\n\r", humData);
        __delay_ms(100);
        printf("+Alert: %u\n\r", alert);
        __delay_ms(100);
        printf("!Home: %u\n\r", home);
        __delay_ms(100);
        
        // Manual: Reads either an h or o and moves motor accordingly assuming it can
        // Read from MQTT -> ESP32 -> PIC
        if (EUSART1_is_rx_ready()){
            manual = EUSART1_Read();
        }
        
        // Check manual input
        if (manual == 'h'){
           man = 1;
        }
        if (manual == 'o') {
           man = 0;
        }
        
        // Check if man is going on
        if (man == 1){
            // Check if plant is not at home
            if (home == 0){
                // Turn on debugging LED (Moving)
                LEDR1_SetHigh();
                
                // Move Motor for 4.55 seconds
                CSN_SetLow();
                motorData = SPI1_ExchangeByte(fwd);
                CSN_SetHigh();
                __delay_ms(3000);
                __delay_ms(100);
                CSN_SetLow();
                motorData = SPI1_ExchangeByte(stp);
                CSN_SetHigh();
                
                // Tell MQTT it's at home
                home = 1;
                
                // Turn on debugging LED (At Home)
                LEDG1_SetHigh();
                
                // Turn off debugging LED (Not Moving)
                LEDR1_SetLow();
                
                __delay_ms(3000);
                man = 3;
            }
            else{
                // Nothing
                man = 3;
            }
        }
        
        // If man is going out
        if (man == 0){
            // If the plant is at home:
            if (home == 1){
                // Turn on debugging LED (Moving)
                LEDR1_SetHigh();
                
                // Move Motor Backward for 4.55 seconds
                CSN_SetLow();
                motorData = SPI1_ExchangeByte(bwd);
                CSN_SetHigh();
                __delay_ms(3000);
                CSN_SetLow();
                motorData = SPI1_ExchangeByte(stp);
                CSN_SetHigh();
                
                // Tell MQTT it's not at home
                home = 0;  
                
                // Turn off debugging LED (Not Home)
                LEDG1_SetLow();
                
                // Turn off debugging LED (Not Moving)
                LEDR1_SetLow();
                        
                __delay_ms(3000);
                man = 3;
            }
            else{
                // Nothing
                man = 3;
            }
        }
    }
}

/**
 End of File
*/
```
[Back to Home Page](/team207-s2024)

[Back to Report](report)
