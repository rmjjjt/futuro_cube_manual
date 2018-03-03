## Operator sizeof

Many functions are using `sizeof` operator as one of the default values.

The nice thing is that as in `AdjArray()` or `PrintArray()`, the size of the array `arr` is given at run time. And this value is usually used as a boundary inside the function. So, if it is really not needed, always leave this param out of the function and it will be passed correctly for you.

```c
// Function definition
AdjArray(arr[], pintensity, startindex = 0, count = sizeof arr, size = sizeof arr)
{
    ...
}
```

or

```c
PrintArray(arr[],size=sizeof arr)
{
    ....
}

//usage:

new cells[20]=[1,2,...]                          //this populates the array by 1,2,3,4,5,....
PrintArray(cells)
....
(  0) 00000001 00000002 00000003 00000004         ................
(  4) 00000005 00000006 00000007 00000008         ................
(  8) 00000009 0000000A 0000000B 0000000C         ................
( 12) 0000000D 0000000E 0000000F 00000010         ................
( 16) 00000011 00000012 00000013 00000014         ................
```

**NOTE: Sizeof packed strings or packed arrays won't give the number of elements, but always the number of cells! See more at** [Packed and unpacked](/pawn-specialties/packed-and-unpacked-strings.md)

**A few more examples:**

```c
new msg[4];               // sizeof msg is 4
new msg[]=[1,2,3,4,5]     // sizeof msg is 5
new msg[10]=[1,2,3,4]     // sizeof msg is 10, rest is filled by zeros

new msg[]=''hello''       // sizeof msg is 6, there is a zero at the end
new msg{}="hello"         // sizeof msg is 2, this is a packed string
new msg[]="hello"         // sizeof msg is still 2, but you get a warning for mixing indexing

new msg{}=[1,2,3,4]       // sizeof msg is 4, but you get a warning for mixing indexing
new msg{}={1,2,3,4}       // sizeof msg is 1, this is a packed structure
new msg{}={1,2,3,256}     // you get an error, because the last element is bigger than 255
                          // check more details at packed und unpacked description
```

**Note:** "sizeof" can be used either with braces or without, i.e. sizeof(msg) is equal to sizeof msg.

