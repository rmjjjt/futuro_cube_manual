## Icon

Insertion of icon and sound information into code

Syntax: `ICON(icon[])`

* `icon` array that defines icon and sound resources
  - `ICON MAGIC1` icon MAGIC1
  - `ICON MAGIC2` icon MAGIC2
  - `menu` menu number <0..2>, specifies which game menu to add the icon. Blue menu is number 0
  - `side` absolute side <0..5>, specifies which side of selected menu the icon should appear
  - `9 cells` nine colors that represent the icon on 3x3 matrix
  - `name` unpacked name of the sound file that represents the name of the script in menu
  - `expl` unpacked name of the sound file that represents the explanation of the script in menu

Notes: This function uses an icon array and therefore it is not removed from the
code during optimization. The array for icon must have a special format to be
recognized by the cube. Icon itself is a colorful icon that replaces a selected
game in the game menu and by tapping it, the user script is selected and started.
Icon has mandatory length and MAGIC fields. Additionally, two names of sound files for name and
explanation can be added into the icon array.

Example:

```
icon[]=[ICON_MAGIC1,ICON_MAGIC2,1,1,
RED,BLUE,RED,BLUE,RED,BLUE,GREEN,GREEN,GREEN,
’’INSTMR2’’,’’UFO’’]
```

```
icon[]=[ICON_MAGIC1,ICON_MAGIC2,1,1,
RED,BLUE,RED,BLUE,RED,BLUE,GREEN,GREEN,GREEN,
’’’’,’’’’]
```
```
ICON(icon)
```

Notes: The second example shows a case when sound resources are not setup.
If you do not want to use them, you should add empty unpacked strings for correct operation.
NOTE THAT ARRAY ”icon” MUST BE DEFINED IN THE GLOBAL NAME SPACE!!!
Otherwise the icon might be wrongly recognized in bytecode.
`ICON(icon)`, icon is used and will be recognized in byte code by the cube
