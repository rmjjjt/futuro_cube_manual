## WalkerTap

Moves walker based on recognized taps toward side that has been tapped

Syntax: `WalkerTap(w,up_down_flag)`

* `w` walker to be moved

Returns: Returns the value that is related to the result of the move, also it fills `up_down_flag` by:

* -1 tap was from opposite side

* 1 - tap was from the same side

note that in the two above cases, the function returns 0 and no move has been processed.
It is up to user to decide what to do in such cases.

* 0 no move, either tap has not been recognized or is not registered, or the tap was either from the same or opposite side
* 1 walker moved 1 step toward the tap side
* 2 walker moved 1 step toward the tap side and went over the edge

Notes: For proper functionionality, all sidetaps must be registered, because inside this function motion output is read. Also walker itself is being turned to look towards the tap.

Example: `result=WalkerTap(w,up_down)`

See also: [WalkerDirUp](/api-native-functions/walkerdirup.md)

