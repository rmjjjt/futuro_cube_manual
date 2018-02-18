# _w

Creates initialized walker with it's default direction

Syntax: `_w(side, square = -1)`

* `side` side number or index number of square
* `square` square number

Returns: Returns initialized walker with it's default direction.

Notes: Input to this function can be either side and square number, or just square index. The second case is used if square argument is used with it's default value.

Example:

* `walk = w(4)`, initialized walk to square index number 4
* `walk = w(4, 3)`, initialized walk to side 4, square 3

See also: [WalkerMove](/api-native-functions/walkermove.md), [WalkerTurn](/api-native-functions/walkerturn.md)

