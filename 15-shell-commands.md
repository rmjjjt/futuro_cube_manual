# 15 Shell commands

When Rubik’s Futuro Cube is connected to Rubik’s Futuro Suite, it is possible to switch to SDK mode and access shell commands.

Shell is available for other applications as well, because USB provides **VIRTUAL COM PORT**. RFCSuite communicates with the cube using more complicated multiplexed packets. Before accessing the shell from other applications it is recommended to cycle USB to reset communication on character basis. Note that in this case, characters are not automatically sent back to the terminal. Use command `echoon` if needed.

## Default shell settings

Anytime USB is plugged into an active port, the cube gets reset to it's default state. 
Unless it is connected to RFC Suite, the charging display is launched.
If you open a VIRTUAL COM PORT device provided by RFC, you can type commands and receive answers. 
After each reset the shell restarts with these settings:

| echoing characters on line | **OFF** | toggle it with "**echoon**", "**echoff**" |
| :--- | :--- | :--- |
| displaying prompt "**$&gt;**" | **ON** | toggle with "**prompton**", "**promptoff**" |
| multiplexed packet mode | **DISABLED** | can be enabled for experiments (1) |
| character speed | **ANY** | com port is virtual |
| HW control flow \(RTS/CTS\) | **DISABLED** | other modes not supported |

(1) In multiplexed packet line mode RFC has internally several lines like SHELL LINE, BOOT LINE, NAND BOOT LINE, SCRIPT BOOT LINE and FAST/SLOW RAW MOTION DATA LINE. Those lines are multiplexed in separated packets with information like size and check sum. We can provide details upon request.

## Shell in RFC Suite

SDK view in RFC Suite offers direct access to the cube shell. Everything is set and ready to go as soon as you switch to this mode.
You can test all available shell commands very easily there. 
**It is important to mention, that RFC Suite turns ON multiplexed packet mode and does not turn it OFF! 
Therefore this must be kept in mind if other proprietary apps wants to access the shell right after the cube has been connected to RFC Suite.**

![](/assets/ViewSDKmode.jpg)

![](/assets/shell_example.jpg)

## Setting shell to default from any app

If you want create a smart app that will communicate with RFC any time, there is a sequence that resets the shell to its default state under any condition (no need to cycle USB). 
The code is in python, but can be ported to any language you use.

```
##########################################
# somewhere in code open sline serial port
##########################################
sline = serial.Serial()
##########################################
def init_basic_shell(kill_clean = 1):
  sline.timeout = 0

  if (kill_clean):
    #"stdshell" in multiplex mode, see below  
    cmd = "SQ\x00\0x0a\x00stdshell\x0d\x70\x71\x00\x73"
  else:
    #"stdshellnk" in mulitplex mode, see below
    cmd = "\x53\x51\x00\x0c\x00\stdshellnk\x0d\x49\x71\x00\x73"

  sline.write(cmd)
  # we have to send once "\r" for case the multiplex was off
  # and we need to discard nonsense commands to obtain the prompt
  sline.write("\r")
  time.sleep(0.2)
  sline.flushInput()

  ##############################################################
  # at this moment, the cube should be communicating in a simple
  # shell with prompt ON and echo OFF
  ##############################################################
  # stdshell kills all ongoing apps
  # if you do not want to interfere
  # and let running apps continue,
  # use "stdshellnk" instead (kill_clean=0)
  ##############################################################
  # if you don't kill a running script on cube, the script can 
  # interfere with the shell with its output - 
  # use only if you know what you are doing :-)
################################################################
```



