---
date updated: '2021-02-04T13:53:52-05:00'

---

# notes

## 1.28.2021 meeting

PWM resolution vs how many channels? 
EPOT chip for volume control - programmable voltage divider
talked to eddie and that seems like it wont really work
TUNING - linearize feedback. 
<https://www.pjrc.com/teensy/td_pulse.html>
frequency locked loop? 
piano has 88 keys which span the frequency range 27.5 Hz (A0) to 4186 Hz (C8).
set up REPO for files and documengation

### 2.1.21 meeting with Dr. Brothers

continuous wave rader as way to do proximity?
he likes the idea and might want to incorporate it into future junior design classes…

### 2.2 work in shop

control voltages are usually -5 to +5V.. teensy can only do 0-5.. how to solve that?

- check out CV schemes for modules
- maybe could alter teensy or change groun ref or make modules do 0. - 5
-

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
