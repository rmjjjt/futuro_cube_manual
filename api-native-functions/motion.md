## Motion

Detects if any registered motion pattern has been recognized

Syntax: `type = Motion()`

Returns: This function returns a number, that has set bits at positions that corresponds to recognized registered [motion patterns](/api-native-functions/motion-pattern-type-list-definition.md).

Notes: If for example more than one [pattern](/api-native-functions/motion-pattern-type-list-definition.md) is registered, then output from this function should be tested for each pattern separately. The typical way is to use predefined macros, which are testing if the bit on it's specified position is set or reset.

Example:

* `motion = Motion()`, variable motion holds information about recognized patterns
* `if (motion) {...}` if there is any motion, we should handle it
* `if (_is(motion, TAP_XPLUS)) {...}` if the motion is specifically `TAP_XPLUS`, we should handle it

See also: [RegMotion](/api-native-functions/regmotion.md), [AckMotion](/api-native-functions/ackmotion.md), [RegAllSideTaps](/api-native-functions/regallsidetaps.md), [UnregAllMotion](/api-native-functions/unregallmotion.md)

