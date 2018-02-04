# 17.37 SetDoubleTapLength 

Set maximum length of double tap detection in milliseconds 

Syntax: `SetDoubleTapLength(max ms=700)` 

* `max` ms maximum length in milliseconds for double tap detection 

Notes: Window for double tap detection is set from 50ms to user defined value. Standard length is 700ms, minimum length for double tap detection is 100ms. 

Example: 

* `SetDoubleTapLength(200)`, sets double tap detection length to 200ms 
* `SetDoubleTapLength()`, sets double tap detection length to 700ms 

See also: Motion, AckMotion

