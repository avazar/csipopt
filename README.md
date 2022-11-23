# csipopt

This repository contains slightly updated (targeting .NET Standard 2.0 to use in modern .NET apps) version of [CSIOPT by Anders Gustafsson](https://github.com/cureos/csipopt).

Copyright (c) 2010-2013 Anders Gustafsson, Cureos AB.<br/>
Published under the Eclipse Public License.

## Introduction

*csipopt* provides a small and simple C# interface to the *Ipopt* non-linear optimizer. If the interface is
contained in a .NET class library, the interface is accessible via any .NET language. The library is targeted to .NET Standard 2.0, so *.NET Framework 4.6.1+* or *.NET Core / .NET* is required.

## Prerequisites

To successfully run an application calling the C# *Ipopt* interface, a dynamic linked library of *Ipopt* is 
additionally required. Pre-compiled libraries can be downloaded from the 
[following location](https://github.com/coin-or/Ipopt/releases).

At the time of this writing, the most up-to-date binaries, version 3.14.10, can be downloaded 
[here](https://github.com/coin-or/Ipopt/releases/download/releases%2F3.14.10/Ipopt-3.14.10-win64-msvs2019-md.zip).

Download binaries suitable for your platform, unpack the compressed *Ipopt* binary archive, from the folder 
*bin* copy the DLL files and place them in a folder that is accessible from the application or system path.

(Note! The actual name of the DLL is of course dependent upon which version of *Ipopt* binaries you are 
downloading.)


## Usage

It is possible to build stand-alone class libraries with all *csipopt* code from the *Cureos.Numerics* solution. 
Open this solution in Visual Studio 2019 or 2022 and build the *Cureos.Numerics* (.NET Standard 2.0), then reference the built project in your own application.

To use the C# interface in your own code, you can also copy the C# files _Ipopt*.cs_ to your class library. 
(Potentially, you may need to redefine the `IpoptDllName` in the *IpoptAdapter.cs* file to match the name of the 
native *Ipopt* DLL.) 

### Visual Studio examples

The example project is included in the VS Solution 
- Cureos.Numerics.Example.Hs071 - C# project
- Cureos.Numerics.Example.Hs071.VB - VB project
- Cureos.Numerics.Example.Hs071.FS - F# project

## Revision

Last updated on Novemver 23, 2022 by Andrey Azarov, avazar[at]bk[dot]ru.
