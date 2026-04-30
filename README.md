**A tiny PCB to grab the audio signal from a 1-slot NeoGeo MVS before it enters the amplifier. Restores the stereo signal.**

## Why ?
Because the speaker amplifier mount on some MVS boards is configured in mono only and kind of scratchy / noisy even after recap when passing through a high/low impedance adapter (typically on a supergun), this mod allows you to extract the sound signal in stereo before any amplification.

Read until the end if your problem is just about sound quality and mono is fine for you.

## How ?
Just drop the gerber for example on [JLCPCB](https://jlcpcb.com/) website (any thickness, any finish, the cheaper the better) and populate the board with a 3.5 mm audio jack plug, 4x4.7 µF capacitors (any voltage, it's low level signals) and 4x6.8 kOhms resistors (any type). A, B and C patches refer to the well known soldering points from the [Jeff Kurtz mod](/Miscellaneous/MV-1FZ_Stereo_Mod.pdf) I just followed. Take the GND where you want, there are plenty of different possibilities. As this mod basically grabs the signal before any amplification, it requires an additional external amplifier.

![](/PCB/PCB.png)

The mod also necessitates permanent modifications to your MVS slot and you will permanently lose sound from the JAMMA comb. The jack directly goes to your prefered amplifier by completely bypassing the usual cabinet / supergun sound circuit. The PCB was designed to be as small as possible with some clearance around capacitors so that any voltage below 50 V must fit.

I guess that an SMD version is totally possible but considering the usual clearance around a consolized MVS motherboard, who cares. Just ask politely in case you need one.

BUT...

## Do you want to try a non destructive (and easy) mod before ?
Assuming you're using a supergun equipped with a high/low impedance adapter (and your own amplifier after), the MVS board amplifier spits signals with basically zero load (near infinite output impedance). In that case when you try to tune the sound level with the potentiometer on the MVS PCB, sound goes from noisy as shit with constant hum but stable to scratchy as shit but without hum in a fraction of tuning angle. Basically: impossible to find a good matching with your own sound amplifier.

I found that just simulating a moderate load with a 50 ohms resistor **before** the high/low impedance adapter improves a lot the sound quality. The only "difficulty" is to find the soldering points on your supergun jamma comb to avoid altering the MVS board (typically pin 10 and L to ground through two 100 ohms resistors in stereo or one of them to ground with a 50 ohms resistor in mono). 50 ohms load is high enough to drain the amplifier output and small enough to avoid any kind of resistor overheating. Other values are probably possible but I took in my case 2x100 ohms simply because I had them in my drawers in 1W. Also 2x100 ohms is high enough resistance to let the mod in place in case you switch to real low impedance arcade speakers.

This of course does not suppress the sound artifacts of some Chinese bootlegs and other 1XX-in-1 cartridges, but at least makes the sound output more enjoyable (I guess close to a genuine arcade cabinet) and the tuning from the PCB potentiometer possible on the whole scale. 
