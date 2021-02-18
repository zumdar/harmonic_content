# notes on progress
### 2.2 work in shop

control voltages are usually -5 to +5V.. teensy can only do 0-5.. how to solve that?

- check out CV schemes for modules
- maybe could alter teensy or change groun ref or make modules do 0. - 5
- look at microprocessor section in the **prophet 5** on how they did it!
- Z80

[2_2_2021.mov](2_2_2021.mov)

### 2.3

lots of chatter in the [forum](https://www.muffwiggler.com/forum/viewtopic.php?f=17&t=244045 "forum") about the project
people suggesting just the teensy for this project
[axoloti](http://axoloti.com/) is a cool project that might be perfect for this

- First of all it is essential to have a solid port for note-inputs, with low latency and ideally no jitter.
- I would use one dac for each cv. At least 16bit, better 24 for fidelity. Everything else would be a compromise.
- If you want a rocksolid poly, you need adcs for tuning and autocalibration.
- Solid psu, grounding and separated digital and analog boards against noise.
- The openness, future-proofness, you are not sure where this is going to lead you, the complexity in general, the variety of high level interfaces such as gesture-control or wifi, the universality of usage (polysynth, art installations) and the easy acsessibility for other students in the future, make me wonder why you want to restrain yourself with a developer-board or microcontroller instead of using full-blown computers?
- You should do a list of priorities and compromises for you project. What is important, what isn't? What exactly do you want and why?
- Also, how much can you spend? How much time do you have? How open and flexible or hard-wired and fixed should each part be?

| priorities           | compromise |
| -------------------- | ---------- |
| art intallation      |            |
| playable             |            |
| invites future usage |            |
| expandable           |            |
|                      |            |

### 2.11

got raspberry pi set up
 
 ### 2.17 
 raspberry pi not wanting to work today.. 
 decided to use my computer as the brains and not worry about rPi for now. 
 got the teensy talking to the computer via Firmata.
 tried to get pure data Firmata to work, but i realized it was over my head
 went with [processing with firmata](https://github.com/firmata/processing)
 analog control --> teensy --> firmata into computer --> visualize on the computer --> teensy --> DAC --> synth 
 rudimentry 3 buttons and 1 knob, but a proof of concept.
 