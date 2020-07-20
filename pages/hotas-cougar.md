---
layout: page
title: "Hotas Cougar"
permalink: /hotas-cougar.html
---
The Thrustmaster HOTAS Cougar is a replica U.S. Air Force F-16 block 52 controller (stick and throttle). It is built with a full metal casing including base, handle, and buttons. It connects to the PC via USB. The device comes with a Windows Control Panel to configure various options. An equivalent Control Panel does not exist for Linux.

Windows Control Panel settings can be saved and stored in a file called a "profile". The files have a file extension .tmc and by default are located at C:\Program Files\HOTAS\Profiles.

![]({{ site.baseurl }}/assets/pages/hotas-cougar/cougar.png "HOTAS Cougar")

### Profile Loader for Linux

Sunday, February 4 2007 : This profile loader code enables a Linux user to load and configure a HOTAS Cougar device. Just download and compile the attached code using standard Linux GCC tools. A makefile is supplied. (Note: You must have libusb installed on your system.) A program called cougarProfile will be built. cougarProfile can be executed from any shell prompt. [Download]({{ site.baseurl }}/assets/pages/hotas-cougar/cougar-profile_v2007_0204.zip) 

![]({{ site.baseurl }}/assets/pages/hotas-cougar/control-panel-0.png "Control Panel")

The default profile configured for the Cougar is shown above. The primary reason for developing the cougarProfile tool was to enable Linux to "see" and read the Microstick X and Y inputs.

![]({{ site.baseurl }}/assets/pages/hotas-cougar/control-panel-1.png "Control Panel")

A new profile can be created by adjusting the parameters available through the control panel (yes, this must be done in Windows!) and saved. The cougarProfile zip file includes a profile file called cursorEnable.tmc. This profile configures the Microstick X and Y channels so that Linux can "see" and read them.
