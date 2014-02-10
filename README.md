elastatripper
=============
The Elastic Tripcode Mining Kernel

=============

One of the primary goals for the overall project is to modularize the 3 independant parts of the Tripcode@Home system, since this will ease collaborative development (and possibly debugging as well):
* The Elastatripper
* The Tripperman
* The Cloudtripper

The intention is to keep these separated as much as is feasible, and communicating together through simple, established mechanisms. One of the easiest and most well established mechanisms available is basic textfiles, and it makes sense that all three modules should be able to communicate together using this simple approach.

Available in sourcecode, both the Meriken and MTY trippers use input tripcode pattern textfiles and output tripcode results textfiles, and are suited as Elastatripper baselines for this text-only approach. Of these two Merikens is **a)** usable on both NVidia and AMD cards, and **b)** seems to have better alignment with the general goals of Tripcode@Home . Therefore the choice was made to use the Meriken codebase as a foundation for this project. However the MTY codebase is also available, and any good optimizations available from this more established tripper will certainly be considered as approaches to use within Tripcode@Home's Elastatripper. Any feedback on this choice is welcome, of course.

I will be working on porting his code over to the Linux platform, and will offer it back to Meriken when that port is completed. In the interim, Windows is the only platform currently supported.


Please let us know if you have any usage issues running the Meriken engine correctly. Also, any creative ideas are totally welcome!!


Enjoy! <'LLD~<3

usage:
=============
* Choose whatever platform you're on (x86 or x64), 
* and set the patterns for your tripcodes in the patterns.txt file (note: each pattern must have between 5-10 output characters),
* then just run the tripcode engine's exe from the command line. 

The defaults (no command line options) seems to work fine as a good starting point for most rigs. Tripcodes mined, performance metrics, and output estimates are sent to the console during the tripcode mining operation.

support issues:
=============

* Apparently this won't run on Windows 8 atm. WAAAH! D: Once the initial part of the migration to C++AMP is done, this will go away. -LLD

* Be sure to have recent drivers for your video card installed.

* Though you probably already have it installed on your Windows system, if you get a runtime error you may need to install Visual C++ redistributable. These are available from Microsoft at:

  * Microsoft Visual C++ 2010 Redistributable Package (x64) 
  http://www.microsoft.com/en-us/download/details.aspx?id=14632
  * Microsoft Visual C++ 2010 Redistributable Package (x86)
  http://www.microsoft.com/en-us/download/details.aspx?id=5555

* Microsoft .NET Framework 4 is also required, and is also probably on your Windows system already. Use the Windows Update facility to install it if not.

