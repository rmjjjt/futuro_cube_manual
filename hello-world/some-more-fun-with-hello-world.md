## Some more fun with Hello World

Let's get started with Futuro cube programming and the RFS, step by step with a 'hello world' program:

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
  main()
  {
      SetColor(cORANGE)
      DrawSquare(GetCursor())
      PrintCanvas()
      printf("hello world\r\n")
  }
  ```




In order to access shell commands and compiling ability, once RFC Suite is started, use the "view" menu to enable SDK mode.

