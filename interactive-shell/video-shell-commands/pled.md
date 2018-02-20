# pled

Lights up leds according to PAWN numbering.

Syntax: `pled side square ledRGBselect intesity`

* `side` : `side number <0,5>` , this value can be higher than 100, then ”clr” is performed and 100 is subtracted
* `square` : `square number <0,8>`
* `ledRGBselect` : `0-red 1-green, 2-blue, 3-white (R+G+B)`
* `intensity` : `value <0,255>`

Note: Intensity range is always scaled to actual PWM turnover. For most of the cases it is 64. Therefore, intensity is divided by 4 internally.

```
$>pled 0 0 3 255           //this turns on white spot on side 0, square 0   
__OK__
$>pled 0 1 2 255           //this turns on blue spot on side 0, square 1       
__OK__
$>pled 0 2 0 255           //this turns on red spot on side 0, square 3   
__OK__
$>pled 100 3 1 255         //this clears LEDs first and turns on green spot on side 0, square 3   
__OK__
```



