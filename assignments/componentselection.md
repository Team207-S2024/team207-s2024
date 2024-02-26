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
    <th style="width:25%">
	    <b>Solution</b>
    </th>
    <th style="width:35%">
	    <b>Pros</b>
    </th>
    <th style="width: 40%">
	    <b>Cons</b>
    </th>
  </tr>
  <tr>
    <td> 
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/7ad08af1-8cb1-4037-a20c-35aa7d08064c" /> <br>
	Name: EN22  <br>
	Price: $2.61  <br>
	Link: https://www.digikey.com/en/products/detail/energizer-battery-company/EN22/704825<br>
    </td>
    <td>
    		<li> Common brand(?) </li>
		<li> In heavy stock </li>
		<li> Good shelf life  </li>
    </td>
    <td>
    		<li> Not used before </li>
    </td>
  </tr>
</table>

<p align="center">  Table 1b: Battery Component Selection 2 </p>

<table>
  <tr>
    <th style="width:25%">
	    <b>Solution</b>
    </th>
    <th style="width:35%">
	    <b>Pros</b>
    </th>
    <th style="width: 40%">
	    <b>Cons</b>
    </th>
  </tr>
  <tr>
    <td> 
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/1b56bf59-16bc-44e0-964f-426e8c069229" /> <br>
	Name: 6LF22XWA/B  <br>
	Price: $2.34  <br>
	Link: https://www.digikey.com/en/products/detail/panasonic-bsg/6LF22XWA-B/5067196  <br>
    </td>
    <td>
		<li> Used before in EGR304 </li>
		<li> Can be put into series </li>
		<li> Fairly cheap </li>
		<li> In stock </li>
    </td>
    <td>
		<li> Had a few issues using it previously </li>
		<li> May not be enough/be too much voltage </li>
		<li> Not a great datasheet </li>
		<li> Not rechargeable </li>
    </td>
  </tr>
</table>

<p align="center"> Table 1c: Battery Component Selection 3 </p>

<table>
  <tr>
    <th style="width:25%">
	    <b>Solution</b>
    </th>
    <th style="width:35%">
	    <b>Pros</b>
    </th>
    <th style="width: 40%">
	    <b>Cons</b>
    </th>
  </tr>
  <tr>
    <td> 
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/fa049aea-b20a-460f-ad2b-1b5b661dc1d0" /> <br>
	Name: A23BPZ <br>
	Price: $2.26 <br>
	Link: https://www.digikey.com/en/products/detail/energizer-battery-company/A23BPZ/5431480 <br>
    </td>
    <td>
		<li> Has a discharge rate (500uA) </li>
		<li> In depth datasheet </li>
		<li> 12 V vs 9, won’t need to make a battery pack in series potentially if we only need 12 volt </li>
    </td>
    <td>
		<li> Probably isn’t efficient </li>
		<li> Not used this kind of battery in a system like this before </li>
    </td>
  </tr>
</table>

<p align="center"> Table 1d: Battery Component Selection 4 </p>

<table>
  <tr>
    <th style="width:25%">
	    <b>Solution</b>
    </th>
    <th style="width:35%">
	    <b>Pros</b>
    </th>
    <th style="width: 40%">
	    <b>Cons</b>
    </th>
  </tr>
  <tr>
    <td> 
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/902b9b2e-6fac-4c15-890b-417b1c524b63" /> <br>
	Name: Amazon Basics 4-Pack 9 Volt Alkaline Performance All-Purpose Batteries, 5-Year Shelf Life, Packaging May Vary <br>
	Price: $9.58 <br>
	Link: https://www.amazon.com/Amazon-Basics-Performance-All-Purpose-Batteries/dp/B0774D64LT <br>
    </td>
    <td>
		<li> Has a discharge rate (500uA) </li>
		<li> In depth datasheet </li>
    </td>
    <td>
		<li> Have to buy from Amazon </li>
		<li> Unsure of quality </li>
    </td>
  </tr>
</table>

<p align="center"> Choice: 1d- Amazon Basics 4-Pack 9 Volt Alkaline Performance All-Purpose Batteries </p>

Rationale: We chose this because the 1.2 A/hr seemed like the best choice versus the others. It provides the necessary amperage for every part, and will last longer than the competition. If we chose a 500 mA/hr battery, it would get drained very quickly due to the motor’s current draw. 

### Switching Voltage Regulator

<p align="center"> Table 2a: Voltage Regulator Component Selection 1 </p>

<table>
  <tr>
    <th style="width:25%">
	    <b>Solution</b>
    </th>
    <th style="width:35%">
	    <b>Pros</b>
    </th>
    <th style="width: 40%">
	    <b>Cons</b>
    </th>
  </tr>
  <tr>
    <td> 
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/29c06b99-2c73-4fdf-8ed8-b8d8295385c9" /> <br>
	Name: LM2575D2T-3.3R4G <br>
	Price: $2.39/ea <br>
	Link: https://www.digikey.com/en/products/detail/onsemi/LM2575D2T-3-3R4G/1476688 <br>
    </td>
    <td>
		<li> Used in class (Through hole) </li>
		<li> Relatively cheap </li>
		<li> Good max input V </li>
		<li> In stock </li>
    </td>
    <td>
		<li> Surface mount not used in class </li>
		<li> Might be hard to apply </li>
    </td>
  </tr>
</table>

<p align="center">  Table 2b: Voltage Regulator Component Selection 2 </p>

<table>
  <tr>
    <th style="width:25%">
	    <b>Solution</b>
    </th>
    <th style="width:35%">
	    <b>Pros</b>
    </th>
    <th style="width: 40%">
	    <b>Cons</b>
    </th>
  </tr>
  <tr>
    <td> 
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/329a5b38-57bb-4cfb-8d81-943d562c46ea" /> <br>
	Name: TLVM13620RDHR <br>
	Price: $4.42/ea <br>
	Link: https://www.digikey.com/en/products/detail/texas-instruments/TLVM13620RDHR/16585658 <br>
    </td>
    <td>
		<li> Newer than other regulators </li>
		<li> Has a lot of different options </li>
		<li> Higher current </li>
    </td>
    <td>
		<li> Unused to the actual component itself (never had experience with this kind of surface mount) </li>
		<li> Somewhat confusing as to how to regulate to 3.3 V </li>
    </td>
  </tr>
</table>

<p align="center">  Table 2c: Voltage Regulator Component Selection 3 </p>

<table>
  <tr>
    <th style="width:25%">
	    <b>Solution</b>
    </th>
    <th style="width:35%">
	    <b>Pros</b>
    </th>
    <th style="width: 40%">
	    <b>Cons</b>
    </th>
  </tr>
  <tr>
    <td> 
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/1686e49e-bf2b-4305-b163-cb8caf663232" /> <br>
	Name: TPS560430X3FDBVR <br>
	Price: $1.07/ea <br>
	Link: https://www.digikey.com/en/products/detail/texas-instruments/TPS560430X3FDBVR/9094603 <br>
    </td>
    <td>
		<li> Less current running through the regulator, may be good? </li>
		<li> Lots of stock </li>
    </td>
    <td>
		<li> Seems fairly small </li>
		<li> Not used in class </li>
    </td>
  </tr>
</table>

<p align="center">  Choice: LM2575D2T-3.3R4G </p>

Rationale: The class used the through-hole version of this component for a prior ICC, so it would be beneficial to be able to use that knowledge going forward as much as possible. Although it wasn’t the surface mount version, it stands to reason the same circuit should theoretically work.

## Motor Subsystem Components

### Motor Driver 

<p align="center">  Table 3a: Motor Driver Component Selection 1 </p>

<table>
  <tr>
    <th style="width:25%">
	    <b>Solution</b>
    </th>
    <th style="width:35%">
	    <b>Pros</b>
    </th>
    <th style="width: 40%">
	    <b>Cons</b>
    </th>
  </tr>
  <tr>
    <td> 
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/fa2f181d-d769-4e24-b150-2b5fae608ecd" /> <br>
	Name: IFX9201SGAUMA1 <br>
	Price: $4.00000 <br> 
	Link: https://www.digikey.com/en/products/detail/infineon-technologies/IFX9201SGAUMA1/5415542 <br>
    </td>
    <td>
		<li> Will gain experience using this motor driver in class </li>
		<li> The teaching team has more experience with this motor driver </li>
		<li> Cheaper alternative </li>
    </td>
    <td>
		<li> Only utilizes SPI communication </li>
		<li> More expensive than other motor drivers </li>
    </td>
  </tr>
</table>

<p align="center">  Table 3b: Motor Driver Component Selection 2 </p>

<table>
  <tr>
    <th style="width:25%">
	    <b>Solution</b>
    </th>
    <th style="width:35%">
	    <b>Pros</b>
    </th>
    <th style="width: 40%">
	    <b>Cons</b>
    </th>
  </tr>
  <tr>
    <td> 
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/6fb70a7a-9a56-4a44-aa95-f2dc19603632" /> <br>
	Name: IRMCF311TY <br>
	Price: $4.82000 <br>
	Link: https://www.digikey.com/en/products/detail/rochester-electronics-llc/IRMCF311TY/12597383 <br>
    </td>
    <td>
		<li> Less Expensive </li>
    </td>
    <td>
		<li> Has more pins to solder will be a bit difficult </li>
		<li> Less Experience with the IC </li>
    </td>
  </tr>
</table>

<p align="center">  Table 3c: Motor Driver Component Selection 3 </p>

<table>
  <tr>
    <th style="width:25%">
	    <b>Solution</b>
    </th>
    <th style="width:35%">
	    <b>Pros</b>
    </th>
    <th style="width: 40%">
	    <b>Cons</b>
    </th>
  </tr>
  <tr>
    <td> 
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/6fb70a7a-9a56-4a44-aa95-f2dc19603632" /> <br>
	Name: IRMCF312TR <br>
	Price: $8.88000 <br>
	Link: https://www.digikey.com/en/products/detail/infineon-technologies/IRMCF312TR/1982944 <br>
    </td>
    <td>
		<li> Has a variety of interfaces for customizable settings </li>
    </td>
    <td>
		<li> Less Experience with the IC </li>
		<li> Will be more difficult to solder </li>
    </td>
  </tr>
</table>

<p align="center"> Choice: IFX9201SGAUMA1 </p>

Rationale: This motor driver was provided for us in class and would provide less of a learning curve, in terms of operation and coding itself. The IC itself would take less time to solder because there are less pins on the layout. 

### Motor

<p align="center"> Table 4a: Motor Component Selection 1 </p>

<table>
  <tr>
    <th style="width:25%">
	    <b>Solution</b>
    </th>
    <th style="width:35%">
	    <b>Pros</b>
    </th>
    <th style="width: 40%">
	    <b>Cons</b>
    </th>
  </tr>
  <tr>
    <td> 
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/ce98df8e-5be8-418e-9900-d1be90d2d710" /> <br>
	Name: 95010 <br>
	Price: $1.79000	<br>
	Link: https://www.digikey.com/en/products/detail/kitronik-ltd/2546/8635440 <br>
    </td>
    <td>
		<li> Small compact size for versatility  </li>
		<li> Within  the range operating voltage </li>
		<li> The shaft offers a variety for different pieces to be added.  </li>
    </td>
    <td>
		<li> The RPM does exceed the desired output by a small margin </li>
    </td>
  </tr>
</table>

<p align="center"> Table 4b: Motor Component Selection 2 </p>

<table>
  <tr>
    <th style="width:25%">
	    <b>Solution</b>
    </th>
    <th style="width:35%">
	    <b>Pros</b>
    </th>
    <th style="width: 40%">
	    <b>Cons</b>
    </th>
  </tr>
  <tr>
    <td> 
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/dcf3a048-7de8-4bd3-bbe5-8329fb8fb685" /> <br>
	Name: 80047 <br>
	Price: Out of Stock <br>
	Link: https://www.digikey.com/en/products/detail/makeblock-co-ltd/80047/9917308 <br>
    </td>
    <td>
		<li> Highest value of torque which would be useful for our specific application </li>
		<li> Optimal Power consumption for battery </li>
    </td>
    <td>
		<li> The Availability of the unit itself </li>
		<li> The data sheet is not the most reliable </li>
    </td>
  </tr>
</table>

<p align="center"> Table 4c: Motor Component Selection 3 </p>

<table>
  <tr>
    <th style="width:25%">
	    <b>Solution</b>
    </th>
    <th style="width:35%">
	    <b>Pros</b>
    </th>
    <th style="width: 40%">
	    <b>Cons</b>
    </th>
  </tr>
  <tr>
    <td> 
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/e1683a3e-649c-42b6-8b43-5e6d825b0402" /> <br>
	Name: 114090046 <br>
	Price:$5.20000 <br>
	Link:https://protosupplies.com/product/dc-geared-motor-and-wheel-kit-3-9v-77rpm/ <br>
    </td>
    <td>
		<li> Less expensive model </li>
		<li> Smaller and compact for versatility </li>
		<li> Correct operating voltage </li>
    </td>
    <td>
		<li> Data sheet is not too detailed </li>
		<li> Less torque </li>
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
    <th style="width:25%">
	    <b>Solution</b>
    </th>
    <th style="width:35%">
	    <b>Pros</b>
    </th>
    <th style="width: 40%">
	    <b>Cons</b>
    </th>
  </tr>
  <tr>
    <td> 
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/a7342114-bf14-4f61-8147-91a580e589a3" /> <br>
	Name: Honeywell Sensing and Productivity Solutions HIH6030-021-001 <br>
	Price: $13.43 <br>
	Link: https://www.digikey.com/en/products/detail/honeywell-sensing-and-productivity-solutions/HIH6030-021-001/4291625 <br>
    </td>
    <td>
		<li> Hybrid SPI and I2C communication types </li>
		<li> Good accuracy </li>
		<li> Outward surface mount pins </li>
		<li> Low power consumption </li>
		<li> Easy application circuit </li>
    </td>
    <td>
		<li> Somewhat Small Size </li>
		<li> High Price Point </li>
    </td>
  </tr>
</table>

<p align="center">  Table 5b: Humidity Sensor Component Selection 2 </p>

<table>
  <tr>
    <th style="width:25%">
	    <b>Solution</b>
    </th>
    <th style="width:35%">
	    <b>Pros</b>
    </th>
    <th style="width: 40%">
	    <b>Cons</b>
    </th>
  </tr>
  <tr>
    <td> 
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/274d9813-0ebb-46a9-8484-f0171b79a834" /> <br>
	Name: STMicroelectronics HTS221TR <br>
	Price: $5.36 <br>
	Link: https://www.digikey.com/en/products/detail/stmicroelectronics/HTS221TR/5180551 <br>
    </td>
    <td>
		<li> Low Noise and High Resolution </li>
		<li> Hybrid SPI and I2C </li>
    </td>
    <td>
		<li> Small size </li>
		<li> Strange pin layout </li>
    </td>
  </tr>
</table>

<p align="center"> Table 5c: Humidity Sensor Component Selection 3 </p>

<table>
  <tr>
    <th style="width:25%">
	    <b>Solution</b>
    </th>
    <th style="width:35%">
	    <b>Pros</b>
    </th>
    <th style="width: 40%">
	    <b>Cons</b>
    </th>
  </tr>
  <tr>
    <td> 
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/b7ea10e3-afd7-4817-b204-d1b6bb69c9e9" /> <br>
	Name: Bosch Sensortec BME280 <br>
	Price: $6.42 <br>
	Link: https://www.digikey.com/en/products/detail/bosch-sensortec/BME280/6136306 <br>
    </td>
    <td>
		<li> Hybrid IC and SPI </li>
		<li> 3 in 1 pressure, temp and humid sensor </li>
		<li> Fast response time </li>
		<li> Good price </li>
		<li> Low power consumption </li>
    </td>
    <td>
		<li> Small size </li>
    </td>
  </tr>
</table>

## Temperature System Components

### Temperature Sensor

<p align="center"> Table 6a: Temperature Sensor Component Selection 1 </p>

<table>
  <tr>
    <th style="width:25%">
	    <b>Solution</b>
    </th>
    <th style="width:35%">
	    <b>Pros</b>
    </th>
    <th style="width: 40%">
	    <b>Cons</b>
    </th>
  </tr>
  <tr>
    <td> 
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/d49d95eb-7639-4d37-84a0-a159211c539b" /> <br>
	Name: MCP9700T-E/TT <br>
	Price: $0.30 <br>
	Link: https://www.digikey.com/en/products/detail/microchip-technology/MCP9700T-E-TT/1212510 <br>
    </td>
    <td>
		<li> This device can connect to both I2C and SPI outputs. </li>
		<li> You can surface mount it. </li>
		<li> This device has a wide temperature measurement range of -40 celsius to 125 celsius at an extended temperature and -40 celsius to 150 celsius at the high temperature. </li>
		<li> This device is optimized to drive a large amount of capacitive loads. </li>
    </td>
    <td>
		<li> It’s too small. </li>
		<li> It has a low operating current at 6 meu. </li>
    </td>
  </tr>
</table>

<p align="center"> Table 6b: Temperature Sensor Component Selection 2 </p>

<table>
  <tr>
    <th style="width:25%">
	    <b>Solution</b>
    </th>
    <th style="width:35%">
	    <b>Pros</b>
    </th>
    <th style="width: 40%">
	    <b>Cons</b>
    </th>
  </tr>
  <tr>
    <td> 
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/15031345-2c1c-4474-a92b-bda2e4949643" /> <br>
	Name: NCT75MNR2G <br>
	Price: $0.83 <br>
	Link: https://www.digikey.com/en/products/detail/onsemi/NCT75MNR2G/2748391 <br>
    </td>
    <td>
		This device can connect to both I2C and SPI outputs. </li>
		You can surface mount it. </li>
		This device has a wide temperature measurement range of -55 celsius to 125 celsius. </li>
		It has a “shutdown mode” when it has a low power consumption. </li>
		This device has an “over temperature indicator”. </li>
    </td>
    <td>
		It’s too small. </li>
		It is a “one-shot” mode. </li>
		This device has a small input voltage of 3.0 V to 5.5 V. </li>
    </td>
  </tr>
</table>

<p align="center">  Table 6c: Temperature Sensor Component Selection 3 </p>

<table>
  <tr>
    <th style="width:25%">
	    <b>Solution</b>
    </th>
    <th style="width:35%">
	    <b>Pros</b>
    </th>
    <th style="width: 40%">
	    <b>Cons</b>
    </th>
  </tr>
  <tr>
    <td> 
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/b9a35b65-73f6-4229-b2ca-78624b025d78" /> <br>
	Name: LMT84DCKR <br>
	Price: $0.80 <br>
	Link: https://www.digikey.com/en/products/detail/texas-instruments/LMT84DCKR/4090899 <br>
    </td>
    <td>
		<li> This device can connect to both I2C and SPI outputs. </li>
		<li> The outputs are short-circuited protected. </li>
		<li> You can surface mount it. </li>
		<li> The temperature is very accurate at a +/- of 0.4 celsius typical. </li>
		<li> It has a wide temperature range of -50 celsius to 150 celsius </li>
    </td>
    <td>
		<li> It’s too small. </li>
		<li> It has a low voltage operation at 1.5. </li>
		<li> It has a low quiescent current at 5.4 meu. </li>
    </td>
  </tr>
</table>
