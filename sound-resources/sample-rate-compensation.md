# Sample rate compensation

The playback engine in Rubik's Futuro Cube does not exactly have output rate equal to 22.050kHz or 11.025kHz.
In fact it is 22kHz and 11kHz.
If you want to have, for example, precisely played some tones or chords, or even music, you have to resample the sound into these frequencies.

Using GoldWave, this is very easy to achieve.
Some software allows you to use batch processing, so all resources together with other filtering can be processed at final stage.