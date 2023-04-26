# Hardware
The only requirement for PiPower is a relay set up to short two pins (N/O and common with no inputs attached).

I have built a reference board and provided schematics to copy it. You will need:
* breakaway pin headers
* a 3.3v or 5v relay
* an NPN transistor
* ~ 1k ohm resistor
* copper perfboard
* optionally an led for activity, I like green since they often don't need a resistor to use at 3.3v

This is the basic circuit diagram I made:

![circuit](https://github.com/brendenhoffman/PiPower/blob/2a96c0132774238de9a3e4d2073b479dabd0d93a/images/circuit.png)

Here is what my, uh, ~~production~~ prototype board looks like:

<img src="https://github.com/brendenhoffman/PiPower/blob/2a96c0132774238de9a3e4d2073b479dabd0d93a/images/relay.jpg" width="600"/>

Here is with the circuits traced out:

<img src="https://github.com/brendenhoffman/PiPower/blob/2a96c0132774238de9a3e4d2073b479dabd0d93a/images/diagram.png" width="600"/>

# Other options
You can buy relay kits that plug directly into a Pi, they should work fine, just change the GPIO pin in pipower-relay accordingly.
