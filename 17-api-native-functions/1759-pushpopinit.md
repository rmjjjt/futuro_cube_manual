# 17.59 PushPopInit

Initialization of [Push Pop Arrays](/10-push-pop-arrays.md)

Syntax: `PushPopInit(arr[],ppindex=0,size=sizeof arr)`

* `arr` array that will be used as Push Pop Array 
* `ppindex` index of available PPArray arbiter &lt;0...3&gt;
* `size` size of array to be stored into arbiter as initial size 

Notes: Before any usage of Push, Pop,  PushCanvas or PopCanvas, the array must be initialized.

Example:

* `PushPopInit(arr)`, initialized arbiter with index 0 with array arr 
* `PushPopInit(temp,1)`, initialized arbiter with index 1 with array temp 

See also: [Push](/17-api-native-functions/1760-push.md), [Pop](/17-api-native-functions/1761-pop.md)

