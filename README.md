# C-basicconfig-cmake
Boilerplate template code for configuring C++ basic configuration on VS code, and cmake

## **Table of Contents**

1. [Basic Configuration for C++ to run on VS code](#basicconfig)
2. [CMake](#cmake)

## **Basic Configuration for C++ to run on VS code**
Ensure you have the following installed:
- g++
- VS code
- C/C++ Extensions on VS code
- gdb (GNU debugger)

Configure your file so that the `launch.json` and `tasks.json` look like the ones located in the repository (note that this repository is running Arch linux on WSL).
Notice that the `program` in `launch.json` looks like the following:
```
"program": "${workspaceFolder}/main",  // Adjust this path to point to your executable
```
This is because the executable here is main.cpp, so that means that if the main executable is named differently, this will have to be changed too.

Also note that `"miDebuggerPath": "/usr/bin/gdb", ` this path has to be correct in order for VS code to know where gdb is within `launch.json`

## **CMake**
The [VS code documentation](https://code.visualstudio.com/docs/cpp/cmake-linux) on how to get Cmake tools work is quite complete, below are some of the things that are outlined in the tutorial

### Prerequisites
1. Visual Studio Code
2. C++ Extension for VS code
3. CMake Tools Extension for VS Code
4. CMake
5. Compiler (g++)
6. Debugger (gdb)
7. Build Tools (Ninja or make)

The build tools being referred to here are tools required for building the configuration that CMake needs. You could either install [ninja](https://ninja-build.org/) or [make](https://gnuwin32.sourceforge.net/packages/make.htm). `ninja` is known for its fast build times and `make` has been around for longer.

You'll also need to configure a CMake project by following the [tutorial](https://code.visualstudio.com/docs/cpp/cmake-quickstart), the quickstart in VS code's command palette does this neatly.

The 1CMakeLists.txt` and `CMakePresets.json` produced by CMake should resemble something like the ones found in this repository.
