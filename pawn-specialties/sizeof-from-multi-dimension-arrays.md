# Sizeof from multi-dimension arrays 

With multi-dimensional arrays, the `sizeof` operator can return the number of elements in each dimension. For the last \(minor\) dimension, an element will again be a cell, but for the major dimension\(s\), an element is a sub-array.

```c
new matrix[3][2] = { { 1, 2 }, { 3, 4 }, { 5, 6 } }
printf("%d %d", sizeof matrix, sizeof matrix[]);
```

Output is 3 a 2!

