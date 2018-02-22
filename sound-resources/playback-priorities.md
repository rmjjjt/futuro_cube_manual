# Playback priorities

The playback engine supports a total of 4 audio channels, which are mixed in real time.
Channels are sequenced in order and the engine always looks for the first available quiet channel.
If it does not find any, it uses one that has been used for the longest time.
I.e. it stops it's playback and starts a new one.
There are many APIs that work with this and of course it is possible to check if the channel will play or not.
And many more tricks like individual channel volume and etc.

But most important is that all shell commands and all native APIs are taking only the **name of the file** **without the name of the folder** as input.
And this can possibly raise a problem of files with the same names.

Luckily, there is a priority system of mounted folders and rules around the requested file for playback is being searched:

* highest priority has folder with the same name as the script, that is currently running (if any)
* second highest priority has folder, with its name starting with **'@'**, this is called main resources folder
* rest is in random order or in some mounted order - it is assumed this has no meaning