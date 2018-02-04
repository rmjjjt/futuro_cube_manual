# 17.25 FlashCanvas 

Prints virtual canvas to LEDs with fading attributes 

Syntax: `FlashCanvas(step=1,diff=3,exclusive=0)`

* `step` indicates occurrence of fade towards frame counter, 
  * value 1 means proceed with fade every new frame
  * value 2 means every second frame
* `diff` indicates what value will be subtracted from each color component every step exclusive if the parameter is set to 1, than LEDS are updated only if their value was zero. That means if they were for example still fading from previous call, their values are not overriden 

Notes: This function is usually used for some graphical effects, where canvas is not needed to be updated so often 

Example: `FlashCanvas` 

See also: PrintCanvas, ClearCube

