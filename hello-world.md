## Hello world

Let us code, compile and run your first program.

**Prerequisites:**

* Install and run [Rubik's Futuro Cube Suite](http://www.futurocube.com/support/#sw), we will call next time just **RFCSuite **and **connect CUBE via USB cable to PC**.

* If RFCSuite correctly communicates with cube, cube becomes black and screen should look like this:

![](/assets/ConnectedRFCSuite.jpg)

* Now switch to **View-&gt;SDK mode**, you should see SDK view and available prompt given by [Interactive shell](/interactive-shell.md)

![](/assets/ViewSDKmode_small.jpg)

-&gt;

![](/assets/prompt.jpg)

* Just for fun type "**colh 0x55124800**" and hit enter, you should get the cube filled by the given color, for more information later check [Colors, palettes and drawing](/colors-palettes-and-drawing.md), but now let us come back to programming.

```
$>colh 0x55124800
r: 85(0x55), g: 18(0x12), b: 72(0x48), 0x55124800
__OK__
$>
```

---

Rubik’s Futuro Suite contains a standard PAWN compiler and allows you to compile scripts automatically with preset recommended stack and optimization settings (these can be adjusted by experienced user).

---

* Create a directory, where you will have your first program and download there API definition file called "**futurocube.inc"** Something like header in C language, there is always[ link on SDK page](http://www.futurocube.com/sdk/) to the latest version.

* In you favorite text editor create file **hello.p** (**p** extension is neccesary for RFCSuite to find this file). Simply copy, paste and save there next lines:

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

Continue at [Compile and Run Hello World](/hello-world/compile-and-run-hello-world.md)

