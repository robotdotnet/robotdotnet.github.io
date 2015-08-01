---
layout: page
title: Frequently Asked Questions
---

## Installing and Running RobotDotNet

### What version of the .NET Framework is used for RobotDotNet?

RobotDotNet is compiled for the .NET Framework 4.5. All programs are generally compiled using VS 2015 with the new Roslyn compiler. However, the libraries are usable using VS 2013 as well as VS 2015. Mono 4.0 can be used on Linux and Mac to compile and run the libraries. On the RoboRIO, we currently use Mono 4.0.1 compiled from source using a slightly modified version of the NI build tools found [here](https://github.com/ni/nilrt/tree/dev/mono_support)

### What happens when an exception is thrown?

When an exception is thrown and not caught, the exception will be printed out to the console, and will log to the Driver Station if it is connected. The console output can be read from NetConsole, which can be opened from the FRC menu in VS. It can also be set to automatically open on deploy in the VS FRC Settings.

### How do I use WPILib?

To use the WPILib, import WPILib "using WPILib" in C# or "Imports WPILib" in Visual Basic. However, if starting a new robot project, we recommend using one of our project templates included with the extension. Visual Basic templates should be added by build season.

### Why is there an error when trying to use the Encoder class?

By default, when creating a new class, "using System.Text" will automatically be included. System.Text includes an Encoder class, which is interfering with WPILib encoder class. There are 2 ways to solve this problem.
* Remove "using System.Text". This is the recommended fix if you are not using anything in the System.Text namespace.
* Add "using Encoder = WPILib.Encoder" to the usings. This will make any reference to Encoder use the WPILib version. If you need to use System.Text's Encoder, you will have to use its fully qualified name "System.Text.Encoder".

### How do I use a simulator?

Currently, there are no prebuilt simulators. We are working on one though. However, you can run your code on the computer by running it directly in Visual Studio, and it should run. We do currently have a prototype simulator running in MonoGame, but it requires some slight manual setup currently. 

### Can I build a simulator in Unity?

Currently, no. Unity only supports up to .NET 3.5, whereas we require the DLR for the simulator, which requires at minimum .NET 4.0. We hope that sometime in the future Mono 4 support gets added, which would bring .NET 4, but for now Unity is not supported.
