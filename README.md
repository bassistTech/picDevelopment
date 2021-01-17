# picDevelopment: Microchip PIC development system for 68k Apple Mac

## Under construction

Francis Deck, Jan. 16, 2021

I recently dug up all of this stuff, and discovered that the most important pieces were still recoverable. I don't think you'd want to build anything from it today.

It's a development tool for 8-bit PIC microcontrollers, that ran on a 68k Apple Macintosh under System 7. I created it because I switched from MS-DOS to Mac in 1993, but found that there was virtually no interest in hardware hacking within the Mac community, and no available tools. So I made my own. I was already familiar with hardware hacking on earlier machines (MS-DOS, Apple II), and microcontrollers (8051, PIC).

## Motivation: Why does a Mac hardware hacker need microcontrollers?

Other than for pure fun, of course. Earlier computers usually had some kind of easy hardware interface. The Apple II had its slots. The IBM PC had slots too, and most MS-DOS computers had a parallel printer port that could be used as a crude GPIO (general purpose input-output). I ran my entire PhD thesis experiment off the printer ports of two MS-DOS machines, using homemade data acquisition hardware. I couldn't justify the cost of commercial hardware for a proof-of-concept, and the POC worked well enough that I kept using it.

The Mac didn't have a convenient port. The NuBus slots on some advanced Macs were too complex for a hobbyist to deal with. I had a Quadra 605, which only had a couple of serial ports -- Modem and Printer. The most straightforward way to interface a serial port to anything turns out to be through a microcontroller (MCU). Today, this stuff is old hat. Most hobby projects that connect things to PC's do so through standard interfaces such as USB or wireless, using microcontrollers such as the ubiquitous Arduino, Teensy, or ESP32, that support those interfaces. What I was doing with the Mac was the same thing, only more primitive in keeping with what components and interfaces were readily available at the time. Remember, this predates USB and wi-fi.

Once you've got a basic interface working with a microcontroller, other benefits begin to emerge. The MCU is not affected by the complexity of software running under a modern OS, so it can implement realtime functionality, and perform multiple operations on its own before having to exchange data with the PC. Also, most modern MCU's have built-in features such as analog-to-digital converters, allowing them to be used as low cost data acquisition peripherals with relatively little additional circuitry.

## What I built

I built a device programmer that connected to one of the standard Mac serial ports, and wrote an assembler in Hypercard! At the time, developers considered Hypercard to be a toy, but it was a fully functional programming tool, and supported add-ons for things like talking to the serial ports. Today, Hypercard is thought to be visionary, since it introduced people to hypertext and active content before the Web, and enabled laypeople to write software for the hideously complex graphical computing platform.

How I built it was kind of shady. I got it working on my MS-DOS machine -- its last use before I threw it away. Then I transferred it to the Mac, piece by piece. In fact my rather odd use of the negative signals on the Mac serial port allowed me to control the programmer circuit using the negative logic of RS232. But eventually I was able to replicate the entire thing -- hardware and firmware -- on a Mac. I remember it was a big deal when Linux could compile itself and all of its own core tools. I achieved something like that too, but of course on a much more modest scale -- being able to use a Mac to make Mac compatible hardware.

I even created a primitive circuit board layout tool using SuperCard, an advanced successor to HyperCard. But I wanted my programming tool to be something I could share, so I stuck with HyperCard for it. I didn't share my printed circuit layouts -- how dumb of me. Today, the only stuff I have from that era is whatever I shared with everybody. 

In 1996, I wrote an article about my tool chain, for the journal of the MacSciTech Association. You could download my stuff from their Website. I didn't have my own web page, and was using an AOL e-mail address and dial-up modem. But I offered a "partial kit" consisting of a pre-programmed PIC chip and bare printed circuit board. I sold a few dozen. I have no idea if anybody actually ever got one working. The main interest seemed to be making smart cards to break the encryption of early satellite TV systems.

Through a succession of products for hobbyists, I gained some experience with running a tiny, home-based business, but also, some lessons about products. Mainly, I learned that a product has to work before you ship it. Kits are a recipe for unhappy customers unless they are spectacularly well documented. I also learned that it's anything but simple to be responsible for a product that contains software intended for others to use. Of course these things are obvious to everybody today.

## My programmer circuit

## Additional files and links

SciTech Journal article on PIC development system
SciTech Journal article on data acquisition board
Source code for the PIC assembler, in HyperCard scripting language
The Hypercard stack itself, running under emulation
