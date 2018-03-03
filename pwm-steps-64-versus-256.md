## PWM steps - 64 versus 256

LEDs on the cube surface are controlled by PWM modulation.
In a regular run, there is (for each LED), 64 PWM steps available.
Therefore, each color component value before printing onto the cube surface (printing Virtual Canvas is not doing that yet) is divided by 4 and subtracted by 1.
That has the effect that, for example, `SetRGB(7, 7, 7)` still gives black.
Full 256 steps can be switched on if needed. API will be provided later.

