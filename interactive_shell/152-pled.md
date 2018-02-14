# 15.2 pled 

Lights up leds according PAWN numbering. 

Syntax: `pled side square led pwm side side number`

* `side` : `side number <0,5>` ,this value can be higher than 100, then ”clr” is performed and 100 is subtracted
* `square` : `square number <0,8>`
* `led` : `led number <0,3>` if 3, it means all colors **WHITE**
* `pwm` : `intensity <0,255>`

 Note: Intensity range is always scaled to actual PWM turnover. For most of the cases it is 64. Therefore, intensity is divided by 4.

