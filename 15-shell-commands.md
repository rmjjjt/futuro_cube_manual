# 15 Shell commands

When Rubik’s Futuro Cube is connected to Rubik’s Futuro Suite, it is possible to switch to SDK mode and access shell commands.

Shell is available for other applications as well, because USB provides **VIRTUAL COM PORT**. RFCSuite communicates with the cube using more complicated multiplexed packets. Before accessing the shell from other applications it is recommended to cycle USB to reset communication on character basis. Note that in this case, characters are not automatically sent back to the terminal. Use command `echoon` if needed.



## 15.1 Default shell settings

Anytime USB is plugged into active port, cube gets reseted into its default state. Unless connected to RFC Suite, the charging display is launched. If you open VIRTUAL COM PORT device provided by RFC, you type commands and receive answers. After each reset the shell restarts with these settings:

| echoing characters on line | **OFF** | toggle it with "**echoon"**, "**echoff"** |
| :--- | :--- | :--- |
| displaying prompt "**$&gt;**" | **ON** | toggle with "**prompton**", "**promptoff**" |
| multiplexed packet lines | **DISABLED** | lines can enabled for experiments\(1\) |
| character speed | **ANY** | com port is virtual |
| HW control flow \(RTS/CTS\) | **DISABLED** | other modes not supported |

 \(1\) RFC has internally SHELL, BOOT LINE, NAND BOOT LINE, SCRIPT BOOT LINE and FAST/SLOW RAW MOTION DATA LINE. Those line are multiplexed in longer packets with check sums. We provide details by reuqest.   

example:



