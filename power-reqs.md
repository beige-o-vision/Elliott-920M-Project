# Power Supply Requirements

** DRAFT **

## A. Do no harm

It's old, and potentially grumpy. There are no reliable source of spared. We need to be very protective of it if the computer is to be more than ornamental.

<br>

## B. Learn something

Get as much information from the system as we can, even in creating a power supply.

<br>

## C. Power Rails Requirements

Rails and currents per Erik Baigar:

- +18V@2A 36w
- +12V@1A 6w
- +5V@6A 30w 
- -5V@1A 5w

<br> 

## D. Instrumentation 
Show both what the load and supply are doing, and feed the information to an overall instrumentation solution.  This is partly for documentation, and partly to provide the basis for automation

<br>

## E. Automation 

Control of both routine processes and to ensure protection of the load (the computer). 

Routine processes include:

- Power sequencing
- Enabling and disabling computer power separate from overall system which includes simulated peripherals, control and instrumentation.
- Control panel functions

Exceptional processes include:
- Problem detection
- Power disconnect under fault conditions.

<br>

## F. Load protection

- Over current protection for each rail
- Over voltage protection for each rail
- Anomolous condition detection and disconnect (eg. under voltage, unexpected load patterns, etc.)


<br>

<- [Power Supply](power.md)