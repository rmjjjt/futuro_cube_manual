# Sound resources

There is an easy way to modify or upload your own resources into the Rubik's Futuro Cube and work with them.
Standard available sound resources are available [here](http://www.futurocube.com/support/) under **Language packs EN+CZ+GE **section.
If you look at the offered zipped files, you will find out that those are regular Microsoft WAV files in the following supported formats:

| Highest quality | mono PCM WAV 22.050 kHz 16bit | max playback time TBD |
| :--- | :--- | :--- |
| Middle quality | mono PCM WAV 22.050 kHz 8bit | TBD |
| Middle quality | mono PCM WAV 11.025 kHz 16bit | TBD |
| Lowest quality | mono PCM WAV 11.025 kHz 8bit | TBD |

If you want, you can alternate original resource files and make your own language/crazy distribution.
Only, try to follow the following rules that applies to all resources, especially for games and apps:

#### Remove DC component from the sample

Playback system in the cubes does not like DC shifted playback.
Internal algorithm counts DC energy of the sound and in case there is a chance to damage the speaker, playback is stopped.
Lots of free audio editing software has built-in filter for DC part removal.

#### Normalize volume output

Unless you want something specifically loud or silent, always try to normalize the volume to 70-90 % of the maximum output.
That way most of the samples will create a comparable feeling. Again, this is a pretty standard function of an audio editor.

#### Recommended SW

* [www.goldwave.com](/www.goldwave.com)

#### Further reading

* [Uploading resources](/sound-resources/uploading-resources.md)
* [Erasing resources](/sound-resources/erasing-resources.md)
* [Playback priorities](/sound-resources/playback-priorities.md)
* [Naming conventions](/sound-resources/naming-conventions.md)

#### Advanced

These steps are not needed in 95 percent of cases. You probably don't need to pay attention at all.
But, in case you are interested in playback of most accurate samples on the Rubik's Futuro Cube, it might be of interest to you.

* [Sample rate compensation](/sound-resources/sample-rate-compensation.md)
* [Frequency response compensation](/sound-resources/frequency-response-compensation.md)