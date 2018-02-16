# Shell cmd "motion"

`motion` is a special shell command that runs a task which outputs all important data for parsing outside of the cube.

Output rate is 125 Hz.

Structure and control sum is inspired at GPS output.

It is usually not necessary to check control sum when USB transfer is used.

No other messages can be in the middle of lines. However, there is a possibility that if you for example press enter, a prompt will be placed in front of the message. The prompt can be switched off and then there is, for example, the possibility to use command `ledarr...` without disturbing lines.

```
$MOT,0002,-254,0001,4,4,00,1,-,-,-,-,-*57
$MOT,-003,-255,-001,4,4,00,1,-,-,-,-,-*57
$MOT,-001,-249,-005,4,4,00,1,-,-,-,-,-*5C
$MOT,0004,-257,-003,4,4,00,1,-,-,-,-,-*4D
$MOT,-003,-253,-007,4,4,00,1,-,-,-,-,-*57
$MOT,-010,-249,-010,4,4,00,1,-,-,-,-,-*58
$MOT,-017,-251,-017,4,4,00,1,-,-,-,-,-*51
$MOT,-016,-254,-018,4,4,00,0,-,-,-,-,-*5B
$MOT,-015,-252,-013,4,4,00,0,-,-,-,-,-*55
```

```
MOT standard beginning
```

```
accx acc data x
```

```
accy acc data y
```

```
accz acc data z
```

```
side cursor side
```

```
square cursor square
```

```
shake shake percentage
```

```
still flag still flag "-" or "1"
```

```
still flag still flag
```

```
gtap generic tap "-" or "G"
```

```
tap side tap side "-" or "0..5"
```

```
tap type tap type "-" or "SIDE, TOP, BOT"
```

```
shake flag shake flag "-" or "R"
```

```
menu menu gesture flag "-" or "M"
```

```
control sum NMEA control sum
```