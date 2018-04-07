## USB Dongle

Easy way to access BLE on Rubik’s Futuro Cube

USB dongle form creates a bridge between native BLE protocol and a computer user in a very easy way.
 Instead of learning and implementing standard BLE access, the dongle does it (I did it) for us and the dongle communicates with a much simpler interface.
 What more, all communication handling is prepared in the provided Python SDK library and examples. At the end of this document is a detailed description of the HW layer. But, this is important only for 3rd side integrators.

Next follows a little deeper info about communication lines used in the dongle and SDK..
To get a little motivated, you can just jump into the Python SDK and try example_hello_world.py, then come back and read further.

Encapsulated communication lines:

|Command|Description|
|:------------ |:--------------|
|CONTROL|This lines communicates with the dongle only and provides the main interface for user commands and asynchronous messages.|
|SHELL|Shell connection to the cube - the same as if you would be connected via USB and type commands in SDK mode. Shell output/input is split into 20 bytes chunks and assembled/disassembled on both ends. This line acts as stream. End of command is always recognized with “\r”|
|SCRIPT|Communication with running script. Allows to exchange 20 bytes packets of any user data. |
|MOTION_INFO|Packed data of sensor outputs and motion/tapping detection as it is seen by scripts or games. Data is slightly filtered with simple averaging filter. **ODR around 125 Hz. AVAILABLE SOON**|
|MEMS_RAW|Raw data from mems sensor without any additional filtering. ODR and BW is selected by user. **Maximum ODR is 476 Hz** Read shell commands below. |