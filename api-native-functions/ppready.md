## PPReady

Number of ready cells for [Pop](/api-native-functions/pop.md) in [Push Pop Array](/push-pop-arrays.md)

Syntax: `PPReady(ppindex=0)`

* `ppindex` index of PPArray arbiter &lt;0...3&gt;

Returns: Number of available cells to pop.

Notes: If there is the possibility to call `Pop` without being sure about available cells, then this function should be used to check it. Otherwise, an exception will be raised if `Pop` is performed on empty or not enough filled `PPArray`.

Example:

```c
if (PPReady() {
    Pop(arr);
    ...
}
```

See also: [Pop](/api-native-functions/pop.md)

