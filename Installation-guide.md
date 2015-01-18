It has the Max7456 chip powered by two stages to avoid noises from servos attached to ArduPilot Mega board.
It provides an extra clean power line to feed the FPV camera and video link.

The approach is to use two external power sources: 12V from a Lipo Battery and 5V from APM:

![](http://dev.ardupilot.com/wp-content/uploads/sites/6/2013/06/DiagramaMinimOSD.jpg)

**Raw 12V from Lipo Battery:**
Feeds directly FPV camera and video transmitter.
It also feeds Max7456’s analog line (AVDD and AGND) by a 5V voltage regulator (avoiding noises from servos attached to APM).

**5V from APM telem port:**
Feeds the ATmega 328P and Max7456’s digital line (DVDD and DGND);



**Note:** Optionally, you can use two solder jumps to “tie” digital and analog lines.

![](http://dev.ardupilot.com/wp-content/uploads/sites/6/2013/06/PowerTieMinimOSD.jpg)

MinimOSD has no extra pins exposed, because the concept is “capturing all the needed data from MAVLink”.
E.g.: to show RSSI from RC receiver, that info needs to be on msgs #35 and #36 (RC_CHANNELS “RAW” and “SCALED”).
So, the analog reading of RSSI output from receiver needs to be done on APM analog ports and treated inside the APM code.