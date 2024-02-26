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
    	<p>
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
    <th><b>Solution</b></th>
    <th><b>Pros</b></th>
    <th><b>Cons</b></th>
  </tr>
  <tr>
    <td> 
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/1b56bf59-16bc-44e0-964f-426e8c069229" />
    	<p>
	Name: 6LF22XWA/B
	<p>
	Price: $2.34
	<p>
	Link: https://www.digikey.com/en/products/detail/panasonic-bsg/6LF22XWA-B/5067196
    </td>
    <td>
	<li>Used before in EGR304
	<li>Can be put into series
	<li>Fairly cheap
    	<li>In stock
    </td>
    <td>
	<li>Had a few issues using it previously
	<li>May not be enough/be too much voltage
	<li>Not a great datasheet
	<li>Not rechargeable
    </td>
  </tr>
</table>

<p align="center"> Table 1c: Battery Component Selection 3 </p>

     
![b3](https://github.com/Team207-S2024/team207-s2024/assets/156377035/fa049aea-b20a-460f-ad2b-1b5b661dc1d0)


<p align="center"> Table 1d: Battery Component Selection 4 </p>


![b4](https://github.com/Team207-S2024/team207-s2024/assets/156377035/902b9b2e-6fac-4c15-890b-417b1c524b63)


<p align="center"> Choice: 1d- Amazon Basics 4-Pack 9 Volt Alkaline Performance All-Purpose Batteries </p>

Rationale: We chose this because the 1.2 A/hr seemed like the best choice versus the others. It provides the necessary amperage for every part, and will last longer than the competition. If we chose a 500 mA/hr battery, it would get drained very quickly due to the motor’s current draw. 


### Switching Voltage Regulator

<p align="center"> Table 2a: Voltage Regulator Component Selection 1 </p>


![r1](https://github.com/Team207-S2024/team207-s2024/assets/156377035/29c06b99-2c73-4fdf-8ed8-b8d8295385c9)


<p align="center">  Table 2b: Voltage Regulator Component Selection 2 </p>


     
![r2](https://github.com/Team207-S2024/team207-s2024/assets/156377035/329a5b38-57bb-4cfb-8d81-943d562c46ea)


<p align="center">  Table 2c: Voltage Regulator Component Selection 3 </p>



![r3](https://github.com/Team207-S2024/team207-s2024/assets/156377035/1686e49e-bf2b-4305-b163-cb8caf663232)


<p align="center">  Choice: LM2575D2T-3.3R4G </p>

Rationale: The class used the through hole version of this component for a prior ICC, so it would be beneficial to be able to use that knowledge going forward as much as possible. Although it wasn’t the surface mount version, it stands to reason the same circuit should theoretically work.


## Motor Subsystem Components


### Motor Driver 

<p align="center">  Table 3a: Motor Driver Component Selection 1 </p>

   ![md1](https://github.com/Team207-S2024/team207-s2024/assets/156377035/fa2f181d-d769-4e24-b150-2b5fae608ecd)

<p align="center">  Table 3b: Motor Driver Component Selection 2 </p>



![md2](https://github.com/Team207-S2024/team207-s2024/assets/156377035/6fb70a7a-9a56-4a44-aa95-f2dc19603632)

<p align="center">  Table 3c: Motor Driver Component Selection 3 </p>


![md3](https://github.com/Team207-S2024/team207-s2024/assets/156377035/6d564754-70a0-4d86-9743-f5b8525a2bc1)

<p align="center"> Choice: IFX9201SGAUMA1 </p>

Rationale: This motor driver was provided for us in class and would provide less of a learning curve, in terms of operation and coding itself. The IC itself would take less time to solder because there are less pins on the layout. 


### Motor

<p align="center"> Table 4a: Motor Component Selection 1 </p>

     
![m1](https://github.com/Team207-S2024/team207-s2024/assets/156377035/ce98df8e-5be8-418e-9900-d1be90d2d710)


<p align="center"> Table 4b: Motor Component Selection 2 </p>
     
![m2](https://github.com/Team207-S2024/team207-s2024/assets/156377035/dcf3a048-7de8-4bd3-bbe5-8329fb8fb685)

<p align="center"> Table 4c: Motor Component Selection 3 </p>

![m3](https://github.com/Team207-S2024/team207-s2024/assets/156377035/e1683a3e-649c-42b6-8b43-5e6d825b0402)


<p align="center">  Choice: 114090046 </p>

Rationale: This motor provided all the optimal specs for our specific application and was reasonably priced compared to all the other motors that were available. The compact shape also would help with mechanical design of the project. This Motor also offers a higher torque value compared to all the other DC motors and is great for pulling heavy loads, which is required for our application.


## Humidity System Components


### Humidity

<p align="center">  Table 5a: Humidity Sensor Component Selection 1 </p>

![h1](https://github.com/Team207-S2024/team207-s2024/assets/156377035/a7342114-bf14-4f61-8147-91a580e589a3)

<p align="center">  Table 5b: Humidity Sensor Component Selection 2 </p>

![h2](https://github.com/Team207-S2024/team207-s2024/assets/156377035/274d9813-0ebb-46a9-8484-f0171b79a834)

<p align="center"> Table 5c: Humidity Sensor Component Selection 3 </p>

![h3](https://github.com/Team207-S2024/team207-s2024/assets/156377035/b7ea10e3-afd7-4817-b204-d1b6bb69c9e9)

## Temperature System Components


### Temperature Sensor

<p align="center"> Table 6a: Temperature Sensor Component Selection 1 </p>

  ![t1](https://github.com/Team207-S2024/team207-s2024/assets/156377035/d49d95eb-7639-4d37-84a0-a159211c539b)
  

<p align="center"> Table 6b: Temperature Sensor Component Selection 2 </p>

![t2](https://github.com/Team207-S2024/team207-s2024/assets/156377035/15031345-2c1c-4474-a92b-bda2e4949643)

<p align="center">  Table 6c: Temperature Sensor Component Selection 3 </p>
     
![t3](https://github.com/Team207-S2024/team207-s2024/assets/156377035/b9a35b65-73f6-4229-b2ca-78624b025d78)


