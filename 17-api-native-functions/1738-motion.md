# 17.38 Motion

Detects if any registered motion pattern has been recognized

Syntax: `type=Motion()`

Returns: This function returns a number, that has set bits at positions that corresponds to recognized registered [motion patterns](/17-api-native-functions/1735-motion-pattern-type-list-definition.md).

Notes: If for example more than one [pattern](/17-api-native-functions/1735-motion-pattern-type-list-definition.md) is registered, then output from this function should be tested for each pattern separately. The typical way is to use predefined macros, which are testing if the bit on it's specified position is set or reset.

Example:

* `motion=Motion()`, variable motion holds information about recognized patterns
* `if (motion) {...}` if there is any motion, we should handle it
* `if (_is(motion,TAP XPLUS)) {...}` if the motion is specifically `TAP XPLUS`, we should handle it

See also: [RegMotion](/17-api-native-functions/1736-regmotion.md), [AckMotion](/17-api-native-functions/1739-ackmotion.md), RegAllSideTaps, UnregAllMotion

