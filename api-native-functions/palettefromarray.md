# PaletteFromArray 

Fill the palette with values from array 

Syntax: `PaletteFromArray(arr[],size=sizeof array)` 

* `arr` source array 
* `size` size of array, maximum size is 255 

Notes: This function will set up the palette from array. 

* Index 0 from array is stored into index 1 in palette. 
* Index 0 in palette is always 0. 

Example: 

```c
new parr[3]={WHITE,BLUE,RED}
PaletteFromArray(parr) // Set palette from parr
```



