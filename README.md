**A tiny PCB to grab the audio signal from a 1-slot NeoGeo MVS before it enters the amplifier. Restores the stereo signal.**

## Why ?
Because the speaker amplifier mount on some MVS boards is configured in mono only and kind of scratchy / noisy even after recap. Remind that it was meant to sound good enough on cheap cabinet speakers in a room full of chating people and loud playing machines, not exactly the same comfy conditions as in your living room.

## How ?
Just drop the gerber for example on [JLCPCB](https://jlcpcb.com/) website (any thickness, any finish, the cheaper the better) and populate the board with a 3.5 mm audio jack plug, 4x4.7 µF capacitors (any voltage, it's low level signals) and 4x6.8 kOhms resistors (any type). A, B and C patches refer to the well known soldering points from the [Jeff Kurtz mod](/Miscellaneous/MV-1FZ_Stereo_Mod.pdf) I just followed. Take the GND where you want, there are plenty of different possibilities. As this mod basically grabs the signal before any amplification, it requires an additional external amplifier.

![](/PCB/PCB.png)

The mod also necessitates permanent modifications to your MVS slot and you will permanently lose sound from the JAMMA comb. The jack directly goes to your prefered amplifier by completely bypassing the usual cabinet / supergun sound circuit. The PCB was designed to be as small as possible with some clearance around capacitors so that any voltage below 50 V must fit.

I guess that an SMD version is totally possible but considering the usual clearance around a consolized MVS motherboard, who cares. Just ask politely in case you need one.
