# 5 Programming

The script interpreter runs as a separate task in the cube as well as any other games.

Good behavior of the script is to perform so called co-operative multitasking. That means, after you do what you needed to, you should use the `Sleep()` function. If `Sleep()` is not used, nothing bad happen - the system will cut out the script for a while and give some time for system tasks.

If the script is not complicated, no one will ever notice that `Sleep()` isn't called.

If it is important to delay the program or wait for something, like waiting until music playback is over, you should always use delay functions with the built in `Sleep()` instruction. These are, for example: `Sleep()`, `WaitPlayOver()`, `WaitMelodyOver()`.

The following picture shows simplified scheduling and recommended basic programming workflow.![](/assets/Screen Shot 2018-02-04 at 13.37.51.png)

Simplified Scheduling

