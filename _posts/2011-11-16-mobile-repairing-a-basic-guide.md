---
layout: post
title:  "Mobile Repairing: A Basic Guide."
date:   2011-11-16 23:04:00
categories: guide mobile
---

In this post, I am going to share some basic knowledge about mobile Troubleshooting. Note that this post is targeting non-technical audience and therefore will not go in-depth of mobile repairing.

## Building blocks of a mobile

Let's start with some components of a mobile and some tools we use to troubleshoot one. Essential elements of a mobile are:

1. *Battery:* Battery is the power source of a cell phone.
2. *Keypad:* Keypad (push button) is an input device of a mobile phone and is used to give input to the phone. Now a day’s mobile phones have touch screens where there are no keys, but a user can provide input by just touching the screen. It can be of two types:
    * Resistive type: In which touch works from changing of resistance which gets changed when we hit the screen.
    * Capacitive type: In this type when a user touches the screen the capacitance of that part got changed and hence it works according to those changes.
3. *Speaker:*    Speaker is an output device of a mobile phone, which is used for giving hearing outputs.
    In an ordinary mobile there are two speakers:
    - Earpiece: just a small speaker which doesn't produce loud sounds.
    - Ringer: A speaker capable of producing loud sounds. (Generally, a separate ringer IC is used for a ringer speaker)
4. *Display:* Display is also an output device of mobile phone used for giving visual outputs.
5. *Chips and IC’s:* In a mobile, there are large number of chips and IC’s like CPU. Some of them are Power IC, Frequency Filter IC, Ringer IC, etc.
6. *PCB (Printed Circuit Board):* PCB is printed circuit board which is a non-conductive hard platform of a Mobile where all the devices are assembled, and the reason it is called a circuit board is that it have connections on its surface. Nowadays, there are different types of PCB, main are TWO layer PCB and THREE layer PCB. A *two* layer PCB have circuits printed on its upper and lower side whereas a *three* layer PCB have an advantage of having printed circuit also in the middle.

## Mobile Repairing Tools

Some essential tools used for mobile repairing are:

1. *Multi Meter:* (VOM) is a measuring instrument. A multimeter has features like measuring voltage, current, resistance, and continuity. It is used for measuring the correctness of the devices.
2. *Soldering Iron:* Soldering Iron is used for connecting the broken connections or wires. For soldering one always need a Soldering Wire, and on your choice, you can also use Solder paste (It is used to connect the leads of IC packages to attachment points in the circuit PCB)
3. *Toolkit:* One will always need a small kit for repairing a Mobile phone. An ideal kit at least contains some screwdrivers (different sizes),  holders,  multimeter, etc.



Now after knowing the building blocks and tools, let's see some common faults in an average mobile phone.

## Common faults


1. Power Supply: This is a problem when the mobile phone is not getting a proper power supply. Some common reasons are:
    - Dead battery
    - The changed battery may have the same voltage value but different current value OR vice-versa
    - Shorting somewhere in the wires which also leads to the same problem.
    The best way to correct such a problem is first to check for the correctness of the battery and if it is correct then check for the shorting part.
2. Speaker Problem: This is a common problem that the speaker doesn't work. For this, we first check for the correctness of the Speaker with the help of the multimeter. We set the multimeter in continuity direction and test the speaker’s both ends for both directions. If we get Beep sounds in both the direction, that means that the Speaker is functioning properly, but if we don’t get Beep sound from both sides, then it implies that the speaker is not working. And then the easiest way for a beginner is to change the speaker with a new one.
3. MIC Problem: Another common problem in mobile phones is MIC NOT working problem. For testing a MIC, we again set the multimeter to continuity or 20 V and then check the MIC’s both ends in both directions. Then we must get a beep from other side and not from its reverse direction, if it is so, that means that MIC is correct and the problem is somewhere else. Otherwise, change the MIC with a new working one.
4. Keypad problem: Sometimes some keys of a keyboard won't work. For this, we first check the faulty buttons as there might not be any carbon left under the key, we must remove that and check then. Otherwise, we check continuity of the circuit related to the keys.

## My experience with fixing **Nokia 1112**

Well, that's all for the mobile phone troubleshooting post. And now I am writing my personal experience of repairing a mobile phone, which I have troubleshot for my project in a Hardware Course.

**Problem:** The phone has dropped in water by mistake around a month ago, and it's MIC and speaker were not working at all, and some part of the display was also not clear, and some keys were also not working.


**Repairing:** First of all, to start with the troubleshooting part, I opened it. I opened it with care because if we press the screw forcibly while opening, then it may result in cracks in the PCB or can also lead to some other kind of fault.

After opening the body, first of all, I opened the speaker and tested its correctness as mentioned above. There I found that it was only giving beep sound in one direction. This means that the Speaker was dead. And when I took the speaker out of the phone, I found that there was corrosion.

Then I checked for the MIC, and it was giving beeps in both directions. This means that it was also a faulty MIC.

After that, I checked for the keys, and I found that there was carbon on the points, so I cleaned the carbon between the keys and PCB, and after that, I washed it with thinner and then it was working correctly.

And then I checked for the Display problem, so I found that there was water in the screen. And also some connections were got loosened. I took a small soldering Iron and solder all the loose points with the help of soldering wire.

After this, I purchased a speaker and a MIC and tested both of them, and they were working properly. Then I put them in their places. But even then the loudspeaker wasn't working. So I  once more opened the Mobile and this time I started testing for the connection of the Ringer speaker. There the two possibilities were that the ringer IC is not working, or maybe the connection is broken somewhere.

And then I opened the cover of the protected region and checked the connections with the help of a multimeter by setting it to Continuity. And I found that all the connection were right.

So I checked for the upper part where Speaker is connected, and that part was also correctly working. So, I concluded that the ringer IC was NOT working.
I was unable to do anything for the IC part because we don't touch IC's with our hands.
Finally, I successfully troubleshot the MIC, speaker (earpiece), display and keys of the phone.
