## Packed and unpacked strings and arrays

Pawn is a typeless language and each piece of stored information takes one cell. The size of the cell depends on the platform. In our case, for Rubik's Futuro Cube, it is always 32bits, i.e four bytes. This makes the language easy to use, but for example storing **long texts** or in our case mostly some **maze definitions** or **levels** would take too much of the available memory. That is why PAWN introduced packed strings or arrays. If a piece of information can fit into 1 byte &lt;0..255&gt;, then everything takes 4 times less space in RAM.

**Packed string or array** means that it will compress as many characters/bytes as possible into one cell and **unpacked** means that one cell contains only one character/number.

How the string is constructed depends on the quotation marks: **"packed string"** and **' 'unpacked string' '**.

There is available **packed indexing "{index}"** and **unpacked indexing "[index]"**. Most functions working with text like `snprintf` or `sscanf` or similar usually take both options as input, but the output is mostly unpacked.

Next example shows how to work with it and how it is stored in memory:

```c
#include <futurocube>

main()
{
  new i

  new msg1[]=''hello''  // we are indexing msg1[0]...msg1[1]...
  for (i=0;i<sizeof(msg1);i++) printf("_%c",msg1[i]);
  printf("\nunpacked string representation in memory\n")
  PrintArray(msg1)
  printf("\n")

  new msg2{}="hello"    // we are indexing msg1{0}...msg1{1}...
  for (i=0;i<sizeof(msg2);i++) printf("_%c",msg2{i});
  printf("\npacked string representation in memory\n")
  printf("\n");
  PrintArray(msg2)
}

//output is

_h_e_l_l_o_
unpacked string representation in memory
(  0) 00000068 00000065 0000006C 0000006C         h...e...l...l...
(  4) 0000006F 00000000                           o.......

_h_e
packed string representation in memory

(  0) 68656C6C 6F000000                           lleh...o
```

**The second output is maybe not what you expected!**

```
_h_e
```

This is because operator **sizeof always only gives the number of used cells** and not the number of elements. In this case, it would be better to use something like `strlen`, but this function must be implemented separately.

Typical usage of the packed arrays are levels, mazes definitions or list of sound files. In the following examples, they occupy the least space possible:

```c
#include <futurocube>

new i

main()
{
  new songs[]{}=["song1","song2","song3"]

  for (i=0;i<sizeof(songs);i++) printf("%s\n",songs[i])

  for(;;)
  {
    Sleep()
    if (IsPlayOver())
    {
     Play(songs[GetRnd(sizeof songs)])
    }
  }

}
```

or

```c
new const train_levels[]{57} = [
//**************  LEVEL 1 ***************************
                                {'A','*','r',
                                 //--------//
                                 'S','D','x',
                                 ' ','x','x',
                                 ' ','x','x',
                                 //--------//
                                 'x',' ',' ',
                                 'x','x',' ',
                                 ' ','x','x',
                                 //--------//
                                 'x',' ','x',
                                 'x','x','x',
                                 ' ',' ',' ',
                                 //--------//
                                 ' ','x','x',
                                 ' ',' ',' ',
                                 ' ','x','x',
                                 //--------//
                                 'x',' ',' ',
                                 ' ',' ',' ',
                                 ' ',' ',' ',
                                 //--------//
                                 'x','x','x',
                                 ' ','x',' ',
                                 ' ','x','x',
                                },
//**************  LEVEL 2 ***************************
                                {'A','T','r',
                                 //--------//
                                 'x','x',' ',
                                 'x',' ',' ',
                                 ' ','x','x',
                                 //--------//
etc....
```





