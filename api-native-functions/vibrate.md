## Vibrate

Vibrate for given amount of milliseconds

Syntax: `Vibrate(msec = 100)`

* `msec` number of milliseconds for vibration

Notes: Maximum number of milliseconds is 5000. Each time this function is called,
vibration is blocked for double the amount of time.
`Vibrate(150)` blocks another call within the next 300 milliseconds.

Example:

* `if (IsGameResetRequest()) {...init game...}`

Notes: Maximum number of milliseconds is 5000. Each time this function is called,
vibration is block for double amount of time. Vibrate(150) blocks another
call within next 300 milliseconds.
Example: Vibrate(150), vibrates for 150 milliseconds
