## PPFree

Number of free cells for [Push](/api-native-functions/push.md) in [Push Pop Array](/push-pop-arrays.md)

Syntax: `PPFree(ppindex=0)`

* `ppindex` index of PPArray arbiter &lt;0...3&gt;

Returns: Number of free cells to push.

Notes: Using this function ensures that the oldest `Push` will not be thrown away.

Example:

```c
if (PPFree() {
    Push(arr);
    ...
}
```

See also: [PPReady](/api-native-functions/ppready.md)

