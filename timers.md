# Timers

Futuro Cube offers 10 countdown timers for various usage.

Timers can be paused and resumed.

The can be set up in milliseconds, however it is important to understand that the shortest interval and also actual granularity is 8ms.

That is the minimum tick for scheduling a script application.

If `Sleep()` is called, it is the same as if `Delay(2)` or `Delay(8)` were called instead.