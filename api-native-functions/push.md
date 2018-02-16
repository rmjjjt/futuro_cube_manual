# Push

Push array into [Push Pop Array](/push-pop-arrays.md)

Syntax: `Push(arr[],ppindex=0,size=sizeof arr)`

* `arr` array that is going to be pushed in 
* `ppindex` index of available PPArray arbiter &lt;0...3&gt;
* `size` size of pushed array 

Returns: Returns 1 if operation was successful, otherwise an exception is raised.

Notes: If the Push Pop Array is full, simply the oldest items are thrown away and lost. This must be considered as a possible effect to be aware of.

Example:

* `Push(arr)`, push arr into initialized array with index 0 
* `Push(temp,1)`, push temp into initialized array with index 1 

See also: [Pop](/api-native-functions/pop.md), [PPReady](/api-native-functions/ppready.md)

