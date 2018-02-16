# 15.4 pledarr

Putting all LED values in an array at once.

Syntax: `pledarr pwmr0,pwmg0,pwmb0,pwmr1,pwmg1,pwmb1,.,.,.,.,.`

* `pwmr0` : intensity of RED led at index 0
* `pwmb0` : intensity of BLUE led at index 0
* `pwmg0` : intensity of GREEN led at index 0

Note: It is recommended to use `echooff` prior this function. Because echo works on character basis and for long commands it slows down the shell.

