# InKli first setup

Hi! So you want to connect your InKli to your network, to get more out of it, great! :D

Connecting this to your netowrk only really gains you any features if you also plan to connect it to a homeassistant instance,
or an MQTT server.  
If you don't plan to do so, feel free to enjoy it standalone.  
The device should exit the config screen after 1 minute of power
on time.

## Connect to wifi
You have three options to connect your InKli to your wifi:

1. **ImprovBLE** Set up the wifi from a computer over Bluetooth. Supports Chrome or Edge browsers
1. **ImprovSerial** Set up wifi from a computer over USB. Supports Chrome or Edge browswers
1. **WiFi Access point** Set up through the devices backup wifi hotspot. Supports anything with wifi

## 1&2: Improv BLE and Improv Serial 
To connect the device using either improv solutions, visit: https://www.improv-wifi.com/ with a supported browser.
If using Improv Serial, make sure to connect the device to your computer with a USB cable.

## 3: Through the device backup access point
This method is done easiest through a phone, but can be done on anything with wifi.

Go to your wifi settings, and connect to the InKli Config hotspot. It'll have a 6 character address after it's name too.
To get the password for the network, push the front button to go to the AP info screen.

Once connected, you should be prompted to "log in" to the network. If you're not prompted, got to your browser and navigate to http://192.168.4.1

On this page, you can then select your wifi, and sign in to it.

That's it! :) Your InKli should now be on your network.

## Homeassistant
If you're running a homeassistant setup on the network with your InKli, you should now be able to find your InKli there.

Further HA instructions to follow