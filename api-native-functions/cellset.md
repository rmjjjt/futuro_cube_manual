# cellset

Sets the array to predefined constant

Syntax: `cellset(arr[],val=0,size=sizeof arr)`

* `arr[]` array to be filled by val 
* `val` value used for filling 
* `size` size of array 

Notes: This is similar function to memset. It basically puts the value into every cell in an array. The size of the array can be automatically inserted at runtime by using a standard value.

Example:

* `cellset(playground,20)`, fills whole playground array by value 20 
* `cellset(playground,20,3)`, fills first 3 cells by value 20 

See also: [cellcopy](/api-native-functions/cellcopy.md)

