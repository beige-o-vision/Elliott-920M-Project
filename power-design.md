# Power Supply Technical Design

** DRAFT **

The power supply will ultimately live an enclosure along with a control panel, system controller and peripheral emulators. The current idea is this will appear similar to the control panel of a 920C or 903. A multi-voltage power cable will connect to the aircraft computer mounting cradle. 

## Performance Specification

Our target performance is average current capacity, plus 33%.  The system will current protected at average rating plus 15%. Power rails should provide full rated voltage +/- 5%. Over voltage protection should be triggered at +10%

### 5 volt rail

- Average Current Rating: 6A
- Peak Current Rating: 8A
- Over Current Threshold: 6.9A
- Over Voltage Threshold: 5.5V

### -5 volt rail

- Average Current Rating: 1A
- Peak Current Rating: 1.3A
- Over Current Threshold: 1.2A
- Over Voltage Threshold: 1.1V

### 12 volt rail

- Average Current Rating: 1A
- Peak Current Rating: 1.3A
- Over Current Threshold: 1.2A
- Over Voltage Threshold: 13.2V

### 18 volt rail

- Average Current Rating: 2A
- Peak Current Rating: 2.7A
- Over Current Threshold: 2.3A
- Over Voltage Threshold: 19.8V

<br>

## Physical Specification

The power supply will physically contain five elements: 

- Mains Filter (includes input connector and power switch)
- AC/DC adapter: off the shelf internal AC/DC adapter
- PSU main/control board: host multiple modules and interconnect all internal PSU components  
- Output control module: power relay module
- Output power header: chassis mounted power distribution to cabling board

These elements will be made up of the following components:

<br>

## Components

### 1. Logical Control

Control logic will be provided by an Atmel ATmega328P. The control code is being prototyped on an Arduino Uno R3. 

- **External Inputs**: The controller takes a 2-bit digital input. This will be a pin header on the control board. It represents the disired mode of operation. The input will come from the system control panel.
- **External Output**:
  - *Serial Output*: The controller will provide a serial data stream to a an RS232 pin header on the control board. Packages of sample and status information will be posted on that interface. 
  - *OLED display*: The controller will connect to a I2C pin header on the control board. The header will also supply power to a OLED display module. The module will display of a grid of the current sampled data.  In case of exception conditions the display with flash by inverting its output, either by field or on the whole display.
- **Internal outputs**: The controller provides a 3 signal selection output to the output controller. It also provides a 3 signal selection output to each of the analogue signal multiplexors (74HC4051).
  - *Internal inputs*: The Atmel microcontroller read voltage reference, an analogue current signal and analogue voltage signal. Each input analogue signal comes from a 74HC4051 mux chip. Using the mux chip channel selction, it scan voltage and current input channels connected to the current and voltage sense modules. These 74HC4051s also reside on the main control board.
  - *Output Control*: The output control module will be an Elgoo 4-channel relay module. This module will take control signals from the Atmel microcontroller, and DC outputs from each of the power rails.

<br>

### 2. Mains Filter

*TBC* - This will be a panel mounted combination power switch, filter, fuse and input lead module.

<br>

### 3. Mains Current Protection

A mains fuse is provded as part of the filter module. 

<br>

### 4. AC/DC Supply

An overspec, off the self power supply will provide the main internal voltage at 24v.  That module used is a:

  TDK-Lamda RWS-300B-24 AC/DC Enclosed Power Supply (PSU), ITE, 1 Outputs, 300 W, 24 V, 12.5 A

<br> 

### 5. Current Sense

ACS712 hall current sense chips are adapted from generic modules to a riser board package. There are five copies of this riser board -- one for each sensed current source.

<br>

### 6. Voltage Sense

This is a single custom riser board containing voltage dividers for each of the power rails.  It contains a OpAmp chip and precision variable resistor to enable negative rail voltage sensing in positive voltage analogue domain. And it also contains the voltage reference.

<br>

### 7. *5v DC/DC Supply

This is riser module with an external trim pot allowing voltage adustment. The selected module is:

  MEAN WELL  NID100-5  Non Isolated POL DC/DC Converter, ITE, 1 Output, 55 W, 5 V, 11 A, Fixed, Adjustable

All DC to DC modules output to the output control module through a screw terminal head via a current sense module. This 5volt module also connects to a control board pin header supplying 5v to other modules in the system.

<br>

### 8. -5 DC/DC Supply

This is riser module with supporting circuitry on the controller board to derive a negative voltate. It uses the same riser module as the 5v supply, although this is substantially overspec. An additional trim pot allows voltage adustment. 

The selected modules is:

  MEAN WELL  NID100-5  Non Isolated POL DC/DC Converter, ITE, 1 Output, 55 W, 5 V, 11 A, Fixed, Adjustable

All DC to DC modules output to the output control module through a screw terminal head via a current sense module.

<br>

### 9. 12v DC/DC Supply

This is riser module with an external trim pot allowing voltage adustment. The selected module is:

  CUI P783F-Q24-S12-S Non Isolated POL DC/DC Converter, ITE, 1 Output, 36 W, 12 V, 3 A, Fixed, Adjustable

All DC to DC modules output to the output control module through a screw terminal head.

<br>

### 10. 18v DC/DC Supply

This riser module combines a generic variable voltage buck-converter module with an riser adapter.

All DC to DC modules output to the output control module through a screw terminal head via a current sense module.

<br>

<- [Power Supply](power.md)