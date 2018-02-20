# PauseTimer

Pause one of the 10 countdown timers

Syntax: `PauseTimer(timer=0)`

* `timer` available timer &lt;0...9&gt;

Notes: Timer remains paused until ResumeTimer() or [SetTimer()](/api-native-functions/settimer.md) is called.

Example:

* `PauseTimer()`, pause timer 0
* `PauseTimer(2)`, pause timer 2

See also: [SetTimer](/api-native-functions/settimer.md), [ResumeTimer](/api-native-functions/resumetimer.md)

