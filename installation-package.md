# Installation packages

Well, you have created super cool game with lots of nice sounds and you want to share it with others. So let us make it in the most easiest way for them. Let us create installation package, that can be installed automatically with drag & drop in Rubik's Futuro Cube Suite.

We will use as nice example RedKB's Rubik's cube app: [http://www.futurocube.com/score/?view=GAME&game\_id=39](http://www.futurocube.com/score/?view=GAME&game_id=39)

From the same page you can download [installation package](http://isle.princip.cz/download/futurocube/games_library/Rubiks_Cube_1_3.zip) and see the internal structure of the regular zip file:

```
Rubiks_Cube_1_3.zip
|
|RUBIKS CUBE (directory)  //mandatory if you provide your own samples
|     sample1.wav         //during installation it uploads this directory
|     sample2.wav         //called "RUBIKS CUBE", if the directory name matches 
|     sample3.wav         //script name defined in ICON, see bellow, 
|     sample4.wav         //this directory will be searched first for any request 
|     sample5.wav         //playback from the script including name and description
|     ...
|     game_name.wav       
|     game_desc.wav       
|     ...
|
|futurocube.inc           //API definition file used for compiling - not mandatory
|Rubiks_Cube_1_3.p        //source code - not mandatory
|Rubiks_Cube_1_3.amx      //compiled game, that is going to be installed - MANDATORY
|                         //this file is searched by RFCSuite and installed
```

It is important, that ICON is filled correctly and RFCSuite can identify it in bytecode, let us have a look at Rubik's app:

```
new icon[]=[ICON_MAGIC1,                       //magic1, that allows structure to be recognized
            ICON_MAGIC2,                       //magic2, that allows structure to be recognized
            0,0,                               //side and square of the installation, this will be
                                               //alternated by RFCSuite as you will decide where
                                               //you want the app be placed
            BLUE,0x20970000,0xFF740000,        //icon colors      0 1 2
            0xFFA36700,0xFFA36700,RED,         //icon colors      3 4 5
            0xFF1C0000,0x20970000,0xFF740000,  //icon colors      6 7 8
            ''rubiks_cube'',                   //name of the sound resources played as name of the game
                                               //if not used, leave empty '''', it must be unpacked
            ''rubiks_desc'',                   //name of the sound resources played as description of the game
                                               //if not used, leave empty '''', it must be unpacked
            ICON_MAGIC3,                       //magic3, that allows structure to be recognized
            ''RUBIKS CUBE'',1,3,               //this is name of the script that matches name of prefered folder
                                               //and version of the application, i.e. RUBIKS CUBE ver 1.3

            SCORE_BEST_IS_MIN|                 //score flags, read more in section OMLINE SCORE,
            SCORE_PRIMARY_TIME|                //leave 0 if no score is used
            SCORE_SECONDARY_POINTS|
            SCORE_DISP_PTIME_MS|
            SCORE_DISP_SECONDARY]

//somewhere in code:
...
main()
{
    ICON(icon)                   //array icon must be compiled and used
                                 //without this process of optimization
                                 //would remove it from the final bytecode
    ...
```

#### Good rules to follow

* Name of the package should contain the name and the version, in our case **Rubiks\_Cube\_1\_3.zip**
* Compiled script \(file with amx extension\) and source code \(file with p extension\) shall be named similary, i.e. **Rubiks\_Cube\_1\_3.amx** and **Rubiks\_Cube\_1\_3.amx.p**.** **
* ICON array inside amx file should match completely file names, i.e. **RUBIKS CUBE** as script name, and same version **1.3**.** **
* If you use your own created sound resources, create inside directory with same name as script name defined in ICON, in our case **RUBIKS CUBE**, this directory will be searched first for any playback.
* Installation package package can have multiple diretcories, but only one will be prioritized.
* Source code is not mandatory to include, but it is nice to have it there. Especially if someone wants to experiment with it.



