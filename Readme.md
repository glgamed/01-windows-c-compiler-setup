# C/C++ Setup for Windows
I usually develop on Linux (Debian), setting a development environment is easy. Using apt package manager, you can install all needed libraries/tools.

I want start developing on Windows 11 to see if it's easy to setup a C/C++ develpment environment, so I need these minimum tools to be installed:
- C/C++ compiler
- CMake
- Ninja (make is OK but Ninja is fast)
- Editor
- Git

## C/C++ Compiler
I don't want to use Visual Studio due to portability issues, so I choose to install GCC.

To install GCC, you can use prebuilt compiler like **mingw** or **msys2**.

When searching for portable GCC installation (no installer but a zip that you can extract), I found Portable C and C++ Development Kit for x64 Windows **[w64devkit](https://github.com/skeeto/w64devkit)**

You can download files from **[w64devkit Releases](https://github.com/skeeto/w64devkit/releases)**

I installed latest release **[w64devkit 1.23.0](https://github.com/skeeto/w64devkit/releases/download/v1.23.0/w64devkit-1.23.0.zip)** but I get antivirus issues and some files were quarantined.

So I verified all releases until antivirus was OK with **[w64devkit 1.17.0](https://github.com/skeeto/w64devkit/releases/download/v1.17.0/w64devkit-1.17.0.zip)**

## CMake

CMake prortable installer can be downloaded from **[CMake 3.30.0](https://github.com/Kitware/CMake/releases/download/v3.30.0/cmake-3.30.0-windows-x86_64.zip)**

## Ninja
Ninja portable installer can be downloaded for **[Ninja 1.21.1](https://github.com/ninja-build/ninja/releases/download/v1.12.1/ninja-win.zip)**

# Editor

I choose to use Visual studio Code that can be installed from **[here](https://code.visualstudio.com/)**

I use **winget** to install it by this in command prompt or Powershell

`winget install microsoft.visualstudiocode`

# Git
Git can be installed from **[here](https://git-scm.com/download/win)**

I use **winget** to install it by this in command prompt or Powershell

`winget install microsoft.git`

## Environment Setup
Extract downloaded files to a folder, I use C:\Developer for my development tools.

I put ninja.exe in CMake\bin folder

Open Windows Environment Variables dialog and modify PATH to add CMake/bin and w64devkit/bin

![Environment Variables](/images/path.png)

For C-C++ develpment I installed these Visual Studio Code plugins:
![Plugins](/images/plugins.png)

## Hello 
To test if my setup is working I created a simple hello program.
to build, use this command in command prompt or Powershell

`make clean build`

