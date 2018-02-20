# DrawFlicker

Draw cursor type blinking spot

Syntax: `DrawFlicker(wi,speed=20,type=0,phase=0)`

* `wi` walker or spot index 
* `speed` blinking speed. This value is used in each frame to adjust the spot 
* `type` type of flicker, [FLICK STD](/api-native-functions/flicker-type-definition.md) or [FLICK RAZ](/api-native-functions/flicker-type-definition.md) 
* `phase` this value adjusts the phase of the blinking. It can be in range &lt;-127...127&gt;

  Notes: In order to make this function work properly, it must be called repeatedly during drawing. It actually just draws a spot of the current color, but it calculates it's intensity from given values and current frame counter. Therefore, it creates a nicely blinking spot on the virtual canvas.

Example: `DrawFlicker(GetCursor())`

See also: [GetCursor](/api-native-functions/getcursor.md)

