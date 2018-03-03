## getms

Reads system time in milliseconds. This is the time from last RESET. Reset is usually caused by a USB cycle.

**Note: This time measurement is not precise, since it's ticks are based on MEMS sensors ODR. In longer time span, this will get some small offset. **

```
$>getms
931159
__OK__
$>
```

See also: [setms](setms.md)