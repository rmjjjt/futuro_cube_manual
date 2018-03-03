## SetRandomizeFlag

Enables or disables randomizing by accelerometer

Syntax: `SetRandomizeFlag(flag)`

* `flag` 1 - enables randomizing (default), 0 - disables randomizing

Notes: Regularly, the random number generator is irregularly read according to the lowest bits at accelerometer output.
But in some cases, it is necessary that the generator is predictable, this is done by disabling randomizing by accelerometer results in a stable sequence of data from the same random seed.

Example:

* `SetRandomizeFlag(1)`

See also: [GetRnd](/api-native-functions/getrnd.md), [SetRndSeed](/api-native-functions/setrndseed.md)