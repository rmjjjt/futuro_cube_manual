## RegMotion

Register specific [motion pattern](/api-native-functions/motion-pattern-type-list-definition.md) for recognition

Syntax: `RegMotion(type)`

* `type` motion type from [pattern type list](/api-native-functions/motion-pattern-type-list-definition.md)

Notes: Motion type is defined basically by position of a bit in motion mask. Later, if a new motion is detected, output from `Motion()`  has corresponding bit set to logic 1. By calling `RegMotion(...)` consequently, another pattern is added.

Example: `RegMotion(TAP GENERIC)`, registers TAP GENERIC

See also: [Motion](/api-native-functions/motion.md), [AckMotion](/api-native-functions/ackmotion.md), [RegAllSideTaps](/api-native-functions/regallsidetaps.md), [UnregAllMotion](/api-native-functions/unregallmotion.md)

