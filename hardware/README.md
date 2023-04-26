# Hardware
The only requirement for PiPower is a relay set up to short two pins (N/O and common with no inputs attached).

I have built a reference board and provided schematics to copy it. You will need:
* breakaway pin headers
* a 3.3v or 5v relay
* an NPN transistor
* ~ 1k ohm resistor
* copper perfboard
* optionally an led for activity, I like green since they often don't need a resistor to use at 3.3v

You can buy relay kits that plug directly into a Pi, they should work fine, just change the GPIO pin in pipower-relay accordingly.
