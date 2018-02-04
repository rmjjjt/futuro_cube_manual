# 15 Shell commands 

When Rubik’s Futuro Cube is connected to Rubik’s Futuro Suite, it is possible to switch to SDK mode and access shell commands. 

Shell is available for other applications as well, because USB provides **VIRTUAL COM PORT**. RFCSuite communicates with the cube using more complicated multiplexed packets. Before accessing the shell from other applications it is recommended to cycle USB to reset communication on character basis. Note that in this case, characters are not automatically sent back to the terminal. Use command `echoon` if needed.

