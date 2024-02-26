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

# Component Selection

## Power Supply

### Battery

<p align="center"> Table 1a: Battery Component Selection 1 </p>

<table>
  <tr>
    <th><b>Solution</b></th>
    <th><b>Pros</b></th>
    <th><b>Cons</b></th>
  </tr>
  <tr>
    <td> 
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/7ad08af1-8cb1-4037-a20c-35aa7d08064c" />
    Name: EN22
	<p>
	Price: $2.61
	<p>
	Link: https://www.digikey.com/en/products/detail/energizer-battery-company/EN22/704825
    </td>
    <td>
    <li>Common brand(?)
	<li>In heavy stock
	<li>Good shelf life 
    </td>
    <td>
    <li>Not used before
	</td>
  </tr>
</table>

<p align="center">  Table 1b: Battery Component Selection 2 </p>

<table>
  <tr>
   <th>Solution
   </th>
   <th>Pros
   </th>
   <th>Cons
   </th>
  </tr>
  <tr>
   <td>

![b2](https://github.com/Team207-S2024/team207-s2024/assets/156377035/1b56bf59-16bc-44e0-964f-426e8c069229)

<p>
Name: 6LF22XWA/B
<p>
Price: $2.34
<p>
Link: https://www.digikey.com/en/products/detail/panasonic-bsg/6LF22XWA-B/5067196
   </td>
   <td>
<ul>

<li>Used before in EGR304

<li>Can be put into series

<li>Fairly cheap

<li>In stock
</li>
</ul>
   </td>
   <td>
<ul>

<li>Had a few issues using it previously

<li>May not be enough/be too much voltage

<li>Not a great datasheet

<li>Not rechargeable
</li>
</ul>
   </td>
  </tr>
</table>

<p align="center"> Table 1c: Battery Component Selection 3 </p>

<table>
  <tr>
   <th>Solution
   </th>
   <th>Pros
   </th>
   <th>Cons
   </th>
  </tr>
  <tr>
   <td>
     
![b3](https://github.com/Team207-S2024/team207-s2024/assets/156377035/fa049aea-b20a-460f-ad2b-1b5b661dc1d0)

<p>
Name: A23BPZ
<p>
Price: $2.26
<p>
Link: https://www.digikey.com/en/products/detail/energizer-battery-company/A23BPZ/5431480
   </td>
   <td>
<ul>

<li>Has a discharge rate (500uA)

<li>In depth datasheet

<li>12 V vs 9, won’t need to make a battery pack in series potentially if we only need 12 volt
</li>
</ul>
   </td>
   <td>
<ul>

<li>Probably isn’t efficient

<li>Not used this kind of battery in a system like this before
</li>
</ul>
   </td>
  </tr>
</table>


<p align="center"> Table 1d: Battery Component Selection 4 </p>


<table>
  <tr>
   <th>Solution
   </th>
   <th>Pros
   </th>
   <th>Cons
   </th>
  </tr>
  <tr>
   <td>

![b4](https://github.com/Team207-S2024/team207-s2024/assets/156377035/902b9b2e-6fac-4c15-890b-417b1c524b63)

<p>
Name: Amazon Basics 4-Pack 9 Volt Alkaline Performance All-Purpose Batteries, 5-Year Shelf Life, Packaging May Vary
<p>
Price: $9.58
<p>
Link: https://www.amazon.com/Amazon-Basics-Performance-All-Purpose-Batteries/dp/B0774D64LT
   </td>
   <td>
<ul>

<li>Has a very good discharge rate (1.2A/h)

<li>Cheap (4 for 10)
</li>
</ul>
   </td>
   <td>
<ul>

<li>Have to buy from Amazon

<li>Unsure of quality
</li>
</ul>
   </td>
  </tr>
</table>


<p align="center"> Choice: 1d- Amazon Basics 4-Pack 9 Volt Alkaline Performance All-Purpose Batteries </p>

Rationale: We chose this because the 1.2 A/hr seemed like the best choice versus the others. It provides the necessary amperage for every part, and will last longer than the competition. If we chose a 500 mA/hr battery, it would get drained very quickly due to the motor’s current draw. 


### Switching Voltage Regulator

<p align="center"> Table 2a: Voltage Regulator Component Selection 1 </p>

<table>
  <tr>
   <th>Solution
   </th>
   <th>Pros
   </th>
   <th>Cons
   </th>
  </tr>
  <tr>
   <td>

![r1](https://github.com/Team207-S2024/team207-s2024/assets/156377035/29c06b99-2c73-4fdf-8ed8-b8d8295385c9)

<p>
Name: LM2575D2T-3.3R4G
<p>
Price: $2.39/ea
<p>
Link: https://www.digikey.com/en/products/detail/onsemi/LM2575D2T-3-3R4G/1476688
   </td>
   <td>
<ul>

<li>Used in class (Through hole)

<li>Relatively cheap

<li>Good max input V

<li>In stock
</li>
</ul>
   </td>
   <td>
<ul>

<li>Surface mount not used in class

<li>Might be hard to apply
</li>
</ul>
   </td>
  </tr>
</table>


<p align="center">  Table 2b: Voltage Regulator Component Selection 2 </p>


<table>
  <tr>
   <th>Solution
   </th>
   <th>Pros
   </th>
   <th>Cons
   </th>
  </tr>
  <tr>
   <td>
     
![r2](https://github.com/Team207-S2024/team207-s2024/assets/156377035/329a5b38-57bb-4cfb-8d81-943d562c46ea)

<p>
Name: TLVM13620RDHR
<p>
Price: $4.42/ea
<p>
Link: https://www.digikey.com/en/products/detail/texas-instruments/TLVM13620RDHR/16585658
   </td>
   <td>
<ul>

<li>Newer than other regulators

<li>Has a lot of different options

<li>Higher current
</li>
</ul>
   </td>
   <td>
<ul>

<li>Unused to the actual component itself (never had experience with this kind of surface mount)

<li>Somewhat confusing as to how to regulate to 3.3 V
</li>
</ul>
   </td>
  </tr>
</table>


<p align="center">  Table 2c: Voltage Regulator Component Selection 3 </p>


<table>
  <tr>
   <th>Solution
   </th>
   <th>Pros
   </th>
   <th>Cons
   </th>
  </tr>
  <tr>
   <td>

![r3](https://github.com/Team207-S2024/team207-s2024/assets/156377035/1686e49e-bf2b-4305-b163-cb8caf663232)

<p>
Name: TPS560430X3FDBVR
<p>
Price: $1.07/ea
<p>
Link: https://www.digikey.com/en/products/detail/texas-instruments/TPS560430X3FDBVR/9094603
   </td>
   <td>
<ul>

<li>Less current running through the regulator, may be good?

<li>Lots of stock
</li>
</ul>
   </td>
   <td>
<ul>

<li>Seems fairly small

<li>Not used in class
</li>
</ul>
   </td>
  </tr>
</table>


<p align="center">  Choice: LM2575D2T-3.3R4G </p>

Rationale: The class used the through hole version of this component for a prior ICC, so it would be beneficial to be able to use that knowledge going forward as much as possible. Although it wasn’t the surface mount version, it stands to reason the same circuit should theoretically work.


## Motor Subsystem Components


### Motor Driver 

<p align="center">  Table 3a: Motor Driver Component Selection 1 </p>


<table>
  <tr>
   <th>Solution
   </th>
   <th>Pros
   </th>
   <th>Cons
   </th>
  </tr>
  <tr>
   <td>

   ![md1](https://github.com/Team207-S2024/team207-s2024/assets/156377035/fa2f181d-d769-4e24-b150-2b5fae608ecd)


<p>
Name:IFX9201SGAUMA1
<p>
Price:$4.00000
<p>
Link:https://www.digikey.com/en/products/detail/infineon-technologies/IFX9201SGAUMA1/5415542
   </td>
   <td>
<ul>

<li>Will gain experience using this motor driver in class

<li>The teaching team has more experience with this motor driver

<li>Cheaper alternative
</li>
</ul>
   </td>
   <td>
<ul>

<li>Only utilizes SPI communication

<li>More expensive than other motor drivers

<li>
</li>
</ul>
   </td>
  </tr>
</table>


<p align="center">  Table 3b: Motor Driver Component Selection 2 </p>


<table>
  <tr>
   <th>Solution
   </th>
   <th>Pros
   </th>
   <th>Cons
   </th>
  </tr>
  <tr>
   <td>

![md2](https://github.com/Team207-S2024/team207-s2024/assets/156377035/6fb70a7a-9a56-4a44-aa95-f2dc19603632)

<p>
Name:IRMCF311TY
<p>
Price:$4.82000
<p>
Link:https://www.digikey.com/en/products/detail/rochester-electronics-llc/IRMCF311TY/12597383
   </td>
   <td>
<ul>

<li>Less Expensive

<li>
</li>
</ul>
   </td>
   <td>
<ul>

<li>Has more pins to solder will be a bit difficult

<li>Less Experience with the IC
</li>
</ul>
   </td>
  </tr>
</table>


<p align="center">  Table 3c: Motor Driver Component Selection 3 </p>


<table>
  <tr>
   <th>Solution
   </th>
   <th>Pros
   </th>
   <th>Cons
   </th>
  </tr>
  <tr>
   <td>
     
![md3](https://github.com/Team207-S2024/team207-s2024/assets/156377035/6d564754-70a0-4d86-9743-f5b8525a2bc1)

<p>
Name:IRMCF312TR
<p>
Price:$8.88000
<p>
Link:https://www.digikey.com/en/products/detail/infineon-technologies/IRMCF312TR/1982944
   </td>
   <td>
<ul>

<li>Has a variety of interfaces for customizable settings
</li>
</ul>
   </td>
   <td>
<ul>

<li>Less Experience with the IC

<li>Will be more difficult to solder
</li>
</ul>
   </td>
  </tr>
</table>


<p align="center"> Choice: IFX9201SGAUMA1 </p>

Rationale: This motor driver was provided for us in class and would provide less of a learning curve, in terms of operation and coding itself. The IC itself would take less time to solder because there are less pins on the layout. 


### Motor

<p align="center"> Table 4a: Motor Component Selection 1 </p>


<table>
  <tr>
   <th>Solution
   </th>
   <th>Pros
   </th>
   <th>Cons
   </th>
  </tr>
  <tr>
   <td>
     
![m1](https://github.com/Team207-S2024/team207-s2024/assets/156377035/ce98df8e-5be8-418e-9900-d1be90d2d710)


<p>
Name:95010
<p>
Price: 	
<p>
Link: <a href="https://www.digikey.com/en/products/detail/kitronik-ltd/2546/8635440">https://www.digikey.com/en/products/detail/kitronik-ltd/2546/8635440</a>
   </td>
   <td>
<ul>

<li>Small compact size for versatility 

<li>Within  the range operating voltage

<li>The shaft offers a variety for different pieces to be added. 
</li>
</ul>
   </td>
   <td>
<ul>

<li>The RPM does exceed the desired output by a small margin
</li>
</ul>
   </td>
  </tr>
</table>


<p align="center"> Table 4b: Motor Component Selection 2 </p>


<table>
  <tr>
   <th>Solution
   </th>
   <th>Pros
   </th>
   <th>Cons
   </th>
  </tr>
  <tr>
   <td>
     
![m2](https://github.com/Team207-S2024/team207-s2024/assets/156377035/dcf3a048-7de8-4bd3-bbe5-8329fb8fb685)

<p>
Name:80047
<p>
Price:
<p>
Link:<a href="https://www.digikey.com/en/products/detail/makeblock-co-ltd/80047/9917308">https://www.digikey.com/en/products/detail/makeblock-co-ltd/80047/9917308</a>
   </td>
   <td>
<ul>

<li>Highest value of torque which would be useful for our specific application

<li>Optimal Power consumption for battery
</li>
</ul>
   </td>
   <td>
<ul>

<li>The Availability of the unit itself

<li>The data sheet is not the most reliable
</li>
</ul>
   </td>
  </tr>
</table>


<p align="center"> Table 4c: Motor Component Selection 3 </p>


<table>
  <tr>
   <th>Solution
   </th>
   <th>Pros
   </th>
   <th>Cons
   </th>
  </tr>
  <tr>
   <td>
     
![m3](https://github.com/Team207-S2024/team207-s2024/assets/156377035/e1683a3e-649c-42b6-8b43-5e6d825b0402)

<p>
Name:114090046
<p>
Price:$5.20000
<p>
Link:https://protosupplies.com/product/dc-geared-motor-and-wheel-kit-3-9v-77rpm/
   </td>
   <td>
<ul>

<li>Less expensive model

<li>Smaller and compact for versatility

<li>Correct operating voltage
</li>
</ul>
   </td>
   <td>
<ul>

<li>Data sheet is not to detailed

<li>Less torque
</li>
</ul>
   </td>
  </tr>
</table>


<p align="center">  Choice: 114090046 </p>

Rationale: This motor provided all the optimal specs for our specific application and was reasonably priced compared to all the other motors that were available. The compact shape also would help with mechanical design of the project. This Motor also offers a higher torque value compared to all the other DC motors and is great for pulling heavy loads, which is required for our application.


## Humidity System Components


### Humidity

<p align="center">  Table 5a: Humidity Sensor Component Selection 1 </p>


<table>
  <tr>
   <th>Solution
   </th>
   <th>Pros
   </th>
   <th>Cons
   </th>
  </tr>
  <tr>
   <td>
   
![h1](https://github.com/Team207-S2024/team207-s2024/assets/156377035/a7342114-bf14-4f61-8147-91a580e589a3)

<p>
Name: Honeywell Sensing and Productivity Solutions HIH6030-021-001
<p>
Price:$13.43
<p>
Link: <a href="https://www.digikey.com/en/products/detail/honeywell-sensing-and-productivity-solutions/HIH6030-021-001/4291625">here</a>
   </td>
   <td>
<ul>

<li>Hybrid SPI and I2C communication types

<li>Good accuracy

<li>Outward surface mount pins

<li>Low power consumption

<li>Easy application circuit
</li>
</ul>
   </td>
   <td>
<ul>

<li>Somewhat Small Size

<li>High Price Point
</li>
</ul>
   </td>
  </tr>
</table>


<p align="center">  Table 5b: Humidity Sensor Component Selection 2 </p>


<table>
  <tr>
   <th>Solution
   </th>
   <th>Pros
   </th>
   <th>Cons
   </th>
  </tr>
  <tr>
   <td>
     
![h2](https://github.com/Team207-S2024/team207-s2024/assets/156377035/274d9813-0ebb-46a9-8484-f0171b79a834)


<p>
Name: STMicroelectronics HTS221TR
<p>
Price:$5.36
<p>
Link:<a href="https://www.digikey.com/en/products/detail/stmicroelectronics/HTS221TR/5180551">here</a>
   </td>
   <td>
<ul>

<li>Low Noise and High Resolution

<li>Hybrid SPI and I2C
</li>
</ul>
   </td>
   <td>
<ul>

<li>Small size

<li>Strange pin layout
</li>
</ul>
   </td>
  </tr>
</table>


<p align="center"> Table 5c: Humidity Sensor Component Selection 3 </p>


<table>
  <tr>
   <th>Solution
   </th>
   <th>Pros
   </th>
   <th>Cons
   </th>
  </tr>
  <tr>
   <td>

![h3](https://github.com/Team207-S2024/team207-s2024/assets/156377035/b7ea10e3-afd7-4817-b204-d1b6bb69c9e9)

<p>
Name:Bosch Sensortec BME280
<p>
Price:$6.42
<p>
Link:<a href="https://www.digikey.com/en/products/detail/bosch-sensortec/BME280/6136306">here</a>
   </td>
   <td>
<ul>

<li>Hybrid IC and SPI

<li>3 in 1 pressure, temp and humid sensor

<li>Fast response time

<li>Good price

<li>Low power consumption

<li>
</li>
</ul>
   </td>
   <td>
<ul>

<li>Small size

<li>
</li>
</ul>
   </td>
  </tr>
</table>



## Temperature System Components


### Temperature Sensor

<p align="center"> Table 6a: Temperature Sensor Component Selection 1 </p>


<table>
  <tr>
   <th>Solution
   </th>
   <th>Pros
   </th>
   <th>Cons
   </th>
  </tr>
  <tr>
   <td>

  ![t1](https://github.com/Team207-S2024/team207-s2024/assets/156377035/d49d95eb-7639-4d37-84a0-a159211c539b)
 

<p>
Name: MCP9700T-E/TT
<p>
Price: $0.30
<p>
Link: <a href="https://www.digikey.com/en/products/detail/microchip-technology/MCP9700T-E-TT/1212510">https://www.digikey.com/en/products/detail/microchip-technology/MCP9700T-E-TT/1212510</a>
   </td>
   <td>
<ul>

<li>This device can connect to both I2C and SPI outputs.

<li>You can surface mount it.

<li>This device has a wide temperature measurement range of -40 celsius to 125 celsius at an extended temperature and -40 celsius to 150 celsius at the high temperature.

<li>This device is optimized to drive a large amount of capacitive loads.
</li>
</ul>
   </td>
   <td>
<ul>

<li>It’s too small.

<li>It has a low operating current at 6 meu.
</li>
</ul>
   </td>
  </tr>
</table>


<p align="center"> Table 6b: Temperature Sensor Component Selection 2 </p>


<table>
  <tr>
   <th>Solution
   </th>
   <th>Pros
   </th>
   <th>Cons
   </th>
  </tr>
  <tr>
   <td>

![t2](https://github.com/Team207-S2024/team207-s2024/assets/156377035/15031345-2c1c-4474-a92b-bda2e4949643)
   
<p>
Name: NCT75MNR2G
<p>
Price: $0.83
<p>
Link: <a href="https://www.digikey.com/en/products/detail/onsemi/NCT75MNR2G/2748391">https://www.digikey.com/en/products/detail/onsemi/NCT75MNR2G/2748391</a>
   </td>
   <td>
<ul>

<li>This device can connect to both I2C and SPI outputs.

<li>You can surface mount it.

<li>This device has a wide temperature measurement range of -55 celsius to 125 celsius.

<li>It has a “shutdown mode” when it has a low power consumption.

<li>This device has an “over temperature indicator”.
</li>
</ul>
   </td>
   <td>
<ul>

<li>It’s too small.

<li>It is a “one-shot” mode.

<li>This device has a small input voltage of 3.0 V to 5.5 V.
</li>
</ul>
   </td>
  </tr>
</table>


<p align="center">  Table 6c: Temperature Sensor Component Selection 3 </p>


<table>
  <tr>
   <th>Solution
   </th>
   <th>Pros
   </th>
   <th>Cons
   </th>
  </tr>
  <tr>
   <td>
     
![t3](https://github.com/Team207-S2024/team207-s2024/assets/156377035/b9a35b65-73f6-4229-b2ca-78624b025d78)

<p>
Name: LMT84DCKR
<p>
Price: $0.80
<p>
Link: <a href="https://www.digikey.com/en/products/detail/texas-instruments/LMT84DCKR/4090899">https://www.digikey.com/en/products/detail/texas-instruments/LMT84DCKR/4090899</a>
   </td>
   <td>
<ul>

<li>This device can connect to both I2C and SPI outputs.

<li>The outputs are short-circuited protected.

<li>You can surface mount it.

<li>The temperature is very accurate at a +/- of 0.4 celsius typical.

<li>It has a wide temperature range of -50 celsius to 150 celsius.
</li>
</ul>
   </td>
   <td>
<ul>

<li>It’s too small.

<li>It has a low voltage operation at 1.5.

<li>It has a low quiescent current at 5.4 meu.
</li>
</ul>
   </td>
  </tr>
</table>

