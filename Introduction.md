Introduction
MinimOSD is a super-tiny board designed by 3DRobotics. It’s all you need to get OSD telemetry data from ArduPilot Mega. Just connect your FPV camera and a video link and you’re ready to fly with instruments on screen.

![](http://gabek.ddns.net/MinimOSD-Extra_wiki_pictures/MinimOSD.jpg)

It’s intended to be a dedicated APM telemetry video output. So, it reads MAVLink messages from its RX and request rates from APM if you connect its TX to ArduPilot “telem” port.

Important note: You cannot connect the OSD when your APM 2 is also connected via USB (they share the same port). Make sure you disconnect your USB cable from the APM 2 board before attempting to use the OSD.