# 17.28 AdjCanvasPoint

Adjust intensity of the already drawn point

Syntax: `AdjCanvasPoint(wi,pint)`

* `wi` walker or spot index 
* `pint` percentage of new intensity. 0 means no change

Notes: This function changes intensity of a point which is already drawn. So, the color component might not be in the correct ratio if the change is big.

Example: `AdjCanvasPoint(GetCursor(),-20)`, decrease intensity under cursor to 20 percent

See also: [AdjCanvas](/17-api-native-functions/1729-adjcanvas.md), [AdjArray](/17-api-native-functions/1730-adjarray.md)

