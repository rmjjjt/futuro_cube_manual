## AdjArray

Adjust intensity of the array

Syntax: `AdjArray(arr[],pint,sindex=0,count=sizeof arr,size=sizeof arr)`

* `arr` array to be adjusted
* `pint` percentage of new intensity. 0 means no change
* `sindex` start index in array
* `count` number of cells to adjust in array
* `size` size of array

Example:

* `AdjArray(arr,-50)`, decrease intensity of `arr` to 50 percent
* `AdjArray(arr,50,20,2)`, decrease intensity of `arr[20]` and `arr[21]` to 50 percent



