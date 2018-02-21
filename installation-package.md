# Installation packages

Well, you have created super cool game with lots of nice sounds and you want to share it with others. So let us make it in the easiest way for them. Let us prepare installation package, that can be drag & drop in Rubik's Futuro Cube Suite. 

We will use as nice example RedKB's Rubik's cube app: [http://www.futurocube.com/score/?view=GAME&game\_id=39](http://www.futurocube.com/score/?view=GAME&game_id=39) 

From the same page you can download [installation package](http://isle.princip.cz/download/futurocube/games_library/Rubiks_Cube_1_3.zip) and see the internal structure:

```
Rubiks_Cube_1_3.zip
|
|RUBIKS CUBE (directory)  //mandatory if you provide your own samples
|     sample1.wav         //during installation it creates directory
|     sample2.wav         //called "RUBIKS CUBE", which will be mounted
|     sample3.wav         //with priority when the script starts
|     sample4.wav         //in order to work it like that, ICON SCRIPT NAME
|     sample5.wav         //must match folder name, see bellow
|     ...
|     game_name.wav       //optional name and explantion linked from ICON 
|     game_expl.wav       //again those files are searched in preffered folder
|     ...
|
|futurocube.inc           //API definition file used for compiling - not mandatory
|Rubiks_Cube_1_3.p        //source code - not mandatory
|Rubiks_Cube_1_3.amx      //compiled game, that is going to be installed - MANDATORY
|                         //this file is searched by RFCSuite and installed
```

It is important, that ICON is filled correctly, let us have a look at Rubik's app:

```
new icon[]=[ICON_MAGIC1,                                    
            ICON_MAGIC2,
            0,0,
            BLUE,0x20970000,0xFF740000,
            0xFFA36700,0xFFA36700,RED,
            0xFF1C0000,0x20970000,0xFF740000,
            ''rubiks_cube'',
            ''rubiks_desc'',
            ICON_MAGIC3,
            ''RUBIKS CUBE'',1,3,
            SCORE_BEST_IS_MIN|
            SCORE_PRIMARY_TIME|
            SCORE_SECONDARY_POINTS|
            SCORE_DISP_PTIME_MS|
            SCORE_DISP_SECONDARY]
            
//somewhere in code:            
...
main()
{
    ICON(icon)
    ...
```









