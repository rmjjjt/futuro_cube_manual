# Default parameters

This is a beautiful feature of PAWN known from higher languages.

Definition of a function can be done with some parameters having default values. Later, when calling this function, the parameter does not have to be passed.

Many functions are structured in way that these default parameters are in last place and during call, they are simply not mentioned.

```
// Function definition
AdjArray(arr[], pintensity, startindex = 0, count = sizeof arr, size = sizeof arr)
{
    ...
}

AdjArray(ground, 20)
// ... calls AdjArray(ground, 20, 0, sizeof(ground), sizeof(ground))

AdjArray(ground, 10, _, 5)
// ... calls AdjArray(ground, 10, 0, 5, sizeof(ground))
// ’_’ means to use the already-specified default value, it is used if the param is not last in the list of arguments
```



