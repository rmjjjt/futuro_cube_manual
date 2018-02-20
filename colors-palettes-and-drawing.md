# Colors, palettes and drawing 

If we close our eyes a little, how correct is the physical representation of colors on the cube? 

We can use the following coloring scheme: 

Each color is represented by values of RED, GREEN and BLUE component. 

Each value can be from 0 to 255. 

In hexadecimal representation we will have: 0xRRGGBB00 

The last byte, which we left as 00 is used for indexing the color in the palette. 

The palette is an array of 256 colors and any time we want to draw color whose lower byte is **non-zero**, instead of taking it's actual RGB values, the index to the palette is taken and the color is retrieved from the palette array. This array must be preloaded before use, otherwise it contains zeros. 

All drawing is performed on to the so-called Virtual Canvas. After the drawing is finished, the Virtual Canvas can be printed on the physical surface of the cube. All functions that draw onto the Virtual Canvas can use several draw styles. For details see the `SetDrawStyle()` function.

