# PiPower
Set up a Pi to remotely turn on WoL incapable devices.

# Hardware
This is meant to be used with a Raspberry Pi with the GPIO and a relay. See this hardware section for more info on relays.

# Installation
The suggested route would be to use the install-pipower script as root: 

Warning: Only run scripts you trust, especially when they are sent into bash like this

`bash <(curl -s https://github.com/brendenhoffman/PiPower/master/install-pipower )`

If you would like to make configuration changes, it can be done easily by making them in the PiPower git directory and running `# install-pipower c`

# Usage
These scripts are designed to be flexible. They can be used with any number of other programs. They are stored in /bin
* pipower.service: This is a SystemD service file to start the port listening script.
* pipower-listen: This is the port listening script, it will typically not be used unless you are not using the SystemD service.
* pipower-relay: This script triggers the relay. It should not be used directly as there is no protection for whether it is triggering the power button on a running maching or not.
* pipower-check: This is a script that pings given IP addresses to check whether the attached computers are running or not before executing pipower-relay.
* pipower-send: This is a script to distribute WOL packets to any computer in the MAC list.
* pipower-all: This one simply executes both pipower-check and pipower-send at the same time.

# Configuration
The config files are stored in /etc/pipower.
* iplist: This file is a simple list used by pipower-check to ping attached computers. IPs are separated by a newline.
* maclist: Pipower-send will use this to distribute WOL packets. MAC addresses are separated by a newline.

# Usage with NUT
Nothing here yet
