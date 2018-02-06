# 17.74 WalkerGetDir

Retreive direction vector from walker

Syntax: `WalkerGetDir(wlk,vect[3])`

* `wlk` walker for examination
* `vect[3]` vector of size 3 - where to store direction vector 

Notes: This function unpacks the direction vector from the structure of walker.

Example: `WalkerGetDir(wlk,dir)`, retrieves direction vector from `wlk` into `dir`

See also: [WalkerSetDir](/17-api-native-functions/1775-walkersetdir.md)

