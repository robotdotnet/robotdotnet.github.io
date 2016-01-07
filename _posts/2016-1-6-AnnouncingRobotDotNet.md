---
layout: post
title: Initial RobotDotNet 2016 Release
---

Just in time for the 2016 kickoff, we are happy to announce the initial release of RobotDotNet, a port of the FRC libraries to DotNet and C#. This port has been worked on over the past offseason, and has been thoroughly tested. Here's whats working so far.


* [WPILib](https://github.com/robotdotnet/WPILib): A full port of the WPILib to DotNet. 
* [NetworkTablesCore](https://github.com/robotdotnet/NetworkTablesCore): A port of NetworkTables using the new ntcore library from FIRST.
* [FRC Visaul Studio Extension](https://github.com/robotdotnet/FRC-Extension): An easy to use Visual Studio extension, including templates for creating new robot projects, and tools for deploying robot code and the runtime.


The WPILib has all the features you know from FIRST, in addition to some cool new features, including:

* Attributed Command Model: A new way of creating Command-Based robots without all the boilerplate code normally required.
* Full NavX MXP Support: Full NavX MXP support ported from the newest release from KauaiLabs.
* Simulator Support: One of the coolest features. The backend of the code has extensive support for hardware simulation. We also provide a MonoGame template to enable you to create your own simulator. Documentation for this can be found on the Tutorials site.


In order to run on the RoboRIO, the newest version of Mono (4.2.1) has been compiled using NI's compilation tools.

Our documentation can be found at our website, [which is located here.](http://robotdotnet.github.io/Documentation/API/index.html)

Instructions for downloading the extension and the libraries can be found at the tutorials page. The extension is uploaded to the Visual Studio Gallery, and the library has been uploaded to NuGet for easy updating. 

It has been an interesting project to take on, and I would like to thank some people:

* Jeremy Koritzinsky, who helped with much of the porting and created the Attributed Command Model
* Shockwave 4488, who let me borrow a robot for much of the offseason to test and make sure everything worked, in addition to porting previous robot code.
* FIRST and WPI, for providing a great set of libraries to start from.
* RobotPy, which was much of inspiration for the project, and was the starting base for the simulator support. In addition to some direct support from Dustin Spicuzza and Peter Johnson.
* Microsoft, for creating an awesome language and set of tools, and providing them for free to the community.
* Resharper, for their great refactoring tools which have helped clean up the codebase immensely.