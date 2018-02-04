# 17.63 PPFree 

Number of free cells for [Push](/17-api-native-functions/1760-push.md) in [Push Pop Array](/10-push-pop-arrays.md) 

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

See also: [PPReady](/17-api-native-functions/1762-ppready.md)

