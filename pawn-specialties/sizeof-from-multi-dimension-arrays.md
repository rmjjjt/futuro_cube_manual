## Sizeof from multi-dimension arrays

With multi-dimensional arrays, the `sizeof` operator can return the number of elements in each dimension. For the last (minor) dimension, an element will again be a cell, but for the major dimension(s), an element is a sub-array.

```c
new matrix[3][2] = [ [1, 2], [3, 4], [5, 6 ] ]
printf("%d %d", sizeof matrix, sizeof matrix[]);

3 2
```

**Be careful, because there is one sitution, where it does not work:**

```c
This works as expected:

new matrix[][] = [ [1, 2], [3, 4], [5, 6 ] ]
printf("%d %d", sizeof matrix, sizeof matrix[]);

3 2

This does not work (it is due to the fact that size of minor array is not same for all members):

new matrix[][] = [ [1, 2, 3], [3, 4], [5, 6 ] ]
printf("%d %d", sizeof matrix, sizeof matrix[]);

3 0         //!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

This works as expected:

new matrix[][7] = [ [1, 2, 3], [3, 4], [5, 6, 8, 9] ]
printf("%d %d", sizeof matrix, sizeof matrix[]);

3 7


```



