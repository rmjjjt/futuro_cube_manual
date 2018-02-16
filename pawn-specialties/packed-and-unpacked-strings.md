# 7.4 Packed and unpacked strings 

PAWN uses packed and unpacked strings. 

**Packed string** means that it will compress as many characters as possible into one cell and **unpacked** means that one cell contains only one character. 

How the string is constructed depends on the quotation marks: ”stands for packed string” and ”unpacked string”. 

Using unpacked string is safer if you want to access the string as an array. Then you can address characters directly. 

If you don’t need this, then for saving memory, it is good to use packed strings. If any native function uses strings, it does not matter if is packed or unpacked. If you don’t want to bother yourself with that, always use unpacked! 

Examples follows:

```c
Play("music") // music is a packed string
new str[]=’’ahoj’’ // ahoj is unpacked
printf("%c\r\n",str[1]) // result is ’h’
```



