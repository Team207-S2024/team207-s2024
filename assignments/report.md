<h1><b> EGR 314 Report </b></h1><br>

<p align="center">

  <b> Portable Weather System </b><br>

  <b>Team 207</b> - <i>Atmos-Gear </i><br>

  <b>Members:</b> Isaac Linares, JJ Sales, Manuel Garcia, Michaela De Angelis Werner<br>

  <b>Date Created:</b> 01/23/2024<br>

  <b>Date Updated:</b> 1/25/2024<br>

  <i>ASU Polytechnic, EGR 314, Travis Kelley</i><br>
  
</p>

# Table of Contents

1. [Team Organization](#team-organization)

2. [User Needs](#user-needs)

3. [Design Ideation](#design-ideation)

4. [Selected Design](#selected-design)

5. [Block Diagram](#block-diagram)

6. [Component Selection](#component-selection)

7. [Microcontroller Selection](#microcontroller-selection)

8. [Hardware Proposal](#hardware-proposal)

9. [Software Proposal](#software-proposal)


## Team Organization

The following subsections will detail our process for the team charter and mission statement. For the sake of
succinctness, everything else is consolidated into the appendix.

Refer to [Appendix A: Team Organization Assignment](teamorganization) 
for further information about our team organization and team decisions.

### Team Charter

The team decided on the charter fairly late but eventually came to an agreement on what everyone wanted
for the group in terms of personal goals.

_Our goal is to gain knowledge in digital circuits that utilize serial communication. 
We as a team want this product to be compared to other professional-grade devices being sold on the market._

### Mission Statment

After talking with each other about one another's interests, the team began to determine what the project
needed to have as well as what each individual member wanted it to have. 

_The mission of the team is to create a sensor-based weather reporting product that is unique, portable, 
professional, reliable, and user-friendly. It is something that should be focused on that a person can easily
use and install themselves and is relatively simple to collect data from, along with contingency plans in case things go awry._

## User Needs

The team worked exceptionally hard at identifying and deciphering the user needs necessary for a successful project, which included research into similar products that used the name of what the project is as tags. Each team member created at least one setup for a product and 3 positive/negative reviews for each product, with comments on what user needs that could be derived from each review. Once each member was done, members contributed to a Jamboard with each user need deriving from the research as well as ideas that members came up with. It involved multiple days of back and forth, from creating to grouping to ranking the needs. Finally, the user needs were consolidated into an easy-to-read table ranked all together. 

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

Refer to [Appendix B: User Needs and Benchmarking Assignment](userneeds-benchmarking)
for further information, the content of the VOC research, and the final table derived from the work. 

The PRD (Product Requirements Document) was developed soon after, which involved creating unique scenarios for a potential product in order to generate further ideas as well as brainstorming potential stakeholders and what each person wanted from the project. Open questions were also developed that can hopefully be answered as the product develops. 

Refer to [Appendix C: Product Requirements Document Assignment](productrequirements)
for further information about the brainstorming the team did for this assignment, including the stories and aspects created.

## Design Ideation

The design ideation process involved looking back at the user needs, turning them into functions a product could have, and putting them onto a Jamboard for a visual representation. Once finished, people grouped them according to an overall general functionality. Finally, people developed 3 distinct ideas in order to figure out a concrete idea going forward.

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

The GPS Plus Cat Collar (Name Subject to Change) is a cat collar with sensors for humidity and temperature installed onto it, as well as a location tracker. The purpose of the device is to see where feral/outdoor cats go to keep warm and dry/comfy. How it works is you capture a feral/outdoor cat, put the collar on, and then let them free. It will then begin autonomously tracking the cat and where it goes, namely its most common hideouts. Then, when the cat gets near the ‘home base’ (as in, when the collar can connect to a server through Wifi), it will then transmit what data it stored onto the server in a readable format, by parsing through the sensor/tracking data. If in the event where the user doesn’t want the cat to wear the device anymore, and it's in the area, they can put out a radio/Wifi signal that will unlock the collar through a motorized locking system. 

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

This device would feature a sensor that can detect temperature and humidity levels which would then send data over to the stand, the stand, which is controlled by a motor mechanism would then move the plant sitting inside the pot to the optimal position to either increase or decrease the received sunlight by the plant. The device could also send over data via wifi to alert the user of weather conditions such as temperature and humidity and update the user on the life of the plant.  

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/eae8ae64-4bde-4a5f-b422-1e579a1550ce" />
</p>

<p align="center">
  <i>Figure 8: Solidworks Drawing of a Temperature Sensor for Optimal Sunlight</i>
</p>

Refer to [Appendix D: Design Ideation Assignment](designideation)
for further information about the design ideation process.

## Selected Design

The selected design was [Optimal Sunlight for a Plant](#optimal-sunlight-for-a-plant), but expanded upon. For one, the movement of the plant was decided to be put on a belt-like system, where it would move along on a platform placed on treads based on the temperature/humidity sensors. It would also move to and from a shaded area based on a comparison of the sensor data. For the temperature, it would check the temperature of the area, and determine whether it would be too hot or too cold for the plant. For the humidity, it would check the soil for if it was too wet or dry, and move based on that data. In addition, it was determined a good way of utilizing the ESP32 requirement would be to signal over WiFi if the plant needed watering or not. 
The plan is for this to not only be mobile in terms of the device moving something but also be lightweight enough for a user to position this where they need to as well as using batteries so it doesn't need to be tied down anywhere. 

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/d09de321-f589-4fb7-b789-d27ac7dd7ec7" />
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

Refer to [Appendix E: Selected Design](selecteddesign) for further information about the selected design.

## Block Diagram

Once the team decided on a concept to move forward with, it became time to determine how the entire project would fit together within the technical requirements of the project. Thus, the group created a block diagram to hash out a basic concept of how everything would fit together on a technical level. It began with a rough idea, but once components were selected and finalized, the group was able to select what pins were necessary for each component to communicate with one another, as can be seen below.

During this point, each team member chose their assigned subsystem. The choices were as follows:

**Isaac Linares:** Humidity Sensor 

**JJ Sales:** Temperature Sensor

**Manuel Garcia:** Motor Driver/Motor

**Michaela De Angelis Werner:** Microcontroller/Power Supply

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/157151171/3dd5a8ab-1391-4818-83de-0e93be987333" />
</p>

<p align="center">
  <i>Figure 10: Current Block Diagram of the project. </i>
</p>

Refer to [Appendix F: Block Diagram](blockdiagram) for further information, such as a step-by-step breakdown of each component and its overall function within the project.

## Component Selection

As soon as the block diagram was finished, the team began considering what components were needed to fill in the gaps. Each team member studied their assigned subsystem and picked a series of main components that each subsystem critically required. From there, the team member would choose which component out of the lists would be the best fit for this project. The chosen components for each subsystem are as follows:

<p align="center"> Choice for Battery: Amazon Basics 2-Pack 9 Volt Lithium High-Performance Batteries, 10-Year Shelf Life, Long Lasting Power </p>

Rationale: The group chose this because even though there isn't a datasheet to help determine capacity, based on being a lithium battery with stellar reviews and similar products being of the necessary capacity, it seemed like a good enough risk to take. Note that this will be for regular use, and the group may utilize other batteries over the course of the testing phase to see how it can work.

<p align="center">  Choice for Regulator: LM2575D2T-3.3R4G </p>

Rationale: The class used the through-hole version of this component for a prior ICC, so it would be beneficial to be able to use that knowledge going forward as much as possible. Although it wasn’t the surface mount version, it stands to reason the same circuit should theoretically work.

<p align="center"> Choice for Motor Driver: IFX9201SGAUMA1 </p>

Rationale: This motor driver was provided for us in class and would provide less of a learning curve, in terms of operation and coding itself. The IC itself would take less time to solder because there are less pins on the layout. 

<p align="center">  Choice for Motor: 114090046 </p>

Rationale: This motor provided all the optimal specs for our specific application and was reasonably priced compared to all the other available motors. The compact shape also would help with mechanical design of the project. This Motor also offers a higher torque value compared to all the other DC motors and is great for pulling heavy loads, which is required for our application.

<p align="center">  Choice for Humidity Sensor: Honeywell Sensing and Productivity Solutions HIH6030-021-001 </p>

Rationale: This humidity sensor was in stock, was I2C compatible, and seems relatively easy to solder and use. It has a typical application circuit and a decent datasheet to work with.

<p align="center">  Choice for Temperature Sensor: TC74A4-3.3VCTTR </p>

Rationale: This temperature sensor was used in class, so there's a surplus of knowledge and reusable code that the group can utilize. 

### Power Budget

The team also began work on the power supply for the system, with mixed results. Due to a mixture of paltry information about batteries as well as a less than perfect iteration of the calculator used, the results are not as good as they could be. 

<object data="images/componentselection/PowerBudget207.pdf" width="1000" height="1000" type='application/pdf'/>

<p align="center">
  <i>Figure 11: Current Power Budget of the project. </i>
</p>

Refer to [Appendix G: Component Selection](componentselection) for further information, such as the full list for each subsystem and its components.

## Microcontroller Selection

The microcontroller selection was done soon after the component selection. The process was incredibly tedious and confusing at the time, given that there were some questions regarding terminology and just how many serial communication pins were necessary. Overall, though, the search was an enlightening one and made the group more knowledgeable about the differences between the microcontrollers available. 

Eventually, the group decided to go forward with the PIC18F26K40, for many reasons. For one, it will be a significantly nicer time to solder its 28 pins versus the competition's 40-64 pins. In addition, many previous groups had success with it, meaning that in the chance that help is necessary, the group can find it through previous students. Finally, the extensive documentation and the large datasheet will be critical when it comes to working with it hardware and software-wise. 

Refer to [Appendix H: Microcontroller Selection](microcontrollerselection) for further information.

## Hardware Proposal

Soon after, it was time to begin putting everything together. At first, each member took the time to create their own subsystem's circuit according to not only their datasheets but also prior knowledge of using certain components. Next, they were compiled into one schematic, getting a good idea of where each pin would go with regards to each other system. Finally, the team took care in organizing the subsystems and various subcircuits in a way that could flow decently. 

<p align="center">
  <img src = "https://github.com/Team207-S2024/team207-s2024/assets/156377035/77cbff77-dcc5-4553-9823-f4c0480f66fd" />
</p>

<p align="center">
  <i>Figure 12: Current Schematic of the project. </i>
</p>

### Bill of Materials

The group also finalized the bill of materials for the project for the purpose of sending out a purchase request. The first iteration of the purchase request was not perfect, but it was revised as soon as it could be. 

<p align="center">
  <i>Figure 13: Current Bill of Materials for the project. </i>
</p>

Refer to [Appendix I: Hardware Proposal](hardwareproposal) for further information, such as a full breakdown of the schematic, including each subsystem and circuit.

## Software Proposal

Refer to [Appendix J: Software Proposal](softwareproposal) for further information.
