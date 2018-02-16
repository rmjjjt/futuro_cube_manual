# FlashCanvas

Prints the virtual canvas to LEDs with fading attributes

Syntax: `FlashCanvas(step=1,diff=3,exclusive=0)`

* `step` indicates occurrence of fade towards frame counter, 
  * value 1 means proceed with fade every new frame
  * value 2 means every second frame
* `diff` indicates what value will be subtracted from each color component every step exclusively if the parameter is set to 1, then LEDS are updated only if their value was zero. This means that if they were, for example, still fading from a previous call, their values are not overridden 

Notes: This function is usually used for some graphical effects, where canvas is not needed to be updated so often

Example: `FlashCanvas()`

See also: [PrintCanvas](/api-native-functions/printcanvas.md), [ClearCube](/api-native-functions/clearcube.md)

