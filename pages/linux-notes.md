---
layout: page
title: "Linux Notes"
permalink: /linux-notes.html
---
Two of the most popular Linux distributions are either Fedora or Ubuntu-based. Both are often used to develop and execute MIXR-based simulations. This page provides installation and configuration notes to install required prerequisites, compile MIXR libraries and execute examples for the Ubuntu distribution. A working knowledge of Linux is assumed.

### Installing Prerequisites

Prebuilt packages (e.g., deb) are often available to facilitate prerequisite installation.  It is often preferable to install prerequisites using the prebuilt packages as they can be easily removed if necessary or automatically updated if connected to the Internet. Gzipped tar files (.tar.gz or .tgz) are typically available as well.

Note: Ensure you have administrator privileges when installing packages as most of them install header files and libraries into system areas.

```sh
# packages required by mixr's graphics library
sudo apt install libftgl-dev libfreetype6-dev freeglut3-dev libfontconfig-dev
# package required by OpenRTI (HLA interface) to work with XML files
sudo apt install libexpat-dev
# packages required to compile, link and manage C++ code
sudo apt install build-essential cmake autogen automake libtool libtool-bin
```

### Building MIXR Libraries

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
