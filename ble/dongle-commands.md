## Dongle commands on CONTROL line

|||
|:-------|:------|
|ver|Info about FW version and check of the Nordic chip revision.|
|init, close, disconnect|Any of those commands ends ongoing connection (if any) and resets the dongle into initial state after reset. It is good practise to send this command at the beginning of any session. |
|state|Returns “CONNECTED” or “DISCONNECTED”|
|scan|Starts scanning of nearby cubes. If there is an ongoing connection, it is immediately aborted. Serial numbers are reported in scan reports.<br/>Example:<br/>...<br/>adv:PSC01ZC05698<br/>adv:PSC01ZC02333<br/>...|
|scanstop|Stops current scan and currently close any ongoing connection. At the moment it does exactly same as “init”. |
|connect *|Tries to connect to any cube which is first recognized. |
|connect serial_number|Tries to connect only to specific cube with given serial number.<br/> eg: `connect PSC01ZC02333`|

Each command returns at the end either “__OK__” or “__ERR: err messages__”. CONTROL line commands are designed in way, where the answer is not necessary to check. “state” command is also not needed, because if there is disconnecting event, user is informed by asynchronous messages. **It is better to monitor them rather than wait for answer.**