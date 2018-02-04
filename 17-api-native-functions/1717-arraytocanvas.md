# 17.17 ArrayToCanvas

Load virtual canvas from array

Syntax: `ArrayToCanvas(arr[],size=sizeof arr)`

* `arr[]` source array 
* `size` size of the array, must be 54, otherwise exception is raised 

Returns: Function always returns 0

Notes: This function basically copies user's array to the virtual canvas.

Example: `ArrayToCanvas(temp)`, store array temp to canvas

See also: [CanvasToArray](/17-api-native-functions/1716-canvastoarray.md), [Push](/17-api-native-functions/1760-push.md), [Pop](/17-api-native-functions/1761-pop.md), [PushPopInit](/17-api-native-functions/1759-pushpopinit.md)

