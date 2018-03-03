## GetTimer

Returns value of one of 10 countdown timers

Syntax: `res=GetTimer(timer=0)`

* `timer` available timer &lt;0...9&gt;

Returns: Current value of the timer, no lower than 0

Example:

* `res=GetTimer`, returns value of timer 0
* `res=GetTimer(2)`, returns value of timer 2
* `if (!TimerGet(0))`

See also: [SetTimer](/api-native-functions/settimer.md), [PauseTimer](/api-native-functions/pausetimer.md), [ResumeTimer](/api-native-functions/resumetimer.md)

