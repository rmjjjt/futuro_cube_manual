## Starting scripts automatically

There is a special setting available that allows users to start scripts automatically either when the USB is plugged or unplugged.

Therefore, it is possible to replace the standard charging appearance or the script that can be started prior the **GAME MENU**.

The following commands are involved (see details in shell command specification).

In case both scripts have the same settings, then the FLASH script has priority.

```
setpawn type event // this command is obsolete from FW 4.5, see ”setpawnauto”
```

```
setpawnstd // puts settings into default state. This command is obsolete from FW 4.5
```

From FW 4.5 there is a more intelligent command `setpawnauto` which works with multiple scripts as well.

Scripts running during the charging process should not consume too much energy, because then the charging might be inefficient. In this case, the system might stop the script and start regular charging instead. Also, if any script runs instead of **MENU**, then if the **MENU GESTURE** is performed, **GAME MENU** starts as usual.

