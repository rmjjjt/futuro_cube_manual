# 17.46 Easy Tap Type Detection

Easier to use set of functions for tap type Detection

Syntax: `eTapSideOK()`

Notes: Checks if any valid SIDE TAP is detected. It is usually called before `eTapSide()` to confirm correct results. If, for example TAP\_GENERIC would be registered as well,  `eTapSide()` might give the wrong output, because if the function cannot confirm a valid tap, it returns 0.

Syntax: `eTapSide()`

Notes: Gives back number of the side that has been tapped. If the [motion patterns](/17-api-native-functions/1735-motion-pattern-type-list-definition.md) do not include any specific taps, it returns 0 as well. That is why it is good to use `eTapSideOK()`. If only sides taps are registered, then there is no problem.

Syntax: `eTapToSide()`

Notes: Returns 1 if the last tap was to a side. It takes top side from acc data, past=4

Syntax: `eTapToTop()`

Notes: Returns 1 if the last tap was to the top. It takes top side from acc data, past=4

Syntax: `eTapToBot()`

Notes: Returns 1 if the last tap was to the bottom. It takes top side from acc data, past=4

Example:

```c
if (eTapSideOK()) {
    side=eTapSide();
    // work with side
}
```

```c
if (eTapToTop) {...}
```

See also: [ReadAcc](/17-api-native-functions/1789-readacc.md)

