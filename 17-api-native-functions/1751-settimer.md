# 17.51 SetTimer

Sets in milliseconds one of 10 countdown timers

Syntax: `SetTimer(timer=1,value=1000)`

* `timer` available timer &lt;0...9&gt;

Notes: This function sets one of 10 available countdown timers to a value that represents the given milliseconds. From that point on, the counter is counting down to zero. This function also resumes the timer if it was paused.

Example:

* `SetTimer()`, set timer 0 to value 1000 milliseconds 
* `SetTimer(1,200)`, set timer 1 to value 200 milliseconds 

See also: [GetTimer](/17-api-native-functions/1752-gettimer.md), PauseTimer, ResumeTimer

