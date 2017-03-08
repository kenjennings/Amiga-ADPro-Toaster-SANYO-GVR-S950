# Amiga-ADPro-Toaster-SANYO-GVR-S950
Amiga Arexx scripts integrating Art Department Pro, Video Toaster, and Sanyo GVRS-950 SVHS single-frame video recorded.

Short:        ADPro FrED (ARexx) Scripts
Author:       Kenneth Jennings
Uploader:     kenneth at daffy aatech com
Type:         arexx source
Architecture: m68k-amigaos
Distribution: Interplanetary distribution OK.

SaveToSANYO.fred         - Sanyo GVR-S950 saver script
SaveToSANYO.fred.pre     - .pre script

SaveToVT_BUFFER.fred     - Video Toaster saver script
SaveToVT_BUFFER.fred.pre - .pre script

TestBCDAREXX.fred        - BCDARexxHandler test program


Save the scripts in ADPro's FrEDSAVERS directory.  

Everything should be fairly well documented.
Write if you have problems or have 
suggestions for improvements.

For the SaveToSANYO script you need to have 
the SANArexxHandler program which came on the 
Amiga FreeDisk with the Sanyo GVR-S950 
somewhere in the search path.  (in the C: 
directory is ideal.)

The Toaster Switcher must be running in order 
to use the SaveToVT_BUFFER saver.

A test script is included for those with ARexx
hacking experience who would like to help
me figure out why DIRECT communication with
the SANYO/BCDArexxHandler from a running Arexx
script doesn't work.
