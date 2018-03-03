## WalkerMove

Move walker on the cubic surface

Syntax: `WalkerMove(w,step=STEP_FORWARD)`

* `w` walker that will be moved
* `step` type of move to proceed with

Returns: This function will return 1 if the walker went over the edge, otherwise returns 0.

Notes: The step parameter is one [step type](/api-native-functions/step-definition.md).

Example:

* `WalkerMove(walk)`, move walk one step forward
* `WalkerMove(walk,STEP_RIGHT)`, move walk one step to the right without turning

See also: [WalkerTurn](/api-native-functions/walkerturn.md), [_w](/api-native-functions/w.md)

