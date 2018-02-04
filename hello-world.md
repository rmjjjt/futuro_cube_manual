# 3 Hello world 

In order to access shell commands and compiling ability, once RFC Suite is started, use the "view" menu to enable SDK mode. 

Rubik’s Futuro Suite contains a standard PAWN compiler and allows you to compile scripts automatically with preset recommended stack and optimization settings \(these can be adjusted by the user\). 

The easiest way to start is to place the library [futurocube.inc](http://isle.princip.cz/download/futurocube/sdk_examples/futurocube.inc) in the same directory as your script,  then just select the script in the Futuro Suite and try to compile it - click "compile and upload to RAM". It will automatically search for imported libraries in the same folder. You may want to tick "run after upload" to automatically start your script on the connected Futuro Cube.

Rubik’s Futuro Suite does not contain a script editor, but any text editor can be used.

The introduction to most programming languages start with a “hello world” program, so let us do the same:

```c
#include <futurocube>

main()
{
    SetColor(cORANGE)
    DrawSquare(GetCursor())
    PrintCanvas()
    printf("hello world\r\n")
}
```



