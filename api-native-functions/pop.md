# Pop

Pop array from [Push Pop Array](/push-pop-arrays.md)

Syntax: `Push(arr[],ppindex=0,size=sizeof arr)`

* `arr` array that is going to be popped
* `ppindex` index of available PPArray arbiter &lt;0...3&gt;
* `size` size of popped array 

Returns: Returns 1 if the operation was successful, otherwise an exception is raised.

Notes: If the Push Pop Array is empty, or more than available cells are popped, an exception is raised as well

Example:

* `Pop(arr)`, pop `arr` from initialized array with index 0 
* `Pop(temp,1)`, pop `temp` from initialized array with index 1 

See also: [Push](/api-native-functions/push.md), [PPReady](/api-native-functions/ppready.md)

