# Interactive shell

When Rubik’s Futuro Cube is connected to a PC, it is possible to communicate with the cube using 
the interactive command shell.

The shell can be easily accessed from Rubik's Futuro Cube Suite, but is available for other 
applications as well, because USB communication on the cube provides a common **VIRTUAL COM PORT**.

Before accessing the shell from other applications it is recommended to cycle USB to reset 
communication on character basis. This eventually resets more complex communication schemes.   
Note that in this case, characters are not automatically sent back to the terminal. Use command [echoon](/interactive_shell/echoon.md) if needed.