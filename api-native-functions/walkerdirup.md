# WalkerDirUp 

Modifies walker direction to look up according to accelerometer output 

Syntax: `WalkerDirUp(w,all_dirs=1,threshold=50,past=0)` 

* `w` walker to be modified 
* `all_dirs` if set to 1, walker direction will be updated all around, if set to 0, only turns to left and right will be allowed 
* `threshold` gives minimum threshold for gravity, which is usually applied to the top side 
* `past` how far back in accelerometer data to use 

Returns: This function returns a value that represents what happens to the walker. 

* 0 no turn and acc data below threshold 
* 1 no turn but acc over threshold 
* 2 turn according to all dirs 

Notes: This function works with accelerometer data, so it is possible to add a threshold that must be overcome to perform the turn. This is useful if the change of direction is happening on the top side, where the biggest acceleration is masked. 

Example: 

* `WalkerDirUp(w)`, update walker w 
* `WalkerDirUp(w,0,100)`, update walker w only to turn right, left with threshold 100 

See also: [WalkerTap](/api-native-functions/walkertap.md)

