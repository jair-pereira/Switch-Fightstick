# Switch-PCcontroller

## About
This repository allows you to use your computer to send multiple button presses simultaneously to your Switch.
For example, start running then jump in Zelda (Left stick + B then X)

I'm building on top of two works:
1. [progmem/Switch-Fightstick](https://github.com/progmem/Switch-Fightstick): reverse-engineered the Pokken Pro Pad, allowing us to use microcontrollers to send commands to the Switch.
2. [ebith/Switch-Fightstick](https://github.com/ebith/Switch-Fightstick): wrote an interface to send commands from the computer to the Switch using serial communication.

I modified [ebith/Switch-Fightstick](https://github.com/ebith/Switch-Fightstick) to allow multiple button presses simultaneously. If you do not need simultaneous button presses in your macro, I recommend checking [ebith/Switch-Fightstick](https://github.com/ebith/Switch-Fightstick) instead.

There are other interesting repositories for macros such as [Zelda Snowball-thrower](https://github.com/bertrandom/snowball-thrower) and [Splatoon 2 post printer](https://github.com/shinyquagsire23/Switch-Fightstick).

## Requirement
### Hardware
- 1x Teensy (at90usb1286) or Arduino (atmega32u4)
- 1x USB to Serial Adapter
- 1x USB Micro-B Cable
- 2x Male-Female Breadboard Wires

### Software
- Python and the pyserial library
- AVR-GCC (for teensy, follow their instructions [here](https://www.pjrc.com/teensy/gcc.html))

## Setting up
1. Compile this repository
2. Flash the Joystick.hex to the Teensy
3. Run one of the scripts in the example folder

You can also download Joystick.hex [here](https://github.com/ebith/Switch-Fightstick/releases/latest/download/Joystick.hex).

## Writing a macro
todo
<!-- First, check joycon.py and the scripts in the example folder.-->

<!-- Possible commands: -->
<!-- - Button: Y, B, A, X, L, R, ZL, ZR, SELECT, START, LCLICK, RCLICK, HOME, CAPTURE, RELEASE. -->
<!-- - D-Pad: TOP, TOP_RIGHT, RIGHT, BOTTOM_RIGHT, BOTTOM, BOTTOM_LEFT, LEFT, TOP_LEFT, CENTER. -->
<!-- - Sticks: (right) RX value, RY value, (left) LX value, LY value* -->
<!-- *value=\[0,255], where 128 is center -->

<!-- Methods: -->
<!-- Button -->
<!-- - press_button(key, duration, delay) -->
<!-- -- press_button(key="A", duration=1, delay=2) -->
<!-- --- press A for 1 second, release A, then waits 2 seconds -->
<!-- - hold_button(key) -->
<!-- -- holds a key undefinetly -->
<!-- - release_button(key) -->
<!-- -- releases a key previously -->

<!-- Stick -->
<!-- - press_button(key, duration, delay) -->
<!-- -- press_button(key="A", duration=1, delay=2) -->
<!-- --- press A for 1 second, release A, then waits 2 seconds -->
<!-- - hold_button(key) -->
<!-- -- holds a key undefinetly -->
<!-- - release_button(key) -->
<!-- -- releases a key previously -->


