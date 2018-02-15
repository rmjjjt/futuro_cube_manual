# getms

Reads system time in mili seconds. This is the time from last RESET. Reset is usually caused by USB cycle.

**Note: This time measurement is not precise, since its ticks are based on MEMS sensors ODR. In longer time span, the will get some small offset. **

```
$>getms
931159
__OK__
$>
```

See also: [setms](/interactive_shell/system-shell-commands/setms.md)

