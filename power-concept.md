# Power Supply Conceptual Design

** DRAFT **

![PSU Conceptual Block Diagram](img/E920M-PSU-Block.jpg)

The Power Supply will take mains voltage down to an internal regulated 24v. It will provide both line filtering and current protection modules in series with 24v supply. Both current and voltage are sensed. Current sensing is in series, while voltage sensing in parallel with the supply.

Twenty-four volts are distributed to four separate DC to DC secondary supplies (or rails.) Each has both over-current and over-voltage protection. Each has current and voltage sensing. 

The DC to DC secondary supply outputs pass through an output controller to the computer. A separate 5v internal output is supplied for use by other control, instrument and peripheral components.

The Logic Controller recieves all sensing values. It evaluates them against expected behaviour and passes them to an external output. Logic Control also recieves inputs managing the mode of the supplies operation. It manages the output controller's state -  based on both mode and expected conditions.

<br>

<- [Power Supply](power.md)