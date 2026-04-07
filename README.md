**A tiny PCB to grab the audio signal from a 1-slot NeoGeo MVS before it enters the amplifier. Restores the stereo signal.**

## Why ?
Because the speaker amplifier mount on MVS board is mono only and kind of scratchy / noisy. Remind it was meant to be loud enough on cheap speakers in a room full of people and other machines, not qualified for high end audio circuits like the AES.

## How ?
Just order the PCB for example at [JLCPCB](https://jlcpcb.com/) (any thickness, any finish, the cheaper the better) and populate with a 3.5 mm audio jack plug, 4x4.7 µF capacitors (25 V) and 4x6.8 kOhms resistors. A, B and C patches refer to the well known [Jeff Kurtz mod](/Miscellaneous/MV-1FZ_Stereo_Mod.pdf) you should follow. As this mod basically grabs the signal before amplification, it necessitates an additional external amplifier.

The mod also necessitates permanent modifications to your MVS slot, so be careful.

![](/PCB/PCB.png)
![](/PCB/Schematic.png)

The PCB was designed to be as small as possible with some clearance around capacitors so that any voltage below 50V must fit.
