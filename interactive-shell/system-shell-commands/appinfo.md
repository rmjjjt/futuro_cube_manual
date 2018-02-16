# appinfo

Displays various information about FW and it's memory map/usage.

Syntax: `appinfo`

```
$>appinfo
Application info:

Flash size: 393216 bytes, available: 15% (34580 bytes)
Bootloader size: 40960 bytes
Application size: 205036 bytes
Available size for app: 239616 bytes
Script area size: 71680 bytes, start at 0x08044800, end at 0x08055FFF
Variables size: 40960 bytes, start at 0x08056000
BootKey data size: 256 bytes.
NoInit data size: 2048 bytes.
Init data size: 1108 bytes.
UnInit data size: 57376 bytes.
RAM used: 60792/65536 bytes, 92% used.
RAM bootkey starts at: 0x20000000
RAM noinit starts at: 0x20000100
RAM init starts at: 0x20000900
RAM uninit starts: 0x20000d58 bytes
RAM free for stack: 4744 bytes
stext: 0x8000000
appstart: 0x800a000
etext: 0x803bc98
sdata: 0x20000900
edata: 0x20000d54
sbss: 0x20000d58
ebss: 0x2000ed78

$>
```