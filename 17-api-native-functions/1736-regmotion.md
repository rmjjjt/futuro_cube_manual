# 17.36 RegMotion

Register specific [motion pattern](/17-api-native-functions/1735-motion-pattern-type-list-definition.md) for recognition

Syntax: `RegMotion(type)`

* `type` motion type from [pattern type list](/17-api-native-functions/1735-motion-pattern-type-list-definition.md) 

Notes: Motion type is defined basically by position of a bit in motion mask. Later, if a new motion is detected, output from `Motion()`  has corresponding bit set to logic 1. By calling `RegMotion(...)` consequently, another pattern is added.

Example: `RegMotion(TAP GENERIC)`, registers TAP GENERIC

See also: [Motion](/17-api-native-functions/1738-motion.md), [AckMotion](/17-api-native-functions/1739-ackmotion.md), [RegAllSideTaps](/17-api-native-functions/1740-regallsidetaps.md), [UnregAllMotion](/17-api-native-functions/1742-unregallmotion.md)

