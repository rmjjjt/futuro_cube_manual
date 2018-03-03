## Hello world

Let's code, compile and run your first program.

**Prerequisites:**

* Install and run [Rubik's Futuro Cube Suite](http://www.futurocube.com/support/#sw), from now on, we mean: **RFCSuite **and **connect CUBE via USB cable to PC**.

* If RFCSuite correctly communicates with the cube, the cube should turn black and the screen should look like this:

![](/assets/ConnectedRFCSuite.jpg)

* Now switch to **View-&gt;SDK mode**, you should see the SDK view and an available prompt given by [Interactive shell](/interactive-shell.md)

![](/assets/ViewSDKmode_small.jpg)

-&gt;

![](/assets/prompt.jpg)

* Just for fun type "**colh 0x55124800**" and hit enter - you should get the cube filled with the given color. For more information later, check [Colors, palettes and drawing](/colors-palettes-and-drawing.md) but for now let's get back to programming.

```
$>colh 0x55124800
r: 85(0x55), g: 18(0x12), b: 72(0x48), 0x55124800
__OK__
$>
```

---

Rubik’s Futuro Suite contains a standard PAWN compiler and allows you to compile scripts automatically with preset recommended stack and optimization settings (these can be adjusted by experienced user).

---

* Create a directory, where you will create your first program and download there API definition file called "**futurocube.inc"**. This is something like a header in C language and there is always a link on the[ SDK page](http://www.futurocube.com/sdk/) to the latest version.

* In you favorite text editor create a file called **hello.p** (**p** extension is necessary for RFCSuite to find this file). Simply copy, paste and save there the next few lines:

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

