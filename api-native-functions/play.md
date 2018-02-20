# Play

Plays a sound resource from the file system

Syntax: `Play(song)`

* `song` name of the the sound resource from the file system 

Notes: This function starts to play the given file name immediately on the first free audio channel. If no channel is free, it will override the channel that has the oldest track, to play

Example: `Play("myvoice")`

See also: [SetAudioForce](/api-native-functions/setaudioforce.md)

