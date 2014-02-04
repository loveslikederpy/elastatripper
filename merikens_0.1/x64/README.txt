Meriken's Tripcode Engine English 0.1
Copyright (c) 2011-2013 Meriken



INTRODUCTION
============

"Meriken's Tripcode Engine English" is an Windows application 
designed to brute-force tripcodes at maximum speed and efficiency. 
It is arguably the fastest and most powerful program of its kind. 
It makes maximum use of available computing power of CPUs and GPUs,
and the user can specify flexible regex patterns for tripcodes. It 
features highly optimized, extensively parallelized implementations of
Bitslice DES and SHA-1 for SSE2, AVX, CUDA, and OpenCL.

Just to give you ideas as to how powerful the program is, the author
was able to achieve 400M tripcode/s for DES crypt(3)-based 
10 character tripcodes and 11G tripcode/s for SHA-1-based 
12 character tripcodes with a combination of multiple AMD Radeon HD
Series graphics cards.



SYSTEM REQUIREMENTS
===================

Operating Systems:
    Windows XP/Vista/7/8 

Graphics Cards:
    CUDA-enabled graphics cards from NVIDIA 
    AMD Radeon HD 77xx/78xx/79xx or later
    (HD 5xxx/6xxx can be used only for 12 character tripcodes.)

Software: 
    Microsoft .NET Framework 4
    Microsoft Visual C++ 2010 Redistributable Package (x86)
    Microsoft Visual C++ 2010 Redistributable Package (x64)
    (if you are using a 64bit operating system)
    NVIDIA Display Driver Version 320.49 or later
    (if you are using an NVIDIA graphics card) 
    AMD Radeon Desktop Video Card Driver
    (if you are using an AMD graphics card)



INSTALLATION
============

Make sure to download and install the required software packages before 
executing the program.

If there is no OpenCL driver in the system, make sure to copy
either OpenCL\x86\OpenCL.dll or OpenCL\x64\OpenCL.dll,
depending on the operating system, to the folder where 
the executables are located.



USAGE
=====

Specify search patterns in "patterns.txt" and run either
"MERIKENsTripcodeEngine.exe", if you are using a 32bit operating system, or
"MERIKENsTripcodeEngine64.exe", if you are using a 64bit operating system.
Matching tripcodes will be displayed and saved in "tripcodes.txt".



OPTIONS
=======

-g                       : Use GPUs as search devices.
                           (This option can be used in combination
                           with "-c".)

-d [device number]       : Specify a GPU to use.

-c                       : Use CPUs as search devices.
                           (This option can be used in combination
                           with "-g".)

-l [length of tripcodes] : Specify either 10 or 12.
                           (Please note that you can use 12 character
                           tripcodes only at 2ch.net.)

-t [number of threads]   : Specify the number of CPU search threads.

-o [output file]         : Specify an output file.

-f [input file]          : Specify an input file.



LICENSING
=========

"Meriken's Tripcode Engine English" is free software, licensed 
under GPLv3.  Please refer to "Misc\COPYRIGHT.txt" for details.



SOURCE CODES
============

The source codes are found in "Misc\Source codes.zip".

This application was developed using the following programs and
frameworks:

    Visual Studio 2010 Professional
    CUDA Toolkit 5.5
    AMD APP SDK 2.8
    YASM 1.2.0
    Multiple Precision Integers and Rationals (MPIR)

Make sure to copy the include file and library files of MPIR 
to the appropriate Visual Studio folders before building the application.



MISCELLANEOUS NOTES
===================

Please feel free to contact the author at meriken.2ch@gmail.com for feedback, bug reports, suggestions, etc.

"Meriken's Tripcode Engine English" is a heavily stripped-down version 
of the original GUI-based, network-capable "Meriken's Tripcode Finder,"
which is intended primarily for users of 2ch.net in Japan. If Japanese 
does not discourage you, check out the original application as well as
"Meriken's Tripcode Yggdrasil," a web-based distributed tripcode 
brute-force service :-)



HISTORY
=======

0.1 (September 21, 2013)
The initial version was released
