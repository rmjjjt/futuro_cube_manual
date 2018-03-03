## WalkerBuddy

Checks walker neighborhood and step suggestions

Syntax: `WalkerBuddy(wa,wb,step)`

* `wa` source walker for neighborhood check
* `wb` walker to check if is in neighborhood
* `step` place where suggested step will be stored

Returns: This function returns a value that represents the relationship between `wa` and `wb`.

* 0 `wa` is on same spot as `wb`
* 1 `wa` must do a perpendicular step to reach `wb`
* 2 `wa` must do a diagonal step to reach `wb`
* 3 `wa` is too far to reach `wb` in one single step

Notes: This function checks if `wb` is in close neighborhood to `wa`. It also suggests a step which `wa` can perform to reach the spot of `wb`. In case `wb` is too far away from `wa` number 3 is returned and step is filled by `STEP_NONE`.

Example:

* `if(WalkerBuddy(wa,wb,step)<3) {...}`,  if `wb` is close to `wa` do ...
* `WalkerBuddy(wa,wb,step)`, if `wb` is close to `wa`, put the step into step



