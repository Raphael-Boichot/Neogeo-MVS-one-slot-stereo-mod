**A tiny PCB to grab the audio signal from a 1-slot Neo Geo MVS before it enters the amplifier. Restores the stereo signal.**

## Why ?
Because the speaker amplifier mount on some MVS boards is configured in mono only and kind of scratchy / noisy even after recap when passing through a high/low impedance adapter (typically on a supergun), this mod allows you to extract the sound signal in stereo before any amplification and use your own sound amplification system.

Read until the end if your problem is just about sound quality out of a supergun and mono is just fine for you.

## How ?
Just drop the gerber for example on [JLCPCB](https://jlcpcb.com/) website (any thickness, any finish, the cheaper the better) and populate the board with a 3.5 mm audio jack plug, 4x4.7 µF capacitors (any voltage, it's low level signals) and 4x6.8 kOhms resistors (any type). A, B and C patches refer to the well known soldering points from the [Jeff Kurtz mod](/Miscellaneous/MV-1FZ_Stereo_Mod.pdf) I just followed. Take the GND where you want, there are plenty of different possibilities. As this mod basically grabs the signal before any amplification, it requires an additional external amplifier.

![](/PCB/PCB.png)

The mod also necessitates permanent modifications to your MVS slot and you will permanently lose sound from the JAMMA comb. The jack directly goes to your prefered amplifier by completely bypassing the usual cabinet / supergun sound circuit. The PCB was designed to be as small as possible with some clearance around capacitors so that any voltage below 50 V must fit.

I guess that an SMD version is totally possible but considering the usual clearance around a consolized MVS motherboard, who cares. Just ask politely in case you need one.

**BUT...**

## Do you want to try a non destructive (and easy) mod before ?
If you are using an SNK MVS board with a Supergun equipped with a high/low impedance adapter, you’ve likely encountered the "un-tunable" audio symptom. Because the MVS onboard amplifier expects a physical speaker load of 8 Ohms per channel (5 Watts speakers), running it into a high-impedance adapter results in a near-infinite output impedance. When you try to adjust the volume via the MVS PCB potentiometer, the audio behaves erratically. It jumps from a constant hiss at low levels to harsh clipping with just a fraction of a turn. It feels impossible to find a "sweet spot" for the external amplifier.

**The Fix is just a dummy Load.**

To stabilize the signal, you simply need to simulate a moderate load before the high/low adapter. I found that adding approximately 25 Ohm of resistance significantly cleans up the output and restores linear control to the volume pot. I used for example 2x47 Ohms (1W) resistors wired in parallel (totaling  approx. 23.5 Ohms) because I had them in my drawers. This value is high enough to prevent the resistors from overheating, yet low enough to "drain" the amp output effectively.

Connect the resistors to the JAMMA comb between the audio pins (Pin 10 and/or Pin L) and ground. While this won't fix the low-quality audio hardware found on Chinese "1XX-in-1" bootlegs, it makes genuine boards sound better. The audio is much closer to the original arcade cabinet experience, and the onboard volume slider / potentiometer finally works across its entire range without clipping or distortion. This resistance is high enough that you can leave the mod in place even if you eventually switch back to a real low-impedance arcade speaker setup.

![](/My_setup_for_dummy_load.jpg)

Example of a dummy load (2x47 Ohms in parallel, mono configuration) on a SmallCab Supergun Deluxe 2. Note that you must use the RCA outputs for audio; the jack plug bypasses the specific pins used for this load. Be sure to cross-reference your own supergun schematic before replicating this.
