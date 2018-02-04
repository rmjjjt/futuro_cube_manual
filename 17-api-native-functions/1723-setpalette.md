# 17.23 SetPalette 

Fill the palette with given color 

Syntax: `SetPalette(index,color)`

* `index` index in palette. Not 0, range &lt;1...255&gt;
* `color` color that will be stored at given index 

Notes: Palette at index zero has to contain zero value for color, therefore index zero is not accessible. By starting the script, palette values are reset to zero as well. 

Example: 

* `SetPalette(1,WHITE)`, set palette with index 1 to value WHITE 
* `SetPalette(2,0xABCD1100)`, set palette with index 2 to value 0xABCD1100



