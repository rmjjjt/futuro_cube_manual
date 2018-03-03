## Useful macros

Useful defined macros
```
INDEX MASK        0x000000FF, mask for retrieving index
_i(val)           (val&INDEX MASK), index macro
_is(data,bit)     (data&(1<<bit)), test bit macro
_side(index)      (index/9)
_square(index)    (index%9)
abs(val)          ((val) < 0 ? -(val) : (val))
min(a,b)          (a < b ? a : b)
max(a,b)          (a > b ? a : b)
```