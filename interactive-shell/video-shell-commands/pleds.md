## pleds

Lights up whole side according PAWN numbering.

Syntax: `pled side ledRGBselect intesity`

* `side` : `side number <0,5>` , this value can be higher than 100, then ”clr” is performed and 100 is subtracted
* `ledRGBselect` : `0-red 1-green, 2-blue, 3-white (r+g+b)`
* `intensity` : `value <0,255>`

Note: Intensity range is always scaled to actual PWM turnover. For most of the cases it is 64. Therefore, intensity is divided by 4 internally.

```
$>pleds 0 3 255           //this turns on all white spots on side 0
__OK__
$>pleds 1 3 255           //this turns on all blue spots on side 1
__OK__
$>pleds 100 1 255         //this clears LEDs first and turns on all green spot on side 0
__OK__
```



