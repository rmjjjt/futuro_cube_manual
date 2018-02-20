# DrawCross

Draw cross of specified length

Syntax: `DrawCross(wi, length=1)`

* `wi` walker or square index 
* `length` length of the arm of the cross 

Notes: Draw cross with center spot defined by walker or index with preset color and attributes.

Example:

* `DrawCross(walker)`, draws cross with center walker with length=1 
* `DrawCross(23,2)`, draws cross on index 23 with length=2 
* `DrawCross(_w(2,2),3)`, draws cross with center side 2, square 2 and length=3 

See also: [DrawSide](/api-native-functions/drawside.md), [DrawPoint](/api-native-functions/drawpoint.md)

