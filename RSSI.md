# Configuring RSSI

There is two different kind of RSSI MinimOSD-Extra can handle.

###1./ Analoge RSSI
First you need to enable this function in APM. Go to MP than look for it in advanced parameters.

I have changed it to 6 as I use analog port 6. If you use a different port, replace 6 with your analog port number.

Open Config. Tool than choose MAVLINK RSSI for RSSI chanel.

![](http://gabek.ddns.net/MinimOSD-Extra_wiki_pictures/12.png)

Now you have to teach OSD to "read your receiver".

Open Config. Tool check the "RSSI Enable Raw" check-box.

![](http://gabek.ddns.net/MinimOSD-Extra_wiki_pictures/13.png)

By "RSSI Enable Raw" option checked when you power up your OSD with APM, you will see the raw values.
After APM have booted up and you have your TX working (antenna pulled out), than it will show the raw value that you set in "RSSI Max Value" box. 

![](http://gabek.ddns.net/MinimOSD-Extra_wiki_pictures/14.png)

Than turn your tx off, so it will show the raw value that you set in "RSSI Min Value" box.

![](http://gabek.ddns.net/MinimOSD-Extra_wiki_pictures/15.png)

Than plug your OSD to FTDI again, and uncheck "RSSI Raw Value" check-box, than save it to OSD. After this OSD will show RSSI normally.

### 2./ PWM RSSI

You can use Channel 8 on APM to read PWM rssi.

Make sure you have calibrated Channel 8 on APM the same way you do for all other channels.

Now choose Channel 8 for RSSI Channel in Config. Tool.

![](http://gabek.ddns.net/MinimOSD-Extra_wiki_pictures/17.png)

Than configurei it the same way as Analoge RSSI:

You have to teach OSD to "read your receiver".

Open Config. Tool check the "RSSI Enable Raw" check-box.

![](http://gabek.ddns.net/MinimOSD-Extra_wiki_pictures/18.png)

By "RSSI Enable Raw" option checked when you power up your OSD with APM, you will see the raw values.
After APM have booted up and you have your TX working (antenna pulled out), than it will show the raw value that you set in "RSSI Max Value" box. 

![](http://gabek.ddns.net/MinimOSD-Extra_wiki_pictures/19.png)

Than turn your tx off, so it will show the raw value that you set in "RSSI Min Value" box.

![](http://gabek.ddns.net/MinimOSD-Extra_wiki_pictures/20.png)

Than plug your OSD to FTDI again, and uncheck "RSSI Raw Value" check-box, than save it to OSD. After this OSD will show RSSI normally.

![](http://gabek.ddns.net/MinimOSD-Extra_wiki_pictures/21.png)