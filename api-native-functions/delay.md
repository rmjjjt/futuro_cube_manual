# Delay

Delays script by the given number of milliseconds

Syntax: `Delay(value=1000)`

* `value` delay time in milliseconds 

Notes: This function delays at least given millisecond. Internally uses `Sleep()` so the delay is fully cooperative.

Example:

* `Delay()` delays for 1 secs 
* `Delay(100)` delays for 100 milliseconds 

See also: [Sleep](/api-native-functions/sleep.md)

