## Some more fun with Hello World

Let's get started with Futuro cube programming and the RFS, step by step with another 'hello world' program.

This app will create a Matrix-style waterfall of green lights around the cube constantly until you exit the app with a menu gesture.

* First you'll need to make a directory that contains your new Futuro projects

```
$ cd ~
$ mkdir futuro
$ cd futuro
```


* In this directory, you'll need to store the Futuro library
  * You can download it from [here](http://isle.princip.cz/download/futurocube/sdk_examples/futurocube.inc)
* Save this file to your new `futuro` directory
* Create a new file called `hello-world.p`
* Now is the time to fire up your favourite text editor/IDE
  * Open up your `hello-world.p` file
  * Add these lines:

  This first line will tell Pawn you want to use the futuro api library:
  ```
  #include <futurocube>
  ```
  All games/apps must have a main function that runs the app:
  ```
  // Initialize variables to be used later on
  new c
  new j
  new cursorSide
  new square = 0

  // Set a green 'M' as the icon
  new icon[] = [ICON_MAGIC1, ICON_MAGIC2, 1, 4,
      cGREEN,0, cGREEN, cGREEN, cGREEN, cGREEN, cGREEN, 0, cGREEN,
      '''', '''']

  main()
  {
    // Initialize the icon
    ICON(icon)
    for (j = 0; j < 1; j++)
    {
      // Change this hex code to try differenct colours
      SetColor(0x00FF0000)
      // Get cursor lets the RFC know which square is at the top
      c = GetCursor()
      // _side finds the side that the square passed to it is on
      cursorSide = _side(c)
      for(;;) {
        // Calls the function declared below
        lightSide(cursorSide, square)
        // Delay enables you to see the squares lighting up - otherwise, they will be too fast to see!
        Delay(50)
        // Changing the square for the next lighting up function call
        switch (square)
        {
          case 0: square = 3
          case 1: square = 4
          case 2: square = 5
          case 3: square = 6
          case 4: square = 7
          case 5: square = 8
          case 6: square = 1
          case 7: square = 2
          case 8: {
            square = 0
            if (cursorSide == 5) {
              cursorSide = 0
            } else {
              cursorSide++
            }
          }
        }
      }
    }
  }

  lightSide(side, light) {
    ClearCanvas()
    DrawPoint(_w(side, light))
    PrintCanvas()
    printf("side: %d, square: %d\r\n", side, light)
  }
  ```

Save this file.

Back in the RFC, click on `selected script` and find this file.

Click 'run after upload'.

Click 'compile and upload to flash'.

You should now see the 'matrix lights' flowing across the top side of the cube.
Rotate the cube and the new top side will light up.

Use the shake motion to stop the application.