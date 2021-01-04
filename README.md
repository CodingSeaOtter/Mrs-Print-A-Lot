# Mrs. Prints-A-Lot

Printer: Creality Ender 5 Pro, 4.2.2 Board/TMC2208, 
BLTouch: Creality's own bought from [Amazon](https://www.amazon.com/dp/B07WK3T7S7/)

# BLTouch Setup

Endstop Connection, Made an attempt to reverse the wires, but with no success, so returned them to their original state.

![Z-Endstop Connection](http://i.troublesncuddl.es/Flickering-Monumental-Monarch)

Signal Connection.

![Signal Connection](http://i.troublesncuddl.es/Stark-Tedious-Roach)

# Issue

The printer will upon starting up, initiate the BLTouch (unit lights up red, and extends/retracts the probe twice) but fails to get the BLTouch to respond to any of the commands, Reset, Self-Test, Deploy, etc, and fails to get it to work for homing functionality.

# What I've Tried

## First Attempt

I downloaded the bltouch firmware (Release, 14th of Aug/Ender-5 Pro_32bit_Marlin2.0.1 - V1.1_TMC2208.BL Touch_Firmware_0814.rar) from creality's website [here](https://www.creality.com/download)/[Direct Link](https://file2-cdn.creality.com//website/b44ed998-ad76-4fec-91d1-8cc4ca19b42c), put it on the SD card and flashed it to the printer. Printer will start fine, but have the issues explained above, but will further refuse to home and get a fatal error, M119 shows that Z_MIN is always TRIGGERED, regardless of the orientation of the z-endstop wires from the probe.

## Second Attempt

For the second attempt, I downloaded Marlin 2.0.7.2, and made a configuration for it based upon the example configurations shown for the creality v2 board, as well as mixing in the examples on the BLTouch setup. For this attempt, I didn't setup the BLTouch for 5V mode in this attempt. The configuration files are in the repository [sans 5v mode.](https://github.com/CodingSeaOtter/Mrs-Print-A-Lot/blob/8ec95782e90684b6888592c03dfd3f652ba88494/Configuration_adv.h#L711)

## Third Attempt

Repeat of second attempt, but in 5v mode, full configuration in the repository.

## Fourth Attempt

I've attempted to flash the firmware that I found [here](https://drive.google.com/drive/folders/1b7cvZN3Leerr4RhY1L1k1eTbTLEeQMPK) after digging around on Creality's own website. but with no seemingly no effect on my issue.