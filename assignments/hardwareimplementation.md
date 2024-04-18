# Hardware Implementation

## Hardware Implementation

The hardware implementation of the project included development of the team PCB as well as any edits that had to be made.

One of the most significant changes made between the original team PCB and the final team PCB was that the motor driver's SO and SI pins had to be changed in order to properly function- effectively, the microcontroller was sending an input into an input, instead of sending an input into an output. That made it so it couldn't get the exchange of bits necessary to move the motor. 

One change that should have been made but wasn't was the swap between the ESP32's VIN power pin and 3V3 power pin, which was due to a misunderstanding and less than accurate information found online. When the ESP32 is plugged into a computer via USB, it can output either 5V or 3.3V out of the respective pins. However, when it isn't plugged in, VIN and 3V3 turn into alternative power pins to plug the respective voltages into. Unfortunately, by the time the final PCB was printed, it wasn't realized that it was necessary to swap the 3.3V power plane going into VIN to instead go into 3V3. This was fixed by simply fly-wiring (as in, connecting the ESP32 to the board through male-to-female wires) and swapping where the voltage would go. 

## Final Team PCB
<Insert Image + Turnaround 3D Model Here>
