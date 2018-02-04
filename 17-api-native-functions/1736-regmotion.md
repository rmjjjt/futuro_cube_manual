# 17.36 RegMotion 

Register specific motion pattern for recognition 

Syntax: `RegMotion(type)` 

* `type` motion type from [pattern type list](/17-api-native-functions/1735-motion-pattern-type-list-definition.md) 

Notes: Motion type is defined basically by position of a bit in motion mask. Later, if new motion is detected, output from `Motion()`  has corresponding bit set to logic 1. By calling `RegMotion(...)` consequently, another pattern is added. 

Example: `RegMotion(TAP GENERIC)`, registers TAP GENERIC 

See also: Motion, AckMotion, RegAllSideTaps, UnregAllMotion

