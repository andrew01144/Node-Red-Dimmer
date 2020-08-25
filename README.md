# Node-Red-Dimmer
Dimmer function for Node-Red Zigbee Home Automation

![flow1](https://user-images.githubusercontent.com/18399286/91164667-578d9b80-e6c7-11ea-83b6-487afec48a40.png)

# Description
This Node-Red function connects an IKEA control to a dimmable light bulb to provide the behavior of a dimmer.
Hold down a button on the remote to increase or decrease the brightness of a bulb.

# What it does
To increase the brightness, press and hold the button on the remote. The remote issues a brightness_up_hold message.
This causes the Dimmer function to issue set-brightness messages every 250 ms with increasing brightness values.
When you release the button, the remote issues a brightness_up_release message, and the Dimmer function stops.

# Prerequisites
- [Node-Red](https://nodered.org/)
- [zigbee2mqtt](https://www.zigbee2mqtt.io/)
- IKEA TRADFRI Zigbee [E1810 Remote](https://www.zigbee2mqtt.io/devices/E1524_E1810.html) or [E1743 On/Off Switch](https://www.zigbee2mqtt.io/devices/E1743.html)
- Any dimmable Zigbee bulb

For excellent instructions on how to setup all these prerequisites, [start here](https://notenoughtech.com/home-automation/flashing-cc2531-without-cc-debugger/).

# Using the code
The file Dimmer_Flow.json contains the Dimmer function within a small demo flow.
In Node-Red, Import the Dimmer_Flow.json file. Paste it to a new or existing flow.
Modify the mqtt-in and mqtt-out nodes to match the names of your mqtt server, IKEA remote, and Light bulb.
Copy and paste this flow for as many remotes and bulbs as you need.

