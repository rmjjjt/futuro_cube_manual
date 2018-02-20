# PushCanvas

Push virtual canvas to [Push Pop Array](/push-pop-arrays.md)

Syntax: `PushCanvas(ppindex=0)`

* `ppindex` push pop array number, default is 0 

Returns: Funtion returns error code as function Push

Notes: This function internally uses Push, so the `ppindex` array must be initialized

Example:

* `PushCanvas()`, push virtual canvas to array with index 0 
* `PushCanvas(1)`, push canvas to array with index 1 

See also: [PopCanvas](/api-native-functions/popcanvas.md), [Push](/api-native-functions/push.md), [Pop](/api-native-functions/pop.md), [PushPopInit](/api-native-functions/pushpopinit.md)

