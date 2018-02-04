# 17.53 PauseTimer

Pause one of the 10 countdown timers

Syntax: `PauseTimer(timer=0)`

* `timer` available timer &lt;0...9&gt;

Notes: Timer remains paused until ResumeTimer\(\) or [SetTimer\(\)](/17-api-native-functions/1751-settimer.md) is called. 

Example: 

* `PauseTimer()`, pause timer 0 
* `PauseTimer(2)`, pause timer 2 

See also: SetTimer, ResumeTimer

