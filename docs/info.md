<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works

This project generates a VGA signal (640x480 @ 60Hz) using an `hvsync_generator` module for sync timing. The design produces moving color bar patterns by combining pixel coordinates with a frame counter that increments each vertical sync period. The R, G, and B channels are driven by different bit slices of the offset pixel position, creating a scrolling stripe effect.

## How to test

Connect the VGA outputs to a TinyVGA PMOD and plug into a VGA monitor. Apply a 25.175 MHz clock and release reset (rst_n high). You should see animated color bars scrolling across the display.

## External hardware

TinyVGA PMOD connected to the dedicated output pins (uo_out).
