# Beige-o-Vision's Elliott (GEC) 920M Project Page
![](img/faceplate.jpg)

This is the Beige-o-Vision project page for the Elliott 920M.  It's one of the 900-series of 18 and 12-bit small computers manufactured from the 1960s by the British computer company Elliott Brothers. The 920M is an 18-bit family member. It's compatible with other 920 series members and the 903. This was physically the smallest member of the family. It implemented the full architecture in an aerospace friendly package. Considering the 903 was the height of a bar and about as wide as three kitchen cabinets, this was quite a feat of miniatisation.

## Sections

- [Initial Objservations](initial-observations.md)
- [Modules](modules.md)
- [Background](background.md)
- [Power Supply](power.md)
- [References](references.md)
  
## Plan

UPDATED: It seems we have the basis of an operable system here.  So from our original options, we can strike out parts donor.  While the project isn't a front burner option, we can start gathering the pre-requisite items to make an attempt at power it up.  

### Options Considered

- **Working system**
  The most adventurous would be making it a functional minicomputer. One adventurous owner, Dr. Erik Baigar, already achieved this. His is also the [reference site](http://www.programmer-electronic-control.de/index.html#BIGBROTHER) for publically available information on the system.  You can see his system and his project here: [Elliott 900 Series: The 920M, a rugged 1960ties computer for aerospace and airborne use](https://www.youtube.com/watch?v=v-gF5g0nnoE)
- ~~**Parts donor**~~
  ~~There are a number of other restoration attempts happening at present. The only known parts source for these machines... is other machines.~~
- **Static documentation source** 
  There are no public documents on the system circuitry. A tracing project would be useful for the small user community.
- **Basis for a video**
  Naturally, some kind of Beige-o-Vision video will be in the works, but we won't be attempting to duplicate the valuable work of Dr. Erik Baigar. 
- **Office Ornament**
  Well naturally we wanna keep it where we can look at it!

### Next Actions

1. **Collate all available background information.** Much of this has been published in disparate places.  We'll try and bring it together in a referencable format for our own use.
2. **Collate all available technical information.** Much of this has been put together in disparate places.  We'll try and bring it together in a referencable format.
  - Component mapping
  - Module function and schematic
  - Module level netlisting
  - Interface pinout
  - PSU connection and specification
3. **Investigate key gap areas** Some circuit tracing has already begun Terry Froggatt, but this is not a foreground process for him either. 
4. **Build a monitoring rig for long term use** - This will need to include something like a power management monitoring funtion as well as logic trace function. We have adhoc tools, but a number of systems have had unexpected failures, and the modules largely sealed. Its important to capture data about how the system operates to better understand it.
  - UPDATE 11 Dec 2022: Design of this has started.  It will include an instrumented interface, control panel and instumented PSU.
5. **Build a PSU to Spec** - Intend to use a master AC/DC module with DC/DC modules for each rail probably built into a permanent case with a prototype board, and selectable guages for Voltage and Current.
  - UPDATE 11 Dec 2022: Design of this is ongoing (see page)
6. **Build or Acquire PSU cable to Spec** - The rarity of the plugs is well established.  Milling plugs has been done, but we don't have direct access to this capability at present. 
  - UPDATE 1 Sep 2022: An interfacing cradle was donated to me. This breaks out the small Deutch connectors to more more accessible connectors. A cable compatible with the actual power supply is still required.
7. **Build a Paper Tape / Console interface** - Erik's approach is very appealing but it would be interesting to plan for a much Blicken Light type interface -- if that's possible.
7. **Build or Acquire a PTS Cable** -- As above


## Updates

- **31 Jan 2022** Initial assessment notes in progress here --> [initial observations](initial-observations.md)
- **10 Feb 2022** Been working doing a full inventory of the system modules and configuration --> [Modules](modules.md)
- **2 Mar 2022** 
  - Wrapping up initial work.  
  - Updates [Modules](modules), including the component map.  
  - Added [References](references.md) and made basic conclusion under [Initial Objservations](initial-observations.md).
  - Started a [Background](background.md) page to collate information.
- **Summer 2022** Catalogued and cross referenced modules.  Started building schematics of my own understanding.  This was shared with Andrew Herbert, Erik Baigar and Terry Froggatt.
- **1 Sep 2022** Meet up with Andrew Herbert, Erik Baigar and Terry Froggatt at the National Museum of Computing
  - Terry presented his currnent findings on the system design. 
  - Andrew presented me with an aircraft rear interface cradle to help with interfacing.
- **11 Dec 2022** For the last month or two, I've been working on a power supply design. Takes me a while since I have to learn what I'm doing as I go along!

