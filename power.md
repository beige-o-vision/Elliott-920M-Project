# Power Supply 

** DRAFT **

The Elliott 920M needs a custom power supply. 

The computer was originally an embedded system with an application specific power supply. It was targetted for aerospace.  The power supplies originally built for it were compatible with the aircraft's power systems. Even if an original power supply were available, it wouldn't be compatible with the domestic power supply available in a home, office or museum. 

We don't have experience designing power supplies -- so this is going to be a bit of a learning experience. As with any technical design, we'll follow a basic product development process. 

**Requirements -> Approach -> Conceptual Design -> Technical Design -> Development -> Test -> Manufacture -> Fix/Remediation**

<br>

## Sections

- [Requirements](power-reqs.md)
- [Approach](power-approach.md)
- [Conceptual Design](power-concept.md)
- [Technical Design](power-design.md)
- [Development](power-dev.md)
- [Testing](power-test.md)
- Manufacture
- Fix / Remediation

<br><br>

## Additional notes

- Power status signals to the computer:  Any logical system status will come from the main system controller based on monitoring the power supply. 

  - Power good?
  - other?

  <br>

<- [Home Page](index.md)
