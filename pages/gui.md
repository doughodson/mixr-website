---
layout: page
title: GUIs
permalink: /gui.html
---
To provide developers with maximum flexibility and adhere to the concept of a framework, MIXR purposely does not provide a default Graphical User Interface (GUI). In other words, MIXR is not a single application that is customized by a developer; it is a framework designed to build a wide variety of different applications. Because of this, the software developer also defines a main() function. This empowers developers to create their own custom main(), and utilize their favorite GUI toolkit for application development. In some cases, several of these custom applications can be connected together via interoperability networks, such as DIS, to form a complete and possibly complex simulation system.

This approach enables the framework to be used in a wide variety of ways, for example:

* Console applications that require little user interaction can be built quickly and efficiently. This can be very useful for simulation testing and validation purposes.
* MIXR-based "extensions" to popular scripting languages such as Python, TCL, and Ruby, can be built to rapidly construct constructive simulations with, or without, polished GUIs. Leveraging high-level scripting language features can be useful for the efficient post-processing of simulation results.
* Easier integration of MIXR-based code with existing simulation applications. In some cases, an existing simulation application might already provide a GUI.
* A more radical use of the framework is with FPGA devices. MIXR coupled with an RTOS provides a useful environment for small embedded devices.
* The most common approach is the option to leverage the developer's favorite GUI toolkit, such as FOX, FLTK, wxWidgets and/or Qt.

This page provides several screenshots that are contained in the mixr-examples package.

## FOX-based Interface

The example below above integrates MIXR graphic capabilities within a Fox main window (FX:FXMainWindow). The application sets up a real-time thread for the execution and movement of several "worms" on the canvas. The menu provides functions to rotate and translate our logo around the canvas.

![]({{ site.baseurl }}/assets/pages/gui/fox_example.png "FOX Interface")

## FLTK-based Interface

The example below above integrates MIXR graphic capabilities within an FLTK version 1.3 main window. The application opens 2 glut windows and draws our logo as defined in input files. The translate buttons enable movement of the logo on the canvas. This example works in both Windows and Linux. 

![]({{ site.baseurl }}/assets/pages/gui/fltk_example.png "FLTK Interface")
