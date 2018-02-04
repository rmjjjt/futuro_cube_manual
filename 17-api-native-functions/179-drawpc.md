# 17.9 DrawPC

Draw point with given color and intensity

Syntax: `DrawPC(wi, color, int=128)`

* `wi` walker or square index 
* `color` requested color 
* `int` requested intensity 

Notes: Draw spot with given color and intensity to the place defined by the walker or index passed. Given values do not modify current color and current intensity. **They apply just for one call of this function. **

Example:

* `DrawPC(GetCursor(),WHITE)`, draw a white spot at the cursor 
* `DrawPC(2,cORANGE,256)`, draw to square index 2 `cORANGE` with max intensity 

See also: [DrawPoint](/17-api-native-functions/178-drawpoint.md), [DrawSide](/17-api-native-functions/1710-drawside.md), [DrawSquare](/17-api-native-functions/1711-drawsquare.md), [DrawCross](/17-api-native-functions/1713-drawcross.md)

