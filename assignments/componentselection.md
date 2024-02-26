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
		<li>Used before in EGR304</li>
		<li>Can be put into series</li>
		<li>Fairly cheap</li>
		<li>In stock</li>
    </td>
    <td>
		<li>Had a few issues using it previously</li>
		<li>May not be enough/be too much voltage</li>
		<li>Not a great datasheet</li>
		<li>Not rechargeable</li>
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
		<li>Has a discharge rate (500uA)</li>
		<li>In depth datasheet</li>
		<li>12 V vs 9, won’t need to make a battery pack in series potentially if we only need 12 volt</li>
    </td>
    <td>
		<li>Probably isn’t efficient</li>
		<li>Not used this kind of battery in a system like this before</li>
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
	Name: Amazon Basics 4-Pack 9 Volt Alkaline Performance All-Purpose Batteries, 5-Year Shelf Life, Packaging May Vary
	Price: $9.58
	Link: https://www.amazon.com/Amazon-Basics-Performance-All-Purpose-Batteries/dp/B0774D64LT
    </td>
    <td>
		<li>Has a discharge rate (500uA)</li>
		<li>In depth datasheet</li>
    </td>
    <td>
		<li>Have to buy from Amazon</li>
		<li>Unsure of quality</li>
    </td>
  </tr>
</table>

<p align="center"> Choice: 1d- Amazon Basics 4-Pack 9 Volt Alkaline Performance All-Purpose Batteries </p>

Rationale: We chose this because the 1.2 A/hr seemed like the best choice versus the others. It provides the necessary amperage for every part, and will last longer than the competition. If we chose a 500 mA/hr battery, it would get drained very quickly due to the motor’s current draw. 
