# 17.67 WalkerMove

Move walker on the cubic surface

Syntax: `WalkerMove(w,step=STEP_FORWARD)`

* `w` walker that will be moved 
* `step` type of move to proceed with 

Returns: This function will return 1 if the walker went over the edge, otherwise returns 0.

Notes: The step parameter is one [step type](/17-api-native-functions/1764-step-definition.md).

Example:

* `WalkerMove(walk)`, move walk one step forward 
* `WalkerMove(walk,STEP_RIGHT)`, move walk one step to the right without turning 

See also: [WalkerTurn](/17-api-native-functions/1768-walkerturn.md), [\_w](/17-api-native-functions/1766-w.md)

