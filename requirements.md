# Requirements 
Before you download and build the Android source, ensure that your system meets the following requirements, then see Establishing a Build Environment for installation instructions by operating system.

## Hardware requirements
Your development workstation should meet or exceed these hardware requirements:

A 64-bit environment is required for Android 2.3.x (Gingerbread) and higher versions, including the master branch. You can compile older versions on 32-bit systems.
At least 250GB of free disk space to check out the code and an extra 150 GB to build it. If you conduct multiple builds, you need additional space.
Note: If you're checking out a mirror, you need more space as full Android Open Source Project (AOSP) mirrors contain all Git repositories that have ever been used.
At least 16 GB of available RAM is required, but Google recommends 64 GB.
As of June 2021, Google is using 72-core machines with 64 GB of RAM internally, which take about 40 minutes for a full build (and just a few minutes for incremental builds, depending on exactly which files were modified). By contrast, a 6-core machine with a similar amount of RAM takes 3 hours.

## Software requirements
The AOSP master branch is traditionally developed and tested on Ubuntu Long Term Support (LTS) releases, but other distributions may be used. See Establishing a Build Environment for additional required packages and the commands to install them.

Your workstation must have the software listed below. These requirements apply to the AOSP master branch. For Android versions 8.0 (Oreo or O) through 5.0 (Lollipop or L), consider using the included Dockerfile to ease installation of all required packages. For the manual method, see Supporting Older Versions.

## OS
If you're developing against the AOSP master branch, use Ubuntu 18.04 (Bionic Beaver).

Warning: Building on either Windows or MacOS (as of June 22, 2021) is NOT supported.

## JDK
The master branch of Android in AOSP comes with a prebuilt version of OpenJDK, so no additional installation is required.

Older versions of Android require a separate installation of the JDK. On Ubuntu, use OpenJDK.

## Key packages
The AOSP master branch comes with a prebuilt version of Make, so no additional installation is required. Git is similarly installed as part of the Establishing a Build Environment process.

Ensure that your system has Python 3.

Warning: Python 2 support was sunset on Jan 1, 2020 as detailed in Sunsetting Python 2. All major Linux distributions are deprecating support for the Python 2 package. Google strongly recommends that you migrate all your scripts over to Python 3.
Note: AOSP ships with its own copies of the Python 2 and Python 3 packages, and you can use the version (such as SEPolicy) that's included in the source tree. Google is migrating all scripts in the Android source tree to Python 3, and the embedded copy of Python 2 might be deprecated.
For additional details, see Porting Python 2 Code to Python 3, and advice on sunsetting your Python 2 code.

## Device binaries
Download previews, factory images, drivers, over-the-air (OTA) updates, and other blobs below. For details, see Obtaining proprietary binaries.

Preview binaries (blobs) for AOSP master branch development
Factory images for supported devices running tagged AOSP release branches
Binary hardware support files for devices running tagged AOSP release branches
Build toolchain
Android 8.0 and higher support only Clang/LLVM for building the Android platform. Join the android-llvm group to pose questions and get help. Report NDK/compiler issues at the NDK GitHub.

For the Native Development Kit (NDK) and legacy kernels, GCC 4.9 included in the AOSP master branch (under prebuilts/) may also be used.
