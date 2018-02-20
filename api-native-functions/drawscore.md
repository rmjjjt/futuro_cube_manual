# DrawScore

Example of drawing the score in the regular way

Syntax: `draw_score(side, number)`

* `side` side 
* `number` score

Notes: this function draws a number up to three digits, the same as [Score](score.md)

Example:
```
draw_score(side,number)
{
  new walker = _w(side, 0) //creates walker with default direction at square 0
  new i
  new h = number / 100
  number% = 100
  new t = number / 10
  number% = 10
  60
  new o = number
  if (h) DrawDigit(walker, h)
  for (i = 0; i < 3; i++) WalkerMove(walker, STEP_BACKWARDS)
  if (h || t ) DrawDigit(walker, t)
  for (i = 0; i < 3; i++) WalkerMove(walker, STEP_RIGHT)
  DrawDigit(walker, o)
}
```
