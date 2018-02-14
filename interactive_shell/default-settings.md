## Default shell settings

Anytime USB is plugged into an active port, the cube gets reset to it's default state.  
Unless it is connected to RFC Suite, the charging display is launched.  
If you open a VIRTUAL COM PORT device provided by RFC, you can type commands and receive answers.  
After each reset the shell restarts with these settings:

| echoing characters on line | **OFF** | toggle it with "**echoon**", "**echoff**" |
| :--- | :--- | :--- |
| displaying prompt "**$&gt;**" | **ON** | toggle with "**prompton**", "**promptoff**" |
| multiplexed packet mode | **DISABLED** | can be enabled for experiments \(1\) |
| character speed | **ANY** | com port is virtual |
| HW control flow \(RTS/CTS\) | **DISABLED** | other modes not supported |

\(1\) In multiplexed packet line mode RFC has internally several lines like SHELL LINE, BOOT LINE, NAND BOOT LINE, SCRIPT BOOT LINE and FAST/SLOW RAW MOTION DATA LINE. Those lines are multiplexed in separated packets with information like size and check sum. We can provide details upon request.

