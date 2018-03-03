## WalkerSetDir

Tries to apply given direction vector to walker

Syntax: `res=WalkerSetDir(wlk,vect[3])`

* `wlk` walker or index to be modified

Returns: Returns 1 if operation was successful or 0 if the operation failed. That means for example that this direction vector cannot be forced into the current spot.

Notes: Not all of the direction vectors can be forced to every spot over the cube, that is: one should be careful when using this function and also that is why this function returns 0 when the operation fails.

Example: `new vect[3]=[1,0,0]; WalkerSetDir(wlk,vect)`

See also: [WalkerGetDir](/api-native-functions/walkergetdir.md)

