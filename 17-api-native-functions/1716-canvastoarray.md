# 17.16 CanvasToArray

Store virtual canvas to array

Syntax: `CanvasToArray(arr[],size=sizeof arr)`

* `arr[]` destination array 
* `size` size of the array. Must be 54, otherwise exception is raised 

Returns: Function always returns 0

Notes: This function basically copies the virtual canvas to a user's array.

Example: `CanvasToArray(temp)`, stores canvas to array temp

See also: [ArrayToCanvas](/17-api-native-functions/1717-arraytocanvas.md), [Push](/17-api-native-functions/1760-push.md), [Pop](/17-api-native-functions/1761-pop.md), [PushPopInit](/17-api-native-functions/1759-pushpopinit.md)

