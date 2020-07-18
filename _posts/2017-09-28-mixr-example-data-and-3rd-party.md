---
layout: post
title:  "MIXR Example Data and 3rd-Party Library Binaries for Visual Studio"
---
The next release of MIXR is currently in the works. As part of this next release, a few high-level, organizational aspects will change as follows:

* Support for Visual Studio 2013 is being dropped - all current efforts concerning compilation with Visual Studio are focused on using 2015 and 2017. Making this move allows us to tap more available Modern C++ features and concepts throughout the code base. Frankly, in the fast-moving world of C++, Visual Studio 2013 is starting to look and feel a bit dated. Newer C++ features and capabilities used within MIXR are already well-supported by GCC and Clang compiler suites, so this has no impact or effect on Linux users.

* Example data files that have been included as part of the examples package have been extracted, separated and now managed outside of the GitHub hosted repository - they will become part of a new separate 'mixr-data' package (distributed as a zip or tar-zip file). This change greatly lightens the burden on the git ecosystem and repository and eliminates meaningless revision control of binary files that tend to be rather large. As a result of this change, new opportunities have presented themselves – for example, this new MIXR package will include a richer set of data including the last publicly available DAFIF release, the Vector Map (VMap) Level 0 data set (VMAP0), and a TerraPage formatted visual database of the Portland, OR area.

* The MIXR 3rd-party package which contains all MIXR library dependencies is also being updated in a few ways. First, all Visual Studio 2013 binaries have been removed, and second, all the OpenSceneGraph core binary libraries plus the TerraPage plug-in loader for Visual 2015 and 2017 has been added. As with the MIXR data, this package will be now be managed outside of git to avoid meaningless tracking of large binary files.

Making these adjustments has facilitated improvements in the code base, and helped ease the creation of more visually interesting examples. For instance, the old 'SimpleOTW' example has been revamped, updated and improved to serve as a simple image generator example for MIXR-based simulations.
