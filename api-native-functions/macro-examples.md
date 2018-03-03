## Macros examples

Typical situation where macros are used
```
// conversion of cursor square to array index
playground[_i(GetCursor())] = 1

// conversion of walker square to array index
playground[_i(walker)] = 1

// test for different sides
if (_side(prev) != _side(GetCursor())

// test for different indexes of squares
if (_i(prev) != _i(GetCursor())

// test for different squares numbers
if (_square(prev) != _square(GetCursor())

//center walker w at side given by cursor
w = _w(_side(GetCursor()), 4)

//test if double tap flag is set up
if (_is(motion,TAP_DOUBLE))
```