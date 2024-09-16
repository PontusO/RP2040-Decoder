RP2040-Decoder
===============

This Project is a fork from Garbiel Keppensteings RP2040 base DIY DCC Decoder for model railroad locomotives which aims to be cost effective.

News
----

2024-06-30 - Added the possibility to invert the output bits. Very usefull if you are connecting common anode LED's to your decoder.
             Also added support for 14 and 28 speed steps.
	     
2024-03-27 - The latest firmware (V2) now also supports a kick start feature.
             This is controlled by CV65. Setting this CV to anythin non zero will enable a motor pulse equal in milliseconds to the number written into CV65.
	     This feature is used to overcome motor and drivetrain stiction when a locomotive starts to move from standstill.
	     The default value is 0 which means the feature is disabled and setting it to a non zero value will enable the feature.
	     Do not write the value 255 (a 255 mS pulse) to this register as this will completely reset your decoder.

Features
--------

- DCC digital signal decoding
- Motor load/speed control
- 4 Outputs to drive loads up to 400mA each
- 6 GPIO for lighter loads or custom applications
- Programmable on programming track
- CV Function Mapping
- Board size of 25x20 mm

Getting Started
------------


The ["Getting Started"](https://github.com/gab-k/RP2040-Decoder/wiki/Getting-started) page provides an overview of the steps required to use the decoder as well as brief instructions for all the necessary steps.


License
-------
- Software - MIT license
- Hardware - CERN Open Hardware Licence Version 2 - Permissive
- [LICENSE](https://github.com/1nct/RP2040-Decoder/blob/main/LICENSE)

------------
Further details about the project can be found here:  [RP2040-Decoder Wiki](https://github.com/GabrielKoppenstein/pico-decoder/wiki)

Note: The decoder is still in early development, there might (will) be bugs as its not tested that much yet.
So suggestions on how to improve things and bug reports are always much appreciated.
The wiki is also work in progress and will be updated to be as comprehensive as possible.

2 hardware versions is supported. By default the original board created by Gabriel is supported and by running cmake
with the following option: "-DPICO_BOARD=ilabs_opendec02" the project is setup for the iLabs OpenDec02 decoder."

------------
<p float="left">
<img src="/docs/png/RP2040-Decoder-Rev_0_2_front.png" alt="PCB Front Side Image" title="Front" width="400"/>
<img src="/docs/png/RP2040-Decoder-Rev_0_2_back.png" alt="PCB Back Side Image" title="Back" width="400"/>
</p>

