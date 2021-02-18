# Software How To

### raspberry pi
- get latest version of Raspberry Pi OS
- download arduino software from webste
- follow [this tutorial](https://www.raspberrypi-spy.co.uk/2020/12/install-arduino-ide-on-raspberry-pi/)
- download and follow instructions for teensy on [PJRC website](https://www.pjrc.com/teensy/td_download.htm)
- upload a blink sketch and it should work!

### Teensy 4.0
ARM Coretx-M7 IMXRT1062 processor 
all pins on teensy are 3.3 V!

### Firmata

- Firmata is a protocol for communicating with microcontrollers from software on a computer. 
- problem with firmata on Teensy 4.0 initially
- need to change the Board.h file.
- check out the [github for the updated board.h](https://github.com/firmata/arduino/blob/master/Boards.h)
- These are the PWM pins for 4.0:  0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 18, 19, 22, 23, 24, 25, 28, 29, 33, 34, 35, 36, 37, 38, 39
	- 31 of the digital pins support [Pulse Width Modulation (PWM)](https://www.pjrc.com/teensy/td_pulse.html), which can be used to control motor speed, dim lights & LEDs, or other uses where rapid pulsing can control average power. PWM is controlled by the analogWrite function. 5 groups of PWM can have distinct frequencies, controlled by the analogWriteFrequency function.
- getting the firmata_test program to run on Raspberry Pi is another challange
	- download the .tar.gz file from the [PJRC website](https://www.pjrc.com/teensy/firmata_test/)
	- need to install [wxWidgets for Linux](https://wiki.wxwidgets.org/Compiling_and_getting_started) (wx widgets is a C++ library that lets developers create applications for Windows, OS X, Linux and UNIX on 32-bit and 64-bit architectures) 
	- involves sudo apt installing prerequesistes, downloaded the file, unzipping, then building the library
		- the 'make -j3' command seems to be taking a while
