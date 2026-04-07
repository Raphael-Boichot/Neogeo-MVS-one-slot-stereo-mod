**A tiny PCB to grab the audio signal from a 1-slot NeoGeo MVS before it enters the amplifier. Restores the stereo signal.**

## Why ?
Because the speaker amplifier mount on MVS board is mono only and kind of scratchy / noisy. Remind it was meant to be powerfull enough on cheap speakers in a room full of people and other machines, not exactly the same conditions as in your living room.

## How ?
Just order the PCB for example at [JLCPCB](https://jlcpcb.com/) (any thickness, any finish, the cheaper the better) and populate with a 3.5 mm audio jack plug, 4x4.7 µF capacitors (25 V) and 4x6.8 kOhms resistors. A, B and C patches refer to the well known [Jeff Kurtz mod](/Miscellaneous/MV-1FZ_Stereo_Mod.pdf) you should follow. Take the GND where you want, there are plenty of different possibilities. As this mod basically grabs the signal before amplification, it requires an additional external amplifier.

![](/PCB/PCB.png)

The mod also necessitates permanent modifications to your MVS slot and you will permanently lose sound from the JAMMA comb. The jack directly goes to your prefered amplifier by completely bypassing the usual cabinet / supergun sound circuit. The PCB was designed to be as small as possible with some clearance around capacitors so that any voltage below 50 V must fit.
