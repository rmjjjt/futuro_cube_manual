## Important Cube SHELL commands:

|||
|:------|:------|
|bleraw N<br/>\[acc_scale=8]<br/>\[acc_bw=408]<br/>\[gyro_scale=2000]|This command starts reporting raw data over BLE.<br/>N - report every Nth sample. 2,3,4,5,6,.... 2 equals to ODR 476 Hz (native ODR is 952)<br/>N=0 - reports disabled and mems sensor is standardly configured <br/>N>102 - special test mode, ODR will be setup as the N=N-100, but real data are replaced by 20 bytes array of the same byte. And sample this  byte is incremented by 1 (overflow in 256 to zero). This mode is intended for test purposes.<br/>acc_scale - 2,4,8,16 - +-2G, +-4G, +-8G, +-16G. Tapping algorithm is optimized to +-8G, any other value can avoid tapping detection.<br/>acc_bw - 408,211,105,50 Hz<br/>gyro_scale - 245,500,2000 dps<br/>Datasheet to LSM9DS1:<br/>http://www.st.com/content/st_com/en/products/mems-and-sensors/inemo-inertial-modules/lsm9ds1.html<br/>Examples:<br/>bleraw 2<br/>bleraw 2 16<br/>bleraw 2 8 211 2000 (probably the most correct settings, BW<=ODR/2)<br/>At the moment after the command some unwanted tap can be detected. This is due to short raw data gap. TBD for workaround.|
|blei|Prints information about current Nordic BLE FW version and some statistics, can be useful for some debug purposes.|
|cleartimer|Resets precise us timer to zero.|
|pstart script_name|Starts PAWN script with “script_name”. Script must have its name defined in code. See the docs or examples.|
|pdir|List all available scripts in cube with its names and positions.|
|ver|Version of the current FW in the cube|
|stdshell|Setup the shell into standard mode (echo off, prompt on and so on). This command also kills all running applications with stopping all playback and clearing sound queues plus clearing LED display. It is good practise to send this command into the cube as first after connection. It is also recommended to not wait for std answer, since the state before this command is unknown and output can be corrupted. After this command everything should work as intended. |
|stdshellnk|This is a no kill version of the previous command. I.e. it only setups the shell into correct state, but does not interfere with the running app. |
|kill|Kills all running applications with stopping all playback and clearing sound queues plus clearing LED display.|

Other commands can be found in the [Shell Commands section](shell-commands.md)