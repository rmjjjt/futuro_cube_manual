# IsGameResetRequest

Game reset request from user

Syntax: `IsGameResetRequest()`

Notes: Function returns a positive value if during script start the user tapped the icon three 
times. This function is usually used with puzzles that store their state in variables.

Example:

* `if (IsGameResetRequest()) {...init game...}`