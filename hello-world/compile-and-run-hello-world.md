## Compile and Run Hello World

* Set the file as Selected SCRIPT:

![](/assets/selectedScript.jpg)

* And now press **Compile and Upload to RAM** (later get detailed info at [Compiling, uploading and erasing scripts](/compiling-uploading-scripts.md)), output should look like this (we can exact compiler invoke commands and results):

```
$>
Run:
"D:\Programs\Rubik'sFuturoCubeSuite-SC1.8\bin\pawncc.exe" "hello.p" -i. -O3 -d1 -S512
Result:
"D:\Programs\Rubik'sFuturoCubeSuite-SC1.8\bin\pawncc.exe" "hello.p" -i. -O3 -d1 -S512

Pawn compiler 4.0.4733                  Copyright (c) 1997-2012, ITB CompuPhase


Compiling is done.
File length: 192 B, free RAM mem: 8192 B
Upload file: C:\RFC\hello.amx, sd:99
$>
```

We just have successfully compiled **hello.p** to **hello.amx** and uploaded to the RAM memory of the cube. Now we should run the program. We have 2 options and we will show you both. The **second one** is the most widely used.

## # 1. by shell command

If the script has been uploaded into RAM, we can simply use command [prun](/interactive-shell/prun.md):

```
$>prun
## ########################################### next lines are not important now ###################
$>Searching for registered variables.
added from RAM: 0
noscript in FLASH
noscript in MYCUBE
registered variables: 0
cleaning...
Registering for current script
found: 0
registered variables: 0
******
PAWN in RAM: 192 size, align size: 192, data/stack: 7996
******
...script info not complete...
******
script: MAGIC: 0x0000F1E0 (req: 0x0000F1E0)
size: 192 bytes, req: data/stack memory: 2064, available: 7996

amx_Init
--SCRIPT NFO--
base: 0x2000c244
code: 0x2000c284
d/st: 0x2000c304
offset heap: 0x00000010 (16)
offset sttp: 0x00001f3c (7996)
--FLAGS-------
--------------
script starting...
## ########################################### this is our output ##################################
hello world
## ########################################### rest is just exiting ################################
script returns: 0
no script!
```

TBD - picture from CorelDraw

As you can see our only text output **"hello world"** is a bit hidden by lots of other information, which we do not need to pay attention to right now, but on the top side of the cube, there should be a square.

## # 2. by RFCSuite - most common for development

![](/assets/run_and_stop.jpg)

If you check options above (**run after upload** and **stop script before compile**), you get a very nice and automated flow. Because, if the script has been compiled without errors, it is automatically uploaded either for RAM of FLASH and immediately started. We do recommend to check as well **stop script before compile** - this is very useful. If the previously running script has some extensive text outputs, you might miss what is going on during compilation...

