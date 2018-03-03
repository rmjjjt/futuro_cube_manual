## PopCanvas

Pop virtual canvas from [Push Pop Array](/push-pop-arrays.md)

Syntax: `PushCanvas(ppindex=0)`

* `ppindex` push pop array number, default is 0

Returns: Funtion returns error code as function Pop

Notes: This function internally uses Pop, so the `ppindex` array must be initialized!

Example:

* `PopCanvas()`, pop canvas from array with index 0
* `PopCanvas(1)`, pop canvas from array with index 1

See also: [PushCanvas](/api-native-functions/pushcanvas.md), [Push](/api-native-functions/push.md), [Pop](/api-native-functions/pop.md), [PushPopInit](/api-native-functions/pushpopinit.md)

