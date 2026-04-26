# Project README

## Overview
The project is a simple graphical application to demonstrate the use of Perlin Noise in generating 1D patterns. It uses a custom windowing library for different platforms (Linux, Windows, Wine, and Web).

## Features
- Generates 1D Perlin Noise patterns.
- Displays the noise pattern as a line graph.
- Supports real-time updates by adjusting parameters.
- Provides basic user interaction to control the noise generation.

## Project Structure
```
<Project>/
├── build/              # .exe files produced by Main.c
├── src/                # source code
│   ├── Main.c          # Entry point
│   └── *.h             # stand alone Header-based C-files, without *.c files that implement it
├── Makefile.linux      # Linux Build configuration
├── Makefile.windows    # Windows Build configuration
├── Makefile.wine       # Wine Build configuration
├── Makefile.web        # Emscripten Build configuration
└── README.md           # This file
└── LICENSE             # Project License file
```

## Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- Libraries needed for specific projects:
  - Linux: X11
  - Windows: WINAPI
  - Wine: user32, gdi32, winmm
  - WebAssembly: Emscripten

## Build & Run
To build and run the project on different platforms:

### Linux
```sh
cd <Project>
make -f Makefile.linux all
make -f Makefile.linux exe
```

### Windows
```sh
cd <Project>
make -f Makefile.windows all
make -f Makefile.windows exe
```

### Wine (Cross-compile for Windows)
```sh
cd <Project>
make -f Makefile.wine all
make -f Makefile.wine exe
```

### WebAssembly (Emscripten)
```sh
cd <Project>
make -f Makefile.web all
make -f Makefile.web exe
```

These commands will build the project and produce an executable or HTML file in the `build/` directory. The application can then be executed using the appropriate method for each platform.