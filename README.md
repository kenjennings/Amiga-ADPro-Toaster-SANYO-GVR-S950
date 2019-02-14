# Amiga-ADPro-Toaster-SANYO-GVR-S950

Amiga Arexx scripts integrating Art Department Pro with FrED, the Video Toaster, and the Sanyo GVRS-950 SVHS single-frame video recorder.

---

At the time we were running SyntheToonz/Equine Video Studios a decent length, full-motion animation could take hundreds of megabytes to store on disk.  We just didn't have that much space available, or the money to buy buckets of more disk space.

I wrote this script to let us render a frame at a time, and write out the video frame to SVHS tape when rendered, so the computer only needed to have the one frame on disk at a time.  Lightwave was a pretty good, and fast renderer without ray tracing, so a project could be committed to tape overnight.  (Provided lightwave did not crash which was more common than we liked.)

This script monitors frames being output by the Lightwave renderer, may direct ADPro to perform some post processing on it (i.e. composite a watermark/credit on the videe frame), then ADPro loads the frame into the Toaster frame buffer, and then the script directs the GVRS-950 VCR over the serial interface to capture one frame on tape.   Frame counts and timestamps are incremented, and the whole process repeats.   In the event Lightwave crashed it was not too dificult to figure out where to resume and begin rendering/tape writing again.

A bug I could never get past is that the documented utility to talk to the VCR would not work directly from the Arexx script.   Look at the script to see the weird shenanigans I had to pull off to make this function.  Someday I would like to know what is wrong with this.

---

Originally released to Aminet.

Aminet field | Description
--- | ---
Short: |        ADPro FrED (ARexx) Scripts
Author:  |     Kenneth Jennings
Uploader: |    kenneth at daffy aatech com
Type:      |   arexx source
Architecture: | m68k-amigaos
Distribution: | Interplanetary distribution OK.

---

Programs | Description
--- | ---
SaveToSANYO.fred         | Sanyo GVR-S950 saver script
SaveToSANYO.fred.pre     | ADPro FrED .pre (init) script
SaveToVT_BUFFER.fred     | Video Toaster video buffer saver script
SaveToVT_BUFFER.fred.pre | ADPro FrED .pre (init) script
TestBCDAREXX.fred        | BCDARexxHandler test program


Save the scripts in ADPro's FrEDSAVERS directory.  

Everything should be fairly well documented.
Write if you have problems or have 
suggestions for improvements.

For the SaveToSANYO script you need to have 
the SANArexxHandler program somewhere in the search path.  (in the C: 
directory is ideal.)  The program is on the 
Amiga FreeDisk packaged with the Sanyo GVR-S950.


The Toaster Switcher must be running in order 
to use the SaveToVT_BUFFER saver.

A test script is included for those with ARexx
hacking experience who would like to help
me figure out why DIRECT communication with
the SANYO/BCDArexxHandler from a running Arexx
script doesn't work.
