# Sample rate compensation

Playback engine in Rubik's Futuro Cube does not exactly have output rate equal to 22.050 kHz or 11.025 kHz. In fact it is 22 kHz and 11 kHz. If you want to have for example precisely played some tones or chords or even music, you have to resample the sound into this frequencies.

Using GoldWave this is very easy to achieved. Some SWs allows you to use batch processing, so all resources together with other filtering can be processed at final stage.



