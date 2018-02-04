# 17.43 GetTapSide 

Gives back the number of the side that has been tapped 

Syntax: `result=GetTapSide(side)` 

* `side` will contain number of side that has been tapped

Returns: Function returns 1 if the tap to side has been recognized, otherwise 0 

Notes: Function fill the side variable with value 0 to 5 according which side has been tapped. Function reads [Motion\(\)](/17-api-native-functions/1738-motion.md), so for correct operation, side taps must be registered. If you call [AckMotion\(\)](/17-api-native-functions/1739-ackmotion.md) prior this function, the result will become 0. 

Example: `if (GetTapSide(side)) {...work with side...}`

