# Walkers, Squares, Indexes

Each square on the cube surface is defined by a specific **INDEX **or specific **SIDE** and **SQUARE** number.

These values are connected together by simple mathematics:

```
side = index / 9
square = index % 9
```

We can refer to squares either absolutely, that means we know their index, side and/or square, or we can place them on something called **WALKER**.

**WALKER** is a packed structure, that contains information not only about the position of the **WALKER** but also about its direction. This is very useful, because we can move **WALKER** forward, backward, rotate it etc. without paying attention what it's actual absolute position is.

Anytime after, we can retrieve information about it's position by simple predefined macros:

```
index = _i(walker)
side = _side(walker)
square = _square(walker)
```

Of course, the **WALKER** will always stick to the cube's surface, so moves correctly over the edges.

Many functions take **WALKER** directly as argument. For example, if we want to draw on the square defined by **WALKER** position, we simply use `DrawPoint(walker)`. We do not need to add any macros.

Oftentimes, we will construct **WALKER** from a known square index or known side and square:

```c
walker = _w(4, 4) // Defined by side and square
walker = _w(25) // Defined by specific index number
```

In these cases, **WALKER** will have it's default direction. You can use the debug function `DrawTail()` to display the orientation of the **WALKER** automatically.

Macro `i(...)`, which retrieves the index from the **WALKER,**  is very useful to look up the index into an array, that represents, for example, a playground area.

