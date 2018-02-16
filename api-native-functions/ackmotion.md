# AckMotion

Acknowledge reception of recognized motion patterns

Syntax: `AckMotion()`

Notes: This function tells  the system you have received and served all recognized [motion patterns](/api-native-functions/motion-pattern-type-list-definition.md) previously obtained from [Motion\(\)](/api-native-functions/motion.md) and therefore any new motion pattern can be recognized. If this function is not called, bits on output from `Motion()` remain set as if there is still some pattern presented.

Example: `AckMotion()`

See also: [RegMotion](/api-native-functions/regmotion.md), [Motion](/api-native-functions/motion.md), [RegAllSideTaps](/api-native-functions/regallsidetaps.md), [UnregAllMotion](/api-native-functions/unregallmotion.md)