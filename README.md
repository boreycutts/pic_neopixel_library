# PIC NeoPixel Library 
A library used to emulate the Adafruit NeoPixel Library functionality on PIC based microcontrollers. Still a WIP, would like to fix brightness issues and add some more functionalities from the Arduino library

## MPLAB Setup
Create a project in MPLAB and copy `neopixel.h` to the `Header Files` folder and `neopixel.c` to the `Source Files` folder in your main project directory

Put `#include "neopixel.h"` at the top of your `main.c` file and you're done

## Usage
This is meant to work exactly like the Arduino library so everything should be pretty familiar:

**`setPixelColor(int i, int * color)`** - sets the pixel `i` with an RGB color. The variable color should be an integer array of 3 values from 1 to 255

**`show()`** - updates the LED strip with the values set by `setPixelColor`

**Example:**
```
int green[3] = {100, 1, 1};
int zero[3] = {1, 1, 1};

setPixelColor(0, green);
setPixelColor(1, green);
setPixelColor(2, green);
setPixelColor(3, zero);
setPixelColor(4, zero);
setPixelColor(5, zero);

show();
```