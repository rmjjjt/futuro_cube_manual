# SetAudioForce 

Enables forcing audio to channel 0 

Syntax: `SetAudioForce(value)` 

* `value` 1 - enables audio force, 0 - disables audio force 

Notes: This function can enable audio force on channel zero. After enabling, channel zero is not used for overriding when a new [play](/api-native-functions/play.md) command is invoked. It is used to force play audio data in a situation where more resources are mixed and one sound must be completely played without interruption. To use channel zero with forcing function, `Play` must have a song name with the beginning character `@`

Example: 

* `SetAudioForce(1)` 
* `Play("@forcesong")` 

See also: [Play](/api-native-functions/play.md)

