# cw-tone-generator
Morse Code Key Tone Generator

This is a tone generator that I use with a morse code key for input to an SDR.
It uses a 555 timer to generate a tone of 500-1000 Hertz, and a transistor
to turn the tone output on and off.

![Image of schematic](https://github.com/glenoverby/cw-tone-generator/raw/master/CW555.png)

Assembly was done "dead bug" style on an IC socket.

![Image of inside](https://raw.githubusercontent.com/glenoverby/cw-tone-generator/master/inside-half.jpg)

![Image of outside](https://raw.githubusercontent.com/glenoverby/cw-tone-generator/master/outside-half.jpg)

The USB audio adapter is a cheap 48khz 16 adapter from my junk pile.
The microphone input connector broke off but it was good for this project.
 

I've tried a variety of techniques for connecting a morse code key to
an SDR: using a custom USB device (a teensy running LUFA) acting as a
MIDI input, as a virtual serial port, and as an audio input.
The MIDI input suffered from latency of in the handling of MIDI events,
and was limited to slow CW speeds.
The serial port also worked at slow speeds, but required much more work
in timing of events to work at higher CW speeds.
The audio adapter worked well, but was only a single input.
The JACK audio connection kit requires the device be both input and ouptut,
and I never figured out the USB device descriptors to make that work.
This one works!

Glen Overby
October, 2017

