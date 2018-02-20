# Playback priorities

Playback engine supports in total 4 audio channels, which are mixed in the real time. Channels are sequenced in order and the engine always looks for first available quiet channel and if it does not find any, it uses one that has been used for the longest time. I.e. it stops its playback and start new one.  There are many APIs that  work with this and of course there is possible to check if the channel plays or not. And many more tricks like individual channel volume and etc.

But important is, that all shell commands and all native APIs are taking as input only the **name of the file** **without the name of the folder**. And this can possibly bring problem of files with same names. 

Luckily, there is priority system of mounted folders, and rules how the requested file for playback is being searched:

* highest priority has folder with the same name as the script, that is currently running. \(if any\)
* second highest priority has folder, with its name starting with **'@'**, this is called main resources folder
* rest is in random order or in some mounted order - it is assumed this has no meaning



