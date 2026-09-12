# Bambulabs-Creator-3
A repo containing all the mods I have made to my Flashforge Creator 3 (not pro) to bring it back to life.
THIS REPO IS AN ON-GOING WORK IN PROGRESS!
Treat it as my notepad, where I am writing what I have done to get an ageing FFC3 going again.

<h1>Alternative Slicers</h1>
Flashforge proprietary tools work well, but are dated. I wanted some of the newer more advanced slicer tools that allowed me to tinker with the settings. I found profiles for Ultimaker Cura and Orcaslicer. Neither connect directly over Ethernet, but I only use the USB drive anyway so I haven't chased this far.

<H2>Orcaslicer</H2>
This has been the most successful thus far, I found profiles that worked well from the Orcaslicer Github page, https://github.com/OrcaSlicer/OrcaSlicer/issues/9577.

<H2>Ultimaker Cura</H2>
This worked well, but I moved to Orcaslicer when that worked as I found the interface a lot better, and less buggy in Fedora. *reminder to dig out link and add here*.

<h1>Replacement Hotends</h1>
My printer was a freebie from my work as they could not get replacement hotends, ultimately giving up and going to Bambu Labs printers. Obviously, getting the hotends working again was a major hurdle to overcome, as the prints were pretty awful when it did work, and the nozzles forever clogging.

To resolve this, I decided to look at what printers were out there, and what I could get on Amazon cheaply. I found the X1C hotend to be a particularly good match. It was 24V, and a similar resistance to the FFC3 hotend, and similar length. For $24 AUD I gave it a go and it was surprisingly straightforward to install. All it took was a simple 3D printed adapter, K-type thermocouple, and, using existing hardware it was surprisingly straightforward.

Things I learned along the way:
- Printer is 24V, including the hotend

- Bed homing sensor is piezo
  
- Temperature sensor is a K-type thermocouple
  
- Manual calibration of nozzle height negates the need for the homing sensor

<h2>Method:</h2>
<h3>Parts Required:</h3>

- Bambu Labs X1C 0.4mm hotend (I used this clone from Amazon https://www.amazon.com.au/LEOWAY-Upgraded-Printer-Hotend-Assembly/dp/B0GZF311Z4/ref=rvi_d_sccl_8/355-3859315-9873953)

- K-type thermocouple (bare wire worked for me)
  
- JST-XH 2.5mm 2P receptacle (optional, for heater wire)
  
- 22AWG silicone wire (optional, for heater wire)
  
  - Qty:2 ~90mm lengths worked well for me
    
- Heatshrink sized for above wire (optional, for heater wire)
  
- JST-XH 2.5mm 2P plug and crimps (for thermocouple, 28AWG worked for me but required folding the wire)
  
- 3D printed hotend adapter (ref /hotend/)
  
- 3D printed fan shroud (ref /hotend/)
  
- PTFE tube (I reused one from an old FFC3 nozzle)

<H3>Equipment Required:</H3>
- JST-XH crimp tools

- Soldering iron

- Side-cutters
  
- Hex/Allen keys
  

<H3>Method:</H3>
I'm writing this from memory, so please sanity check as you go.
More importantly, I am merely offering my experience on my FFC3, which has worked well for me. By adapting your own machine with these instructions you do so at your own risk and agree not to hold me responsible. This method worked on my setup, and assuming all are the same, may well work on another setup.

1) Print the hotend adapter.

2) Test the new X1C hotend fits into the square hole.

3) Print the fan shroud.

4) Unload the filament.
5) Turn off the printer!
6) Disassemble the extruder head, and retain all fasteners:
     a) Unplug the servo, heater, thermocouple, bed sensor, and fan
  b) Disassemble the carriage, removing the servo, fan, fan shroud, hotend, and bed sensor
  c) Disassemble the fan shroud. Remove all 4 screws.
7) Install the 3D printed hotend adapter:
8) Install the 3D printed hotend adapter:
  a) Place the bed sensor into the normal position.
  b) Offer up the 3D printer hotend adapter, and make sure the bed sensor isn't obstructed.
  c) Using the same screws from the FFC3 hotend, screw the adapter to the carriage arm.
9) Prepare the X1C hotend:
  a) Extend the wires, or fabricate an extender using the silicone wire, heatshrink, and JST-XH receptacle. I made an extender, so hotend replacement was simplified in future.
  b) Trim the K-type thermocouple wire to match the length of the heater, + adapter/extension.
  c) Install the ceramic heater and thermocouple onto the hotend using the supplied clip. Don't forget to add the thermal paste! One of my hotends came preassembled, so I had to disassemble it first.
  d) Install the silicone boot.
10) Install the X1C hotend:
  a) Bend the top heatsink fins upwards. This serves to stabilise the hotend, kind of like a spring. I used a flathead screwdriver, pushed to the base to encourage a bend. Be very careful not to snap the fins off!
  b) Place the PTFE tube into the bed sensor, and trim just shy of the base of the sensor. This took some guesswork, too short and the filament can snag when fed in, too long and the bed sensor doesn't register and the hotend may not fit.
  c) With the PTFE tube in place, install the X1C hotend. Use the qty:2 lower screws from the fan shroud we disassembled earlier and push the into the hotend adapter, and through the two hotend mount holes, until the screw heads are flush. My print of the adapter meant I had some thread bite and they stuck in well. You may have to push the hotend up a little depending how far the fins were bent.
  d) Connect the heater and thermocouple wires to the carriage PCB.
11) Install the fan and shroud, using the remaining qty:2 screws removed from the fan shroud earlier.
12) Connect the fan to the carriage PCB.
13) Reinstall the servo and direct drive mechanism.
14) Tidy-up!

Once installed, I ran a manual calibration of the Z-axis. Manual calibration is an option lower in the FFC3 settings page, and once enabled you run calibration as per normal, but manually setting the nozzle height using an A4 piece of paper.
So far, this has worked well and I went on to swap the second hotend, and ran a full calibration and bed level (manual in Z).
Print away!
