# 17.39 AckMotion

Acknowledge reception of recognized motion patterns

Syntax: `AckMotion()`

Notes: This function tells  the system you have received and served all recognized [motion patterns](/17-api-native-functions/1735-motion-pattern-type-list-definition.md) previously obtained from [Motion\(\)](/17-api-native-functions/1738-motion.md) and therefore any new motion pattern can be recognized. If this function is not called, bits on output from `Motion()` remain set as if there is still some pattern presented.

Example: `AckMotion()`

See also: [RegMotion](/17-api-native-functions/1736-regmotion.md), [Motion](/17-api-native-functions/1738-motion.md), [RegAllSideTaps](/17-api-native-functions/1740-regallsidetaps.md), [UnregAllMotion](/17-api-native-functions/1742-unregallmotion.md)

