# 17.14 PushCanvas

Push virtual canvas to [Push Pop Array](/10-push-pop-arrays.md)

Syntax: `PushCanvas(ppindex=0)`

* `ppindex` push pop array number, default is 0 

Returns: Funtion returns error code as function Push

Notes: This function internally uses Push, so the `ppindex` array must be initialized

Example:

* `PushCanvas()`, push virtual canvas to array with index 0 
* `PushCanvas(1)`, push canvas to array with index 1 

See also: [PopCanvas](/17-api-native-functions/1715-popcanvas.md), [Push](/17-api-native-functions/1760-push.md), [Pop](/17-api-native-functions/1761-pop.md), [PushPopInit](/17-api-native-functions/1759-pushpopinit.md)

