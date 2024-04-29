<h1><b> EGR 314 Report </b></h1><br>
<p align="center">
	
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
	
<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/064d1419-6376-4e5f-84d7-16b91784d796" />
</p>

  <b> Portable Weather System </b><br>

  <b>Team 207</b> - <i>Atmos-Gear </i><br>

  <b>Members:</b> Isaac Linares, Danial Haddad, Manuel Garcia, Michaela De Angelis Werner<br>

  <b>Date Created:</b> 01/23/2024<br>

  <b>Date Updated:</b> 1/25/2024<br>

  <i>ASU Polytechnic, EGR 314, Travis Kelley</i><br>

</p>

# Table of Contents

1. [Introduction](#introduction)

2. [Team Organization](#team-organization)

3. [User Needs](#user-needs)

4. [Design Ideation](#design-ideation)

5. [Selected Design](#selected-design)

6. [Block Diagram](#block-diagram)

7. [Component Selection](#component-selection)

8. [Microcontroller Selection](#microcontroller-selection)

9. [Hardware Implementation](#hardware-implementation)

10. [Software Implementation](#software-implementation)

# Table of Figures

1. [Figure 1: Finished Jamboard of User Needs](https://private-user-images.githubusercontent.com/156377035/299766885-2ac812a8-3b55-4e04-ae91-dae0052d43f2.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTQzMzI2ODYsIm5iZiI6MTcxNDMzMjM4NiwicGF0aCI6Ii8xNTYzNzcwMzUvMjk5NzY2ODg1LTJhYzgxMmE4LTNiNTUtNGUwNC1hZTkxLWRhZTAwNTJkNDNmMi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNDI4JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDQyOFQxOTI2MjZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0xZTNmNTA5ODBiMmU1NDdjZTRkOGE4MTZhZTkwNmIyNDY0ZWUwMzAyMWE0M2JiODRmOWVmNjU2MjBhZDgwYjE1JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.ArcOBsUg4yPSEcTkKJNqxfl_IK3JsyMaBJx0Ku92bjc)

2. [Figure 2: Finished Jamboard Page of the Groups of Needs](https://private-user-images.githubusercontent.com/156377035/299766975-f76e13a6-ce90-4a6b-9a01-4b5c41783925.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTQzMzI5MTEsIm5iZiI6MTcxNDMzMjYxMSwicGF0aCI6Ii8xNTYzNzcwMzUvMjk5NzY2OTc1LWY3NmUxM2E2LWNlOTAtNGE2Yi05YTAxLTRiNWM0MTc4MzkyNS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNDI4JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDQyOFQxOTMwMTFaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT04MDJmM2VhMmRjZjkwZTg0Y2JlZTIwZWQ2MWVjYTI1ZTI5ZWU5YTE4OTRjZjRjN2ZiZDA1NzE4ODY1ZjI0YWMzJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.UIfvSRdMtWGEqiKMTI40wW2308cU4Acv2331qM8S2QY)

3. [Figure 3: Finished Jamboard Page for Ranking Needs](https://private-user-images.githubusercontent.com/156377035/299767086-f3bcb418-bae8-489a-8c10-d187e2fbfd16.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTQzMzI5NTcsIm5iZiI6MTcxNDMzMjY1NywicGF0aCI6Ii8xNTYzNzcwMzUvMjk5NzY3MDg2LWYzYmNiNDE4LWJhZTgtNDg5YS04YzEwLWQxODdlMmZiZmQxNi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNDI4JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDQyOFQxOTMwNTdaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0wMTg2MjJlYjk4NjQ1NjVkZWI5ZTVjOTQ2ODY3YmZlZDg3N2U5NzVkNzU3OGEzOTkzZGFhYzA3ZDgwZWUzNmZmJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.06VVG2nwkZYVbcItKqFNDM5SFIKcBHs9Y1Kc5RTY6Ec)

4. [Figure 4: Jamboard of 100+ Ideas](https://private-user-images.githubusercontent.com/156377035/299767277-c6f79873-33ad-46b4-95e5-f77cf2fe6bc5.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTQzMzMwMTgsIm5iZiI6MTcxNDMzMjcxOCwicGF0aCI6Ii8xNTYzNzcwMzUvMjk5NzY3Mjc3LWM2Zjc5ODczLTMzYWQtNDZiNC05NWU1LWY3N2NmMmZlNmJjNS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNDI4JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDQyOFQxOTMxNThaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT02NjVjNmUwZDYzMDBkODExNWE1NGRiOThlNWQ3M2QzNjAxYjljNDExZjExMDZlODM4OGQ0NjJiYTViZDBjMWNlJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.5ZudBVdLmnNSccF0c4hT27FkICj29iIvEz9fqivzQX8)

5. [Figure 5: Jamboard of Sorted Ideas](https://github.com/Team207-S2024/team207-s2024/assets/156377035/05bf809c-ae8a-430f-bfd4-adbaf3a57823)

6. [Figure 6: Visual Representation of the Fishing Box Plus Weather Balloon](https://github.com/Team207-S2024/team207-s2024/assets/156377035/e3151873-df6c-43e4-ad2b-46fe11cc6450)

7. [Figure 6a: .svg Version of a Visual Representation](https://github.com/Team207-S2024/team207-s2024/assets/156377035/0c427504-2fb9-4878-b487-55d578584596)

8. [Figure 7: Visual Representation of GPS Plus Cat Collar](https://github.com/Team207-S2024/team207-s2024/assets/156377035/1fd00c4e-63b4-4b71-bf99-68123fe1c7a1)

9. [Figure 7a: .svg Version of a Visual Representation](https://github.com/Team207-S2024/team207-s2024/assets/156377035/79927f99-460f-4052-906a-408744bbc65d)

10. [Figure 8: Solidworks Drawing of a Temperature Sensor for Optimal Sunlight](https://github.com/Team207-S2024/team207-s2024/assets/156377035/eae8ae64-4bde-4a5f-b422-1e579a1550ce)

11. [Figure 9: Solidworks Drawing of a Mobile Plant Caretaker](https://github.com/Team207-S2024/team207-s2024/assets/123421321/9130f44f-f915-409b-8f47-7eacb999dd05)

12. [Figure 10: Current Block Diagram of the project.](https://github.com/Team207-S2024/team207-s2024/assets/156377035/726e697d-b265-4ec1-9471-99309df1da97)

13. [Figure 11: Current Power Budget of the Project.](https://github.com/Team207-S2024/team207-s2024/assets/156377035/cf89bee4-d5e6-4fe6-bfba-b43d13470e2d)

14. [Figure 12: Final Schematic of the Project.](https://github.com/Team207-S2024/team207-s2024/assets/156377035/a5f646c2-cc15-4f79-939f-580197792419)

15. [Figure 13: Top and Bottom PCB Layout of the Project.](https://github.com/Team207-S2024/team207-s2024/assets/156377035/4c162306-1a49-4cd9-a8e2-2fcc4e730346)

16. [Figure 14: Picture of PCB fully soldered.](https://github.com/Team207-S2024/team207-s2024/blob/main/images/hardwareproposal/imgonline-com-ua-twotoone-ZomtRfHAWU0FwS.jpg?raw=true)

17. [Figure 15: Current Bill of Materials for the project.](https://github.com/Team207-S2024/team207-s2024/assets/157151171/305feb18-94b1-4edf-b72a-67d888a22c15)

18. [Figure 16: Final Software Implementation UML Chart](https://github.com/Team207-S2024/team207-s2024/assets/156377035/8b84c7f2-362e-4973-926b-3156ad32424d)

19. [Figure 17: Example of Output into MQTT.](https://github.com/Team207-S2024/team207-s2024/assets/156377035/cc5276a2-97fd-414c-bc85-24fcd4e0118f)

20. [Figure 18: Example of Output into MQTT.](https://github.com/Team207-S2024/team207-s2024/assets/156377035/0ea8b264-448c-4806-b154-7555bd1155ee)

21. [Figure 19: Picture of Innovation Showcase Poster.](https://github.com/Team207-S2024/team207-s2024/assets/157151171/79103f75-4e04-4a18-b838-770c90ca01da)

22. [Figure 20: Picture of System Verification Table.](https://github.com/Team207-S2024/team207-s2024/assets/156377035/d4e36a0c-91db-4d79-a53d-7dbb2d148827)



# Appendix

[Appendix A: Team Organization Document](https://team207-s2024.github.io/team207-s2024/assignments/teamorganization)

[Appendix B: User Needs and Benchmarking](https://team207-s2024.github.io/team207-s2024/assignments/userneeds-benchmarking)

[Appendix C: Product Requirements Document](https://team207-s2024.github.io/team207-s2024/assignments/productrequirements)

[Appendix D: Design Ideation](https://team207-s2024.github.io/team207-s2024/assignments/designideation)

[Appendix E: Selected Design](https://team207-s2024.github.io/team207-s2024/assignments/selecteddesign)

[Appendix F: Block Diagram](https://team207-s2024.github.io/team207-s2024/assignments/blockdiagram)

[Appendix G: Component Selection](https://team207-s2024.github.io/team207-s2024/assignments/componentselection)

[Appendix H: Microcontroller Selection](https://team207-s2024.github.io/team207-s2024/assignments/microcontrollerselection)

[Appendix I: Software Implementation](https://team207-s2024.github.io/team207-s2024/assignments/softwareimplementation)

[Appendix J: Hardware Implementation](https://team207-s2024.github.io/team207-s2024/assignments/hardwareimplementation)

## Introduction

The following is an exhaustive report on Team 207's project for EGR314. Below you will find the research, prototyping, and implementation of the team's idea. 

The project itself is currently named *"Mobile Plant Caretaker,"* and as the name suggests, it aids the user in taking care of a potted plant by automatically moving it in and out of shade based on whether it is too hot or too cold, and whether it needs water or not. It is meant to be lightweight for the user to be able to put it where they need to and be mobile in the sense of not needing to be plugged in. To fulfill the ESP32 requirements, it will send its data over Wi-Fi so the user can see how the temperature and humidity and the plant fluctuate over certain intervals. In addition, it will send out a small notification when the plant needs water, so the user can water the plant themselves.

The Mobile Plant Caretaker represents a show of advancement in the realm of automated plant management systems, offering a sophisticated yet user-friendly solution to the challenges of maintaining optimal growing conditions for potted plants. By taking advantage of a combination of IC hardware components and C+ software algorithms, our device represents technological interactions aimed at making plant care more efficient in diverse environments.

Through an adventurous process of research and prototyping, our team has successfully engineered a device that exceeds traditional approaches to plant care. At its core, the Mobile Plant Caretaker contains two sensors, including a temperature and humidity sensor, to continuously monitor the plant's immediate environment. Coupled with a motorized actuator, this system enables precise adjustments to the plant's position relative to light sources, ensuring optimal exposure for photosynthesis and growth.

The ESP32 microcontroller, central to the functionality of the Mobile Plant Caretaker, is a powerful computing platform that collects sensory data and contains wireless communication capabilities. By harnessing the ESP32's processing power, our device delivers real-time insights into environmental metrics, allowing users to remotely monitor and intervene as necessary through the MQTT software on a laptop interface.

What distinguishes the Mobile Plant Caretaker is not just its technical sophistication, but also its potential to revolutionize the way we interact with plants. In essence, the Mobile Plant Caretaker represents a convergence of scientific innovation and practical utility, creating a new era of smart plant care solutions for enthusiasts and professionals alike.


[Here](https://embedded-systems-design.bitbucket.io/course-sequence-requirements/) is a link to the requirements for this course. 

## Team Organization

The following subsections will detail our process for the team charter and mission statement. For the sake of
succinctness, everything else is consolidated into the appendix.

Refer to [Appendix A: Team Organization Assignment](https://team207-s2024.github.io/team207-s2024/assignments/teamorganization) 
for further information about our team organization and team decisions.

### Team Charter

The team decided on the charter fairly late but eventually agreed on what everyone wanted for the group in terms of personal goals. It was agreed that serial communication and the knowledge needed for that is something very important for an engineer to understand, no matter what kind. Many components, including various sensors and drivers, require knowledge of not only the basics of how to set up serial communication but how to find the information required to set it up. That concept includes understanding how to access and read datasheets for products, as well as how to manipulate bits. 

_Our goal is to gain knowledge in digital circuits that utilize serial communication. 
We as a team want this product to be compared to other professional-grade devices being sold on the market._

### Mission Statement

After talking with each other about one another's interests, the team began to determine what the project
needed to have as well as what each individual member wanted it to have. The product requirements were also a significant factor in what we wanted for the mission statement. 

_The mission of the team is to create a sensor-based weather-reporting product that is unique, portable, 
professional, reliable, and user-friendly. It is something that should be focused so that a person can easily
use and install themselves and is relatively simple to collect data from, along with contingency plans in case things go awry._

## User Needs

The team worked exceptionally hard at identifying and deciphering the user needs necessary for a successful project, which included research into similar products that used the name of the project as tags. Each team member created at least one setup for a product and 3 positive/negative reviews for each product, with comments on what user needs that could be derived from each review. Once each member was done, members contributed to a Jamboard with each user need deriving from the research as well as ideas that members came up with. It involved multiple days of back and forth, from creating to grouping to ranking the needs. Finally, the user needs were consolidated into an easy-to-read table ranked all together. 

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/2ac812a8-3b55-4e04-ae91-dae0052d43f2" />
</p>

<p align="center">
  <i>Figure 1: Finished Jamboard Page of User Needs</i>
</p>

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/f76e13a6-ce90-4a6b-9a01-4b5c41783925" />
</p>

<p align="center">
  <i> Figure 2: Finished Jamboard Page of the Groups of Needs </i>
</p>

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/f3bcb418-bae8-489a-8c10-d187e2fbfd16" />
</p>

<p align="center">
  <i>Figure 3: Finished Jamboard Page for Ranking Needs </i>
</p>

Refer to [Appendix B: User Needs and Benchmarking Assignment](https://team207-s2024.github.io/team207-s2024/assignments/userneeds-benchmarking)
for further information, the content of the VOC research, and the final table derived from the work. 

The PRD (Product Requirements Document) was developed soon after, which involved creating unique scenarios for a potential product in order to generate further ideas as well as brainstorming potential stakeholders and what each person wanted from the project. Open questions were also developed that can hopefully be answered as the product develops. The aspects created from the PRD are going to be what the project will use as a baseline for the minimum requirements that the group designs as necessary.  

Refer to [Appendix C: Product Requirements Document Assignment](https://team207-s2024.github.io/team207-s2024/assignments/productrequirements)
for further information about the brainstorming the team did for this assignment, including the stories and aspects created.

## Design Ideation

The design ideation process involved looking back at the user needs, turning them into functions a product could have, and putting them onto a Jamboard for a visual representation. Once finished, people grouped them according to an overall general functionality. Finally, people developed 3 distinct ideas to figure out a concrete idea going forward.

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/c6f79873-33ad-46b4-95e5-f77cf2fe6bc5" />
</p>

<p align="center">
  <i>Figure 4: Jamboard of 100+ Ideas </i>
</p>

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/05bf809c-ae8a-430f-bfd4-adbaf3a57823" />
</p>

<p align="center">
  <i>Figure 5: Jamboard of Sorted Ideas</i>
</p>

### Fishing Box + Weather Balloon

The Fishing Box Plus Weather Balloon (Name Subject to Change) is a set of sensors tied to a weather balloon suspended in the air, where it’ll get and store data. Once it reaches certain thresholds of data, it will transfer data to a device on the ground, which will have stakes to keep it (and the sensors) in place. The box will have an LCD screen with buttons to flip through data and do other functions, such as exporting data onto an SD card for emergencies. When necessary, the box can either take down the weather balloon by clicking on a button, or the user can manually use a crank on the side to manually take it down.

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/e3151873-df6c-43e4-ad2b-46fe11cc6450" />
</p>

<p align="center">
  <i>Figure 6: Visual Representation of the Fishing Box Plus Weather Balloon</i>
</p>

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/0c427504-2fb9-4878-b487-55d578584596" />
</p>

<p align="center">
  <i>Figure 6a: .svg Version of a Visual Representation </i>
</p>

### GPS + Cat Collar

The GPS Plus Cat Collar (Name Subject to Change) is a cat collar with sensors for humidity and temperature installed onto it, as well as a location tracker. The purpose of the device is to see where feral/outdoor cats go to keep warm and dry/comfy. How it works is you capture a feral/outdoor cat, put the collar on, and then let them free. It will then begin autonomously tracking the cat and where it goes, namely its most common hideouts. Then, when the cat gets near the ‘home base’ (as in, when the collar can connect to a server through Wi-Fi), it will then transmit what data it stored onto the server in a readable format, by parsing through the sensor/tracking data. If in the event where the user doesn’t want the cat to wear the device anymore, and it is in the area, they can put out a radio/Wi-Fi signal that will unlock the collar through a motorized locking system. 

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/1fd00c4e-63b4-4b71-bf99-68123fe1c7a1" />
</p>

<p align="center">
  <i>Figure 7: Visual Representation of GPS Plus Cat Collar</i>
</p>

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/79927f99-460f-4052-906a-408744bbc65d" />
</p>

<p align="center">
  <i>Figure 7a: .svg Version of a Visual Representation</i>
</p>

### Optimal Sunlight for a Plant

This device would feature a sensor that can detect temperature and humidity levels which would then send data over to the stand, the stand, which is controlled by a motor mechanism would then move the plant sitting inside the pot to the optimal position to either increase or decrease the received sunlight by the plant. The device could also send over data via Wi-Fi to alert the user of weather conditions such as temperature and humidity and update the user on the life of the plant.  

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/eae8ae64-4bde-4a5f-b422-1e579a1550ce" />
</p>

<p align="center">
  <i>Figure 8: Solidworks Drawing of a Temperature Sensor for Optimal Sunlight</i>
</p>

Refer to [Appendix D: Design Ideation Assignment](https://team207-s2024.github.io/team207-s2024/assignments/designideation)
for further information about the design ideation process.

## Selected Design

The selected design was [Optimal Sunlight for a Plant](#optimal-sunlight-for-a-plant), but expanded upon. For one, the movement of the plant was decided to be put on a belt-like system, where it would move along on a platform placed on treads based on the temperature/humidity sensors. It would also move to and from a shaded area based on a comparison of the sensor data. For the temperature, it would check the temperature of the area, and determine whether it would be too hot or too cold for the plant. For the humidity, it would check the soil for if it was too wet or dry, and move based on that data. In addition, it was determined a good way of utilizing the ESP32 requirement would be to signal over Wi-Fi if the plant needed watering or not. 
The plan is for this to not only be mobile in terms of the device moving something but also be lightweight enough for a user to position this where they need to as well as using batteries so it does not need to be tied down anywhere. 

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/123421321/39f9c1cf-7efa-44a7-adc1-816b349d2b55" />
</p>


<p align="center">
  <i>Figure 9: Solidworks Drawing of a Mobile Plant Caretaker</i>
</p>

<div class="embed-container">
<iframe width="560" height="315" src="https://www.youtube.com/embed/AGAKjpmc-Ck?si=usMTWPXO7_qgTkfR" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>
<style>
.embed-container {
  position: relative;
  padding-bottom: 56.25%;
  height: 0;
  overflow: hidden;
  max-width: 100%;
}
.embed-container iframe,
.embed-container object,
.embed-container embed {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
</style>

Refer to [Appendix E: Selected Design](https://team207-s2024.github.io/team207-s2024/assignments/selecteddesign) for further information about the selected design.

## Block Diagram

Once the team decided on a concept to move forward with, it became time to determine how the entire project would fit together within the technical requirements of the project. Thus, the group created a block diagram to hash out a basic concept of how everything would fit together on a technical level. It began with a rough idea, but once components were selected and finalized, the group was able to select what pins were necessary for each component to communicate with one another.

By carefully analyzing user needs, selecting appropriate components, and constructing a visual representation of component interconnections, the block diagram ensures that the flower pot meets our objectives. Each selected component, including the PIC18LF26K40 microcontroller, temperature sensor, motor driver, and humidity sensor, serves a specific function essential for the flower pot's ability to monitor environmental conditions, orient itself toward sunlight, and notify users of soil moisture levels. Overall, the block diagram represents a comprehensive solution that fulfills user needs while considering technical feasibility and stakeholder interests.

During this point, each team member chose their assigned subsystem. The choices were as follows:

**Isaac Linares:** Humidity Sensor 

**Danial Haddad:** Temperature Sensor

**Manuel Garcia:** Motor Driver/Motor

**Michaela De Angelis Werner:** Microcontroller/Power Supply

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/726e697d-b265-4ec1-9471-99309df1da97" />
</p>

<p align="center">
  <i>Figure 10: Current Block Diagram of the project. </i>
</p>

Refer to [Appendix F: Block Diagram](https://team207-s2024.github.io/team207-s2024/assignments/blockdiagram) for further information, such as a step-by-step breakdown of each component and its overall function within the project.

## Component Selection

As soon as the block diagram was finished, the team began considering the components to fill in the gaps. Each team member studied their assigned subsystem and picked a series of main components that each subsystem critically required. From there, the team member would choose which component out of the lists would be the best fit for this project. The chosen components for each subsystem are as follows:

<table style="width:100%">
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
      <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/0725b3b2-84f1-48d5-a1ad-e1e32612b734" /> <br>
	Name: Amazon Basics 2-Pack 9 Volt Lithium High-Performance Batteries, 10-Year Shelf Life, Long Lasting Power <br>
	Price: $16.38 <br>
	Link: https://www.amazon.com/AmazonBasics-Volt-Lithium-Batteries-8-Pack/dp/B082DMR8DJ <br>
    </td>
    <td>
		<li> Great reviews</li>
		<li> Lithium </li>
		<li> High shelf life </li>
    </td>
    <td>
		<li> Have to buy from Amazon </li>
		<li> Unsure of capacity, but it should be enough according to similar products </li>
    </td>
  </tr>
</table>

<p align="center"> Choice for Battery: Amazon Basics 2-Pack 9 Volt Lithium High-Performance Batteries, 10-Year Shelf Life, Long Lasting Power </p>

Rationale: The group chose this because even though there is not a datasheet to help determine capacity, based on being a lithium battery with stellar reviews and similar products being of the necessary capacity, it seemed like a good enough risk to take. Note that this will be for regular use, and the group may utilize other batteries over throughout the testing phase to see how it can work.

<table style="width:100%">
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
	Link: https://www.digikey.com/en/products/<br>detail/onsemi/LM2575D2T-3-3R4G/1476688 <br>
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

<p align="center"> Choice for Regulator: LM2575D2T-3.3R4G </p>

Rationale: The class used the through-hole version of this component for a prior ICC, so it would be beneficial to be able to use that knowledge going forward as much as possible. Although it wasn’t the surface mount version, it stands to reason the same circuit should theoretically work.

<table style="width:100%">
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
	Link: https://www.digikey.com/en/products/<br>detail/infineon-technologies/IFX9201SGAUMA1/5415542 <br>
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

<p align="center"> Choice for Motor Driver: IFX9201SGAUMA1 </p>

Rationale: This motor driver was provided for us in class and would provide less of a learning curve, in terms of operation and coding itself. The IC itself would take less time to solder because there are fewer pins on the layout. 

<table style="width:100%">
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
	Link: https://protosupplies.com/product/<br>dc-geared-motor-and-wheel-kit-3-9v-77rpm/ <br>
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

<p align="center">  Choice for Motor: 114090046 </p>

Rationale: This motor provided all the optimal specs for our specific application and was reasonably priced compared to all the other available motors. The compact shape also would help with the mechanical design of the project. This Motor also offers a higher torque value compared to all the other DC motors and is great for pulling heavy loads, which is required for our application.

<table style="width:100%">
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
	Link: https://www.digikey.com/en/products/detail/<br>honeywell-sensing-and-productivity-solutions/HIH6030-021-001/4291625 <br>
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

<p align="center">  Choice for Humidity Sensor: Honeywell Sensing and Productivity Solutions HIH6030-021-001 </p>

Rationale: This humidity sensor was in stock, was I2C compatible, and seems relatively easy to solder and use. It has a typical application circuit and a decent datasheet to work with.

<p align="center"> <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/b9a35b65-73f6-4229-b2ca-78624b025d78" /> </p>
<p align="center"> Choice for Temperature Sensor: TC74A4-3.3VCTTR </p>

Rationale: This temperature sensor was used in class, so there is a surplus of knowledge and reusable code that the group can utilize. 

### Power Budget

The team also began work on the power supply for the system, with mixed results. Due to a mixture of paltry information about batteries as well as a less-than-perfect iteration of the calculator used, the results are not as good as they could be. 

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/cf89bee4-d5e6-4fe6-bfba-b43d13470e2d" /> 
</p>
<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/05aa3dde-48a0-4d65-ab61-33576b70d516" /> 
</p>

<p align="center">
  <i>Figure 11: Current Power Budget of the Project. </i>
</p>

Refer to [Appendix G: Component Selection](https://team207-s2024.github.io/team207-s2024/assignments/componentselection) for further information, such as the full list for each subsystem and its components.

## Microcontroller Selection

The microcontroller selection was done soon after the component selection. The process was incredibly tedious and confusing at the time, given that there were some questions regarding terminology and just how many serial communication pins were necessary. Overall, though, the search was an enlightening one and made the group more knowledgeable about the differences between the microcontrollers available. 

Eventually, the group decided to go forward with the PIC18F26K40, for many reasons. For one, it will be a significantly nicer time to solder its 28 pins versus the competition's 40-64 pins. In addition, many previous groups had success with it, meaning that in the chance that help is necessary, the group can find it through previous students. Finally, the extensive documentation and the large datasheet will be critical when it comes to working with it, hardware and software-wise. 

Refer to [Appendix H: Microcontroller Selection](https://team207-s2024.github.io/team207-s2024/assignments/microcontrollerselection) for further information, which includes a full table of what was considered, the information on each microcontroller, and the pros/cons of each one.

## Hardware Implementation

Soon after, it was time to begin putting everything together. At first, each member took the time to create their own subsystem's circuit according to not only their datasheets but also prior knowledge of using certain components. Next, they were compiled into one schematic, getting a good idea of where each pin would go with regards to each other system. Finally, the team took care in organizing the subsystems and various subcircuits in a way that could flow decently. Once tested on a beginning team board, the group made the necessary changes to the schematic to make it work correctly. 

One of the most significant changes made between the original team schematic and the final team schematic was that the motor driver's SO and SI pins had to be changed to properly function- effectively, the microcontroller was sending an input into an input, instead of sending an input into an output. That made it so it could not get the exchange of bits necessary to move the motor. This was fixed in the schematic, which meant in the final PCB it was not necessary to make and break connections.

One change that should have been made but was not implemented, is the swap between the ESP32's VIN power pin and 3V3 power pin, which was due to a misunderstanding and less than accurate information found online. When the ESP32 is plugged into a computer via USB, it can output either 5V or 3.3V out of the respective pins. However, when it is not plugged in, VIN and 3V3 turn into alternative power pins to plug the respective voltages into. Unfortunately, by the time the final PCB was printed, it was not realized that it was necessary to swap the 3.3V power plane going into VIN to instead go into 3V3. This was fixed by simply fly-wiring (as in, connecting the ESP32 to the board through male-to-female wires) and swapping where the voltage would go. 

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/a5f646c2-cc15-4f79-939f-580197792419" />
</p>
<p align="center">
  <i>Figure 12: Final Schematic of the Project. </i>
</p>

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/4c162306-1a49-4cd9-a8e2-2fcc4e730346" />
</p>
<p align="center">
  <i>Figure 13: Top and Bottom PCB Layout of the Project. </i>
</p>

<p align="center">	
  <img src = "https://github.com/Team207-S2024/team207-s2024/blob/main/images/hardwareproposal/imgonline-com-ua-twotoone-ZomtRfHAWU0FwS.jpg?raw=true" />
</p>
<p align="center">
  <i>Figure 14: Picture of PCB fully soldered. </i>
</p>

### Version 2.0

If the PCB were to be made again, with certain restrictions unlocked, there is a decent amount that could be done to augment the concept. 

One primary area for improvement lies in the layout and spacing of components on the PCB. In the original design, while efforts were made to ensure minimal interference between subsystems, there remains room for refinement. By reducing the space between components, especially sensors and control modules, the overall footprint of the device could be minimized. This not only enhances portability but also facilitates a more streamlined and compact design, which is crucial for applications where space is a constraint.

Moreover, revisiting the choice of components offers an opportunity for improvement. In the initial design, certain components such as bypass capacitors and humidity sensor resistors were larger than necessary, potentially occupying more space on the PCB than needed. Downsizing these components while maintaining proper functionality can lead to more efficient use of board real estate, enhancing the overall performance of the device.
Additionally, a crucial aspect that warrants attention is the power supply configuration, particularly concerning the ESP32 microcontroller. The oversight regarding the swap between the VIN and 3V3 power pins highlights the importance of accurate information and following a thorough analytical process during the design phase. In "Version 2.0," fixing this issue by ensuring the correct power distribution to the ESP32 is essential to receive and send data at the correct voltage rate.

Additionally, exploring alternative approaches to interfacing with external components could enhance the versatility and adaptability of the hardware design. For instance, incorporating additional room for daughter boards can offer flexibility in accommodating additional sensors or actuators without compromising the integrity of the main PCB layout. This small fix enables future scalability and customization, allowing the device to evolve and adapt to varying application requirements. Adding this feature leaves more room for expanding upon the existing design by incorporating an automatic watering system. When the plants are moved into the enclosure due to high temperatures, the microcontroller can trigger a water pump to deliver the appropriate amount of water to the plants. Moreover, by incorporating sensors to measure soil moisture levels, the watering system can ensure that plants receive proper hydration without the risk of overwatering or underwatering. This feature not only complements the protective function of the device but also promotes optimal plant growth and health. Adding safety features such as soil sensors enhances the device's ability to maintain proper growing conditions. Soil sensors can continuously monitor moisture levels in the soil, allowing the microcontroller to adjust watering schedules accordingly. This approach helps prevent water stress and ensures that plants receive the necessary moisture for healthy growth.

Incorporating these additional features not only enhances the functionality of the device but also contributes to a more holistic approach to plant care. By leveraging technology to monitor and respond to environmental cues, the device can create an optimal growing environment for plants, minimizing stressors and promoting vigorous growth. This approach to plant protection and care underscores the importance of integrating multiple sensors and systems to create a robust and effective solution for plant health management.

### Bill of Materials

The group also finalized the bill of materials for the project to send out a purchase request. The first iteration of the purchase request was not perfect, but it was revised as soon as it could be. 

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/157151171/305feb18-94b1-4edf-b72a-67d888a22c15" />
</p>

<p align="center">
  <i>Figure 15: Current Bill of Materials for the project. </i>
</p>

Refer to [Appendix I: Hardware Implementation](https://team207-s2024.github.io/team207-s2024/assignments/hardwareimplementation) for further information, such as a full breakdown of the schematic, including each subsystem and circuit. If necessary, the history of the page can be found [here](https://github.com/Team207-S2024/team207-s2024/commits/main/assignments/hardwareimplementation.md) if one were to be interested in the process of how the hardware implementation developed over the semester. 

## Software Implementation

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/8b84c7f2-362e-4973-926b-3156ad32424d" />
</p>

<p align="center">
  <i>Figure 16: Final Software Implementation UML Chart</i>
</p>

The software implementation went through a variety of changes over the semester, although the basic concept of moving a plant in and out of shade based on sensor data remained the same. Some of the reasons for the changes included roadblocks involving coding difficulties as well as misunderstandings of what the software might represent. Much of the implementation was edited according to what the final code turned out to be. 

For a brief explanation, the system will continuously check for if the surrounding temperature of the box is too high a temperature for the plant to do well. If it is too high, it will then make another check for if it is at "home" or not (if it is under the shade or not.) If it is at home and it is too hot, it will stay in place. If it is not at home, it will move the plate home. This is to make sure that the motor does not accidentally drive the plate into the holding space, which could cause damage to the system as well as the plant. After a certain amount of time, it will then make another check to see if it is gotten cooler and thus healthier for the plant- if it has, and it is at home, then it will move back out of the shade. If it is not at home, it will sit in place. 

Simultaneously, it will read the humidity data of the surrounding area of the box, and likewise translate the data into something readable. If the humidity data is below a certain amount, then it will also check if it is at home or not. If it is at home, it will do nothing, but if it is not at home, it will move the plate out and set the alert variable to 1. The intention is that it is meant to alert the user that the plant should be watered. 

Once done with reading data and completing actions, it will then print the data to the ESP32, and thus send it to the MQTT server. Below is an example of what kind of data would be shown:

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/cc5276a2-97fd-414c-bc85-24fcd4e0118f" />
</p>

<p align="center">
  <i>Figure 17: Example of Output into MQTT. </i>
</p>

Here is the MQTT Topic Table we used to determine how best to go about developing our ESP32 Code: 

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/0ea8b264-448c-4806-b154-7555bd1155ee" />
</p>

<p align="center">
  <i>Figure 18: Example of Output into MQTT. </i>
</p>

### Five Biggest Changes Since Software Proposal

There were a lot of changes to the flow of the software proposal, but the top 5 biggest changes will be outlined below. 

<b> 1. Motor Move Position Interrupt </b>

When coming up with the software proposal, it was assumed that it would be easy to detect the motor position and create an interrupt that would manually stop the motor if it would go too far. However, in reality it was significantly easier to code the motor going forward/backward according to delays, and then creating the home variable to control if it would move or not. The intention of stopping the motor before it would go too far was the same, but the actual implementation was not a proper interrupt. Programming-wise, it is a cruder method as during delays, the microcontroller will not do anything which can cause issues.

<b> 2. Humidity Sensor Issues </b>

In the beginning it was assumed that the humidity sensor would work simply like the temperature controller. However, it actually required significantly more coding prowess than what was assumed, which meant the software proposal concept simply did not match the actual work required for the humdity sensor to function. We also found that we had to replace the humidity sensor due to us receiving a buggy/defective humidity sensor. Though there was a chance to replace the on-board sensor, we decided to not potentially cause issues from desoldering and resoldering a new humidity sensor, and instead left it as-is. 

<b> 3. Overall Flow of Main Loop </b>

The main loop of the original software proposal was done at a time where it was a bit vague on how the actual setup would work. It was very clunky originally, and really did not make a lot of sense. The final  correctly follows what was actually written code-wise, instead of blindly writing pseudocode and then trying to make it flow in a "professional" way. 

<b> 4. Misunderstandings of Checks </b>

It was not actually necessary to make variables for high humidity or temperature, it is more accurate to make a basic check function and work off of that instead of making additional variables to keep track of. There might be a good reason one might want to do that, but for this circumstance it did not seem necessary. 

<b> 5. Misunderstandings of Motor </b>
The motor really did not need to check if there was a signal or not, this was done because there was a misunderstanding of whether technical lingo was necessary for this assignement rather than something actually readable. 

Refer to [Appendix J: Software Implementation](https://team207-s2024.github.io/team207-s2024/assignments/hardwareimplementation) for further information, including a full breakdown of what the UML chart demonstrates as well as how each part aids in the user needs stated previously within the report. If necessary, the history of the page can be found [here](https://github.com/Team207-S2024/team207-s2024/commits/main/assignments/softwareimplementation.md) if one were to be interested in the process of how the hardware implementation developed over the semester. 

## Innovation Showcase Poster

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/157151171/79103f75-4e04-4a18-b838-770c90ca01da" />
</p>

<p align="center">
  <i>Figure 19: Picture of Innovation Showcase Poster. </i>
</p>

## System Verification

Finally, the group created a system verification table that would showcase how each system is connected. It was then confirmed by the teaching team over the end of the semester.

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/d4e36a0c-91db-4d79-a53d-7dbb2d148827" />
</p>

<p align="center">
  <i>Figure 20: Picture of System Verification Table. </i>
</p>

## Lessons Learned

Many things were learned in this class, both hardware and software-wise. Below is a numbered list of the top 10 that the group considered: 

1. The simplest solution is usually the best solution. If you have a lot of time to kill you can try to make something very complex, but know that it will probably be your undoing. Keep it simple. 

2. When working with communication methods, try to make all components use the same language. If one is I2C, the rest should be as well. The same goes for SPI. Each one has its ups and downs, and that is something you would need to figure out for yourself on what you are comfortable with.

3. It is best to assign a person dedicated to whatever they are best at doing/most comfortable with. It is also good to put people in situations that they may not be the best at so they can improve. 

4. Things are going to break, so it is always best to keep backups of every part/system. You will be learning by doing, and sometimes you will not know what to do, and that is okay.

5. Sometimes it is faster to replace a part rather than fix it. Fixing a sinking ship is cheaper than escaping and buying another one, but whether you will fix it before you drown is hard to say. 

6. Picking a part with a well-made/detailed datasheet is very important. This goes the same for technical notes. If a part has convoluted notes then it is going to be a pain to work with or debug.

7. Proper communication with teammates is the key to success and making sure you find people that you both can work with and have casual conversations with is always the best route. 

8. Having dedicated meeting times with your team can lead to a major boost in productivity. We believe that is what allowed us to be so successful with our design compared to other teams. 

9. Trying to do everything yourself is never a good idea, asking for help from your fellow teammates should not be frowned upon but instead encouraged. Trying to do everything yourself is a recipe for disaster, both for you and your group. You can not learn anything if someone else is doing everything, and you do not learn to work with people if you do not let them help. 

10. When ordering a board, the extra investment it takes to get a good quality board with good solder masking and pads is well worth it. It saved us a lot of time to do our team prototype on a JLC printed board rather than the Peralta boards here. That is not to say the Peralta boards are impossible to use, but whether it is worth painting soldermask on versus buying a JLC board for 15-20 bucks is up to you.

## Recommendations

There is a lot of recommendations to give, and it is a bit difficult to leave it to 5, but here are the top 5 that the group considered:

<b> 1. Time Management </b>

There are a lot of things to learn and do in this class, and getting them done is paramount to getting a working project in the end. It is a bit of a lie to make this (and EGR 304) a 3-credit course, because it tells people that it is possible to succeed with only a couple of hours outside of class to get things done. It does not. Take advantage of all the free time you can muster, talk to TAs, talk to other students, make sure that you are doing at least 5-15 extra hours if you can help it. That seems like a lot, but it goes away really quickly as you are learning by doing, and that takes a lot of time. You will learn, but you will struggle at some point. 

<b> 2. Group Management </b>

This is probably the meanest thing to say out of everything here, but depending on your situation it will be extremely important. Make sure that people are doing their job, and are not slacking off. If someone is not doing their job, do not try to handle it yourself before going to the instructor. Tell the instructor immediately what is going on so it can get worked out immediately. While it is nice to keep everything in the group, sometimes it can get sour very quick. If you take too long in alerting the instructor something is wrong, there is a high chance of that person getting away with it, and being allowed to succeed when they should not have. This sounds harsh, but it is for the best that you understand how important it is to not overexert yourself so someone else can slack off. As stated previously, there is a lot to do in this course, and you will burn out if you think you can get it done by yourself. You need a team to get through it, not people relying on you to carry them. 

<b> 3. Pick Easy Parts </b>

Exactly as it sounds, pick the simplest part because the room for error is usually very low. Our recommendation is based a lot on the communication type and datasheet of the part. A part that has a well-written datasheet and technical notes is always a good choice. It is also even better if said notes have a debug section detailing what you can do if you run into a specific problem. If it is possible to find parts that previous students have done, it is recommended to at least have a look at how they implemented them and if they had problems with them. 

<b> 4. Make Good Relations </b>

This one might seem obvious but is not implemented enough. Try to make as many relations as you can with your classmates, classmates in other sections taking the same course, your TA's, and your Insturctors. Leverage these relations to your advantage by acquiring new knowledge everyday. The people you spend time with shape who you are and shape the base of your knowledge and how you use it to a certain extent. Make sure your friends are as hardworking as you are if not more.

<b> 5. Be Nice </b>

Being kind to your teammates, even when things get tough, is key to building strong relationships and effective teamwork. However, if someone consistently isn't pulling their weight, it's important to talk about it. Starting with a one-on-one chat can help uncover any issues they might be facing and find a way forward together. And if you've tried that and it's still not working, it's okay to bring it up with your instructor or team leader. It's not about blaming anyone; it's about finding the best way for everyone to work together and succeed. By balancing kindness with open communication, teams can overcome challenges and grow stronger together.
