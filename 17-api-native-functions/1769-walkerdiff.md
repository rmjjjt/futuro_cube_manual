# 17.69 WalkerDiff

Calculates distance in 2D coordinate system and hints the next step

Syntax: `WalkerDiff(wa,wb,dx,dy)`

* `wa` walker or index of spot A 
* `wb` walker or index of spot B 
* `dx` place to store the difference in x coordinate 
* `dy` place to store  thedifference in y coordinate 

Returns:

* Immediate return value gives [step type](/17-api-native-functions/1764-step-definition.md) describing how `wa` should continue to meet `wb`
* `STEP_NOTHING` walkers are at same spot or at opposite sides
* `STEP ...` if walker `wa` proceeds with this step, he will be closer to `wb`

Notes: `dx` and `dy` will contain values that represent the number of steps in each direction that walker `wa` would have to make to reach `wb` in the order of dx and dy. If `wa` would continue by the given suggested step and then ask for another one, finally it would reach `wb`. The returned step is determined by the highest absolute value between `dx` and `dy`. `dx` relates to `STEP_FORWARD` and `STEP_BACKWARDS`, while `dy` is `STEP_LEFT` and `STEP_RIGHT`. If `wa` is on the opposite side of `wb`, then `STEP_NOTHING` is performed and returned.

Example: `WalkerDiff(23, GetCursor(),dx,dy)`, difference from index 23 to actual cursor

See also: WalkerStepTo, GetCursor, ReadAcc

