# 10LC

10LC Calculator Project

Beta version 0.9 notes

Advantage of this implementation is speed, but not using calc. ROM means some aspects of the calculator may seem different than original.  Source code may be released at a later date after clean up.  Recommended micro SD flash (to retain program, registers, etc.) - SanDisk Ultra 16GB SDHC.  Card may need to be formatted.  It can be used without a micro SD card, but programs and registers are not retained.

To retain program and registers, press the OFF key (to the left of the + key).  To prevent battery drain, turn the hardware switch located on top to the OFF position.  The calculator automatically turns off (and retains current settings) after 3 minutes.  To turn back on after an automatic shut off, press the RST (reset) button on the top left of the calculator.

Features:

- 10 registers and 99 program steps
- 2 line stack X and Y display
- 2 selectable display fonts
- 3 selectable display colors
- audible keyboard beep
- fast - approx. 100,000 loop iterations in 10 seconds
- internally has number range from approx. 1e-317  to 9.9e307

Known issues / differences from 10C:

- EEX implemented slightly differently - single digit exponent processed immediately
- Clear prefix not implemented
- Eng notation not implemented
- SST in normal calculator mode looks different for GTO or branching
- LASTX in program mode is 46 instead of 42.36
- commas for numbers and dot separators in program mode are not implemented
- tangent function less accurate when close to 90 degrees
- battery drains in sleep mode - use hardware off switch to preserve battery life

Program mode has been tested with program examples from the 10C manual:

P. 61 Temperature conversion example
P. 72 Cylindrical can example
P. 78 Looping example
P. 82 Radio isotope decay example
P. 84 Sales commission exercise
P. 92 Adding instructions by replacement
P. 93 Adding instructions by branching
P. 96 Storing another program


Burning firmware:

This 10LC firmware may be used for non-commercial personal or educational purposes.  No warranties are made on the use of the firmware.  It is up to the user to verify the accuracy or precision of this calculator implementation.

Go to Github riker2072 10LC repository.

Get 10LC.ino.bin, 10LC.ino.bootloader.bin and 1LC.ino.partitions.bin files.

Get Windows ESP32 flash download tool at: https://www.espressif.com/en/support/download/other-tools

For ChipType, use ESP32-S3

For WorkMode, use Develop

For LoadMode, use USB

Click on … to select 10LC.ino.bin file directory location.  Check mark in the box on the left.  In the @ box, put 0x10000

Click on … to select 10LC.ino.bootloader.bin file directory location.  Check mark in the box on the left.  In the @ box, put 0x0000

Click on … to select 10LC.ino.partitions.bin file directory location.  Check mark in the box on the left.  In the @ box, put 0x8000

SPI speed is 40MHz, SPI mode is DIO.  Check mark in the box labeled “DoNotChgBin”.  My port settings are COM4, baud 115200.  Connect the M5 Cardputer to your PC using a USB C cable.  Click on START to burn the firmware.

Files for color and black and white overlays are also on Github.




