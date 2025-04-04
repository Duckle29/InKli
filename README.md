# InKli

From the Danish "Indeklima" or "indoor climate", is an small sensor box, measuring CO2, temperature and relative humidity.

It displays this on an E-paper display, to allow you to keep an eye on the air in the room you're in.  
Additionally, as it is made with ESPHome, it can also easily connect to a Homeassistant instance, for further home automation and logging.

![Image](https://github.com/user-attachments/assets/8a406870-4cd5-410b-8cb9-5f982c64b4e7)
![Image](https://github.com/user-attachments/assets/2fabcd8c-5f1c-4234-9853-e2954723ad6b)


## History
Quite some time ago I built an air quality monitor, and played around with it. (https://blog.mikkel.cc/posts/airq/) It had PM10 sensors, CO2 sensors and BME680 for TVOC.

I've since had this running, and while it was fine, it was bulky, and I only ever really paid attention to the temperature, humidity and CO2 sensors.
The display I used on that box also had issues. Mainly with the backlight being a significant heat source, and an annoyance at night.

So now this is the replacement.
It has:
- ESP32
- 2.13" Waveshare E-paper display  (https://www.waveshare.com/2.13inch-e-paper.htm)
- IR remote demodulator
- 2 side-firing high-current IR LEDs 
- QWIIC port for future expansion / experimentation
- Single push button
- Touch-pad under screen (tested, works so~so, not great)
It also has a (hopefully) quite efficient 3V3 buck regulator to reduce self heating. (pretty good, seems around 2-3C self heating enclosed, mostly from the ESP itself )

At this point, I have the displays and the sensors. I'm getting most things working first, so I don't learn I've used a strapping pin when I have PCBs in hand and they don't cooperate.
I'm pretty happy with the simple display layout, and will see tomorrow how the graph turns out (set to 8h)

The IR blasters are there because one of these sensors will pull double duty, and act as an IR remote for a heat pump. 
On the rest of the PCBs these probably won't be populated.