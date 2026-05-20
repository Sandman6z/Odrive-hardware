# ODriveHardware

**!Bug !Bug !Bug**

When I design my PCB project, I forked from Odrive official repository. [ODriveHardware](https://github.com/odriverobotics/ODriveHardware) 
However, the PCB project under /v3 have some different with schmetic in /v3/v3.5docs.
After I find too much data, and ask AI, and other opensource projects, like `oshwhub`. They all told me that use v3.5 schmetic not the one under repository root.
Such a big oolong.

***And another one thing. The schematics of version 3.6 are basically the same as those of version 3.5. Only the voltage resistance of the capacitor has been changed due to firmware adjustments.***


---

This project is all about accuratly driving brushless motors, for cheap. The aim is to make it possible to use inexpensive brushless motors in high performance robotics projects.

If you want to get your hands on a board, check out [this post](https://hackaday.io/project/11583-odrive-high-performance-motor-control/log/40702-boards-and-development).

This repository contains the circuit board design of ODrive. The other related repositories are:
* [ODriveFirmware](https://github.com/madcowswe/ODriveFirmware): Firmware that runs on the board.
* [ODrive](https://github.com/madcowswe/ODrive): Configuration and analysis scripts that runs on a PC.

There is also [ODriveFPGA](https://github.com/madcowswe/ODriveFPGA), which contains the FPGA logic and software that runs on the FPGA based ODrive. This is not currently in development, but may be resumed at some later date.

## Odrive v3 board
The pinout from the microcontroller to the board is documented [here](https://docs.google.com/spreadsheets/d/1QXDCs1IRtUyG__M_9WruWOheywb-GhOwFtfPcHuN2Fg/edit?usp=sharing).

### Pictures!
![Odrive v3.1 top](https://cdn.hackaday.io/images/8135651482554401117.png)
![Odrive v3.1 bottom](https://cdn.hackaday.io/images/6142841482554487941.jpg)

### ODrive v3.1 errata
* The silkscreen labels for the encoders (M0, M1) are reversed.
* The output impedence of the current amplifiers were not considered when designing the post-amplifier filters. Hence the response is about 5x slower than designed. Max allowed modulation index is therefore about 50%.
