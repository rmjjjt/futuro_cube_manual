# Playback priorities

Playback engine supports in total 4 audio channels, that are mixed in real time. Channels are sequenced in order 1,2,3,4 and if all 4 channels are used, next request is given back to 1 even the playback there is still in progress and etc.. There are many APIs that  work with this and of course there is possible to check if the plays or not. 

But important is that all shell commands or all native APIs are taking input only the name of the file without name of the folder. That means there will be no problem if all names of the file are unique. But this is hardly the case and it wouldn't be really managable. 



