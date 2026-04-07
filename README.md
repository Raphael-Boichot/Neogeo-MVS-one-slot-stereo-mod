A tiny PCB to grab the audio signal from a 1-slot NeoGeo MVS before it enters the amplifier. Restores the stereo signal.

## Why ?
Because the speaker amplifier mount on MVS board is mono only and kind of scratchy / noisy. Remind it was meant to be loud enough on cheap speakers in a room full of people and other machines, not qualified for high end audio circuits like the AES.

## How ?
Just order the PCB and populate with 3.5 mm audio jack plug, 4.7 µF capacitors (25 V) and 6.8 kOhms resistors. A, B and C patches refer to the well known [Jeff Kurtz mod](/Miscellaneous/MV-1FZ_Stereo_Mod.pdf) you should follow. As this mod basically grabs the signal before amplification, it necessitates an additional external amplifier.

![](/PCB/PCB.png)
![](/PCB/Schematic.png)

The PCB was designed to be as small as possible with some clearance around capacitors so that any voltage below 50V must fit.
