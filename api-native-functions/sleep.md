## Sleep

Gives control to system and waits until new game accelerometer data arrives

Syntax: `Sleep(value=0)`

Notes: This function is essential for cooperative multitasking. It should be called after all events are processed. If the program does not call this function regularly, the system can block the task for non-cooperative behavior.

Example:

* `Sleep()`, most general use of sleep, waits for new data, gives time to system
* `Sleep(100)`, same as `Delay(100)`

See also: [Delay](/api-native-functions/delay.md)

