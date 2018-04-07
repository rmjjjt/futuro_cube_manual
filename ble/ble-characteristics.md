## BLE characteristic offered by Rubik’s Futuro Cube

(interested for phone app developers)
Service: 6e400001-b5a3-f393-e0a9-e50e24dcca9e

| Characteristic        | UUID           | Status in Cube FW  |
|:------------ |:--------------|:------|
| Shell TX |6e400003-b5a3-f393-e0a9-e50e24dcca9e| FW 8.1 OK |
| Shell RX |6e400002-b5a3-f393-e0a9-e50e24dcca9e| FW 8.1 OK |
| Script TX |6e400005-b5a3-f393-e0a9-e50e24dcca9e| FW 8.2 OK |
| Script RX |6e400004-b5a3-f393-e0a9-e50e24dcca9e| FW 8.2 OK |
| Motion Info TX |6e400007-b5a3-f393-e0a9-e50e24dcca9e| ✖ |
| Motion Info RX |6e400006-b5a3-f393-e0a9-e50e24dcca9e| ✖ |
| Mems Raw Data TX |6e400008-b5a3-f393-e0a9-e50e24dcca9e| FW 8.1 OK |

MEMS_RAW_FORMAT (all data BIG ENDIAN):

| 4 bytes | UUID           |
|:------------ |:--------------|
| 2 bytes |acceleration  x|
| 2 bytes |acceleration  y|
| 2 bytes |acceleration  z|
| 2 bytes |angular rate  x|
| 2 bytes |angular rate  y|
| 2 bytes |angular rate  z|
| 4 bytes |TBD - magnetic field|

Value interpretation depends on current IMU settings. See “bleraw” shell command.