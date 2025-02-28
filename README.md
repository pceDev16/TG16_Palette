﻿# Turbografx Palette Generator

## What is it?
For years, people had assumed that the PC Engine's composite output was simply an encoded version of the RGB colors output from the video processor. No stock releases of the TG16 or PC Engines had RGB output by default, so composite was the de-facto standard for the system. Some screenshots which showed some color scenarios that were clearly not intended by the artist led to a search for why the RGB colors and Composite output didn't match well. Furrtek decapped the encoder and discovered that there was a lookup table of values that was indexed by the RGB color, but did not linearly reflect these values.

After much trial and error I used this dumped LUT to find a reasonable approximation of the color math that matched vectorscope plots provided by Artemio. The code here uses this math to generate palette files for use in emulation.

## Building
To build, simply compile with gcc or clang using the `gcc -o tg16color tg16color.c -lm` command. Simply running the program will generate the palettes with no input from the user.
