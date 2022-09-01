---
layout: page
title: "Linux Notes"
permalink: /linux-notes.html
---
## Ubuntu Notes

Two of the most popular Linux distributions are either Fedora or Ubuntu-based. Both are often used to develop and execute MIXR-based simulations. This page provides installation and configuration notes to install required prerequisites, compile MIXR libraries and execute examples for the Ubuntu distribution. A working knowledge of Linux is assumed.

### Installing Prerequisites

Prebuilt packages (e.g., deb) are often available to facilitate prerequisite installation.  It is often preferable to install prerequisites using the prebuilt packages as they can be easily removed if necessary or automatically updated if connected to the Internet. Gzipped tar files (.tar.gz or .tgz) are typically available as well.

Note: Ensure you have administrator privileges when installing packages as most of them install header files and libraries into system areas.

#### Ubuntu

```sh
apt install libftgl-dev
apt install libfreetype6-dev
apt install freeglut3-dev
apt install libfontconfig-dev
apt install libexpat-dev
apt install build-essential
apt install cmake
apt install autogen
apt install automake
apt install libtool
apt install libtool-bin
```

Installing packages for FTGL, freetype and freeglut are essential components to build the MIXR **graphics** library and compile GLUT-based applications.

The 'libexpat-dev' package is required to compile OpenRTI (an HLA interface).

Installing the 'build-essential' package installs c++ tools to compile and link that language. 'cmake', 'autogen', 'automake', 'libtool' and 'libtool-bin' install support building tools needed to compile all of mixr's dependencies.

Note: Some Linux distributions don't provide FTGL packages in a convenient manner.  For example, CentOS 7 doesn't include FTGL on any of their ISOs.  Because of this, the build script provided with 3rd party source code will compile FTGL.

#### Common Image Generator Interface (CIGI)

[CIGI](http://cigi.sourceforge.net) is an open-source visual system interface library that is an essential component to build MIXR's **ighost_cigi** library. Download and install the latest CIGI Class Library (CCL).  As of this writing, it is distributed in a gzipped tar file.

Download ccl_3.3.3a.tar.gz and perform the following steps:

````sh
tar xzvf ccl_3.3.3a.tar.gz    // unzips and extracts the directory "ccl"
cd ccl                        // change to "ccl" directory
configure                     // configure package
make                          // compile libraries
make install                  // install libraries
````

#### JSBSim Flight Dynamics Model

[JSBSim](http://jsbsim.sourceforge.net), is an open source flight dynamics model (FDM) that is an essential component to build the MIXR **model** library.

Note: Use the version of JSBSim included with MIXR, as it is often the most current available and supported by the MIXR vehicle interface. It can be found in the mixr-3rdpartysrc download.

````sh
tar xzvf jsbsim_cvs_v2015_0704.tgz   // unzips and extracts the directory "jsbsim"
cd jsbsim/JSBSim                     // change to "JSBSim" directory
./autogen.sh --enable-libraries      // configure package to make linkable libraries
make                                 // compile libraries
make install                         // install libraries
````

#### Data Recording/Storage Library

[Google Protocol Buffers](http://code.google.com/p/protobuf/) : Google protocol buffers is a way of encoding structured data in an efficient yet extensible format. It is an essential component required to build the MIXR **recorder** library.

````sh
unzip protobuf-2.4.1.zip         // unzips and extracts the directory "protobuf-2.4.1"
cd protobuf-2.4.1                // change to "protobuf-2.4.1" directory
configure                        // configure package to setup build environment
make                             // compile protoc application and protobuf libraries
make install                     // install application and libraries
````

### MIXR

#### Building Libraries

MIXR can be compiled and installed in two ways, as a system component just like any other prerequisite, or within a user account.

#### As a System Component

For this installation, MIXR is installed just like many other packages. Perform the following steps:

````sh
cd /usr/local
tar xzvf mixr_vX.X  // unzips and extracts the directory "mixr"
cd mixr             // change to "mixr" directory
cd src              // change to "src" directory
                    // consider reviewing the makedef file to configure options
make                // compile libraries
make install        // install header files and libraries to /usr/local/include/mixr
                    // and /usr/local/lib/mixr respectively
````

#### Within a User Account

We supply a build script with the 3rd party source code to automate building source code within a user account.

#### Building Examples

When the examples are compiled, the environment MIXR_ROOT is used to locate header files and link libraries.  Simply unzip and extract the examples to the directory desired, change to the "src" directory and run "make".
