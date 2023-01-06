# Tiny collection of byte fonts

## Description

PushedDisplayFonts is a small collection of bit-defined fonts available in _const_ and _PROGMEM_ variations.

Is suits page addressing mode with 8-bit columns in page with top->bottom bit order in column.

Every font defines c++ASCII symbols from 32 to 127.

Each symbol defined as two-dimensional C++ array, where each sub-array represents page:

F.ex symbol that takes 3 pages and 20 columns looks like
{
  {0x0, ..., 0x0},  // page1 of 3
  {0x0, ..., 0x0},  // page2 of 3
  {0x0, ..., 0x0}   // page3 of 3
}

Note, that symbol definitions do not imply gap-columns at the edges and usually take up all allocated space

## Work in progress

- [x] 8x5 symbols (1 page, 5 cols)
- [x] 16x9 symbols (2 pages, 9 cols)
- [] 24x18 symbols (3 pages, 9 cols)
- [] iconic fonts
  - [] 5x5 status icons (1 page, 5 cols)
    - battery
    - wireless
    - bluetooth
    - numbers
  - [] 8x8 icons (1 page, 8 cols)
    - github
    - message
    - musical note
    - arrows and markers
    - temperature, humidity, co2 etc

## Requirements

1. C++ compiler with support of C++14 or later
2. Following header files in standard library:
  1. stdint.h (uintX_t type definitions)
  2. stddef.h (size_t definition)

## Compatibility

PushedDisplayFonts originally created to work with other Pushed display libraries.

It will nicely suite any other display library with same font structure.

## License

PushedDisplayFonts is free software, distributed without any warranty.

You can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 3, or (at your option) any later version.

Some separate files not so somplex or contain only simple definitions and you are free to use them
as standalone without any conditions as long as you credit me somewhere

## Have fun!
If you find this code useful, I will be glad if you use it in your GPL3-or-later-compatible licensed project.

**"Why GPL-3. Author, are you too proud?"**
> Nope. Just join us now and share the software.
> My code is neither perfect nor revolutionary. But the world is crazy, you know

Any help and criticism is greatly appreciated.