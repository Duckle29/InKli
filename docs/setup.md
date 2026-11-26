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

Go to your wifi settings, and connect to the "InKli Config" hotspot.
To get the password for the network, push the front button until you reach the config screen (it shows the SSID and password).
The screens cycle: welcome, info, config, and back to welcome. So from the welcome screen it's two pushes.

The info screen shows the device's ID, IP address and DNS servers.

Once connected, you should be prompted to "log in" to the network. If you're not prompted, got to your browser and navigate to http://192.168.4.1

On this page, you can then select your wifi, and sign in to it.

That's it! :) Your InKli should now be on your network.

## Changing wifi
The hotspot only runs while the InKli isn't connected to a network. If it's already on wifi, the config screen shows
"Connected to <your network>" instead of the hotspot details.

To set it up on a different network, go to the config screen (hold the front button for 2 seconds), and hold the button for 4 seconds. The bar shows "forget wifi" at that point. Let go, and the InKli forgets
the network and restarts. After a few seconds the "InKli Config" hotspot is back, and you can follow the steps above.

## Clock
Push the button to cycle through the CO2, temperature, humidity and clock screens.

The InKli gets the time from the internet (NTP) when it's on wifi. You can also set it by hand:

1. On the clock screen, hold the button for 4 seconds, until the bar reaches "set time", and let go.
2. Push the button to count up the highlighted digit.
3. Hold the button for 1 second to move to the next digit. Doing that on the last digit saves the time.

If you leave it for 2 minutes without pressing the button, it goes back without changing the time.
A time set by hand is forgotten when the InKli restarts, and is replaced by the internet time whenever that's available.

The timezone defaults to Central Europe. To change it, or to turn off automatic daylight saving time, use the
"Timezone" and "Automatic daylight saving time" entities in Home Assistant.

## Homeassistant
If you're running a homeassistant setup on the network with your InKli, you should now be able to find your InKli there.

The temperature offset can be calibrated from Home Assistant. There are two, "Temperature offset (wifi connected)" and
"Temperature offset (wifi not connected)", as the radio warms the case a bit when it's on. They're disabled by default,
so enable the entities in Home Assistant if you want to adjust them.

Further HA instructions to follow