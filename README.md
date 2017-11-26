[Home Assistant](https://home-assistant.io/) configuration files (YAMLs)

Hass.io running on [Raspberry Pi 3](http://amzn.to/2e3DOBY)

**Software on the Pi :**
* [Stock Hass.io Image](https://home-assistant.io/hassio/installation/) 
* [Samba Share](https://home-assistant.io/addons/samba/) For Windows network access
* [Bluetooth BCM43xx](https://home-assistant.io/addons/bluetooth_bcm43xx/) Mainly used for Mi Flora plant sensor
* [DuckDNS with Let's Encrypt](https://home-assistant.io/addons/duckdns/)
* [Mosquitto Broker](https://home-assistant.io/addons/mosquitto/) For Smarrthings and Sonoff integration
* The amazing [Floorplan](https://github.com/pkozul/ha-floorplan) project to help visualize my smarthome.

**Devices I have :**
* [Google Wifi system (set of 3)](http://a.co/3BT0xq1) I use 3 for a 1,500, which is serious overkill. One would have probably been enough. I had to upgrade from a Linksys EA2700, because DuckDNS requires a Router that supports NAT Loopback.
* [Amazon Echo DOT](http://amzn.to/2e3vHFQ)
* [Amazon Echo Tap](http://amzn.to/2sz891k)
* [Amazon Dash Wand](https://www.amazon.com/Amazon-Dash-Wand-With-Alexa/dp/B01MQMJFDK/ref=sr_1_1_a_it?ie=UTF8&qid=1498928735&sr=8-1&keywords=dash+wand) - Alexa outside by the pool area.
* [Amazon Fire Tablets Gen 7](http://amzn.to/2tqlMCW)- Used for [Wall Mounted Controllers](http://www.vmwareinfo.com/2017/07/visualizing-smart-home-using-home.html)
* [Samsung SmartThings Smart Home Hub](http://a.co/gB0tLnc) All my Z-wave devices connect through this via MQTT
* [Phillips Hue Hub Gen 2](http://amzn.to/2eoQTJy)
* Mixture of [Hue Colored lights](http://amzn.to/2l2viGK), [White Lights](http://amzn.to/2lEf4Xq)
* [GE Z-Wave Outdoor Module 12720](http://amzn.to/2q17R4S) These control my Outdoor lights. Brought in through Smartthings.
* [GE Z-wave Wireless In-Wall paddle switch 12722](http://a.co/5aDYIpF) Most Interior lights. Brought in through Smartthings.
* [GE Z-wave Wireless In-Wall paddle dimmer 14294](http://a.co/5aDYIpF) Brought in through Smartthings.
* [SkyBell HD](http://amzn.to/2dcexIB)
* [ChromeCast Audios](http://amzn.to/2lE9gNu)
* Emulated Hue pushes all Switch, Group, input_boolean, script and scene information to Alexa for First Class Control!
* [SonOff](http://amzn.to/2l2sx8g)
<!-- 
**Automations:**
* Voice Notifications via the [AMPs](http://amzn.to/2j18dlT) connected to ChromeCast Audios and [Mixer](http://amzn.to/2v9Zp3x).  Accomplished via the [~~Google~~ Amazon Polly TTS](https://home-assistant.io/components/tts/) component.
* Ability to ask Alexa to repeat the last Voice notification - 'Alexa, Turn on Last message'.
* Track garbage days and chore days for the kids. Voice reminders and Alexa intergration/request for info.
* Guest mode to disable certain interior automations. Trigger via Alexa & IFTTT.
* IFTTT and Slack Notifications for Offline Devices, BadLogins, HA Startups, new HA versions and [External IP changes](https://community.home-assistant.io/t/detect-if-ip-changes/6830) for DSN.
* Monitor the reflection rates of [Garadget](http://amzn.to/2jQLpVQ) and notify when they being to drop too low when closed (indicating a shift in the controller)
* Notifications when the garage door is left open at night or when we leave the house.
* (IFTTT) Logging entries in Logbooks for [Rachio Sprinkler system](http://amzn.to/2eoPKBW), and [SkyBell HD](http://amzn.to/2dcexIB).
* Auto Heal ZWave at 2:30am
* Using [Etekcity Outlets](http://amzn.to/2efNoBP) to control accent lighting above kitchen cabinets and room cutouts.
* Turn on Hallway light for no more than 20 minutes when Pantry door is opened.
* Turn on TV Time Lights (dim and color) at Sunset (if home and TV is on)
* Turn on Upstairs light if [Nest Thermostats](http://amzn.to/2eAhB1k) detects people and it's nighttime.
* Turn off lights when [Nest Thermostats](http://amzn.to/2eAhB1k) detects we are away. (Upstairs and Downstairs)
* Turn on some lights and switches when we get home
* Turn on some outdoor Lights at Sunset or if it gets darkish in the house, Turn off 4 hours before sunrise.  Turn off interior lights when we go to sleep.
* Turn on lights during school days for a morning routine for the kids and wife. Has No School overide boolean in GUI.
* Rainy days trigger extra light inside the house.
* Check the UV Rays for the day and let us know if we need sun tan lotion over the TTS system.
* Detects when lights are turned on and adjusts them to correct brightness based on time of day.
* Leverage Alexa, IFTTT and Elekcity outlet to control Printer On/Off via Voice. Turns off automatically after 20 minutes.
* Turn on [AMPs](http://amzn.to/2j18dlT) when Chromecast reports 'Playing'.  Turn them off when we are done streaming music.
* (IFTTT) Blink ALL lights at 9:30 to remind me to take medicine. (also Alexa Alert)
* (IFTTT) Blink Office lights 15 minutes before ANY meeting on my calendar (using IFTTT)
* (IFTTT) Stop watering grass via [Rachio Sprinkler system](http://amzn.to/2eoPKBW) if winds are greater than 20 MPH.
* (IFTTT) Add a 1 day rain delay to [Rachio Sprinkler system](http://amzn.to/2eoPKBW) if it is going to rain tomorrow.
* (IFTTT) Blink ALL lights if Winds get to 70MPH - Hurricance warning.
* (IFTTT) Trigger Good Night routine when I step on the [Withings](http://amzn.to/2kr78nW) scale after 10pm.
* Sets up the front lights in the house with preset colors depending on the ~~month~~ day!.
* On motion from [SkyBell HD Doorbell](http://amzn.to/2dcexIB) (IFTTT) Turn front lights to Bright White lights for 10 minutes and then back to original colors.  Fake Dog barking when there is motion by the house.
* When someone rings the Doorbell (IFTTT), the backyard and Bathroom lights Flash - Since we might not hear the doorbell. Fake Dog barks as well (which can be snoozed for 30 minutes via Alexa).
* Watch and alert on Home Assistant's Disk usage. Get alerts before Pi runs out of space on the [SD Card](http://amzn.to/2kNttio).
* Digital Cuckoo Clock that goes off each hour and on the half just like a real Cuckoo Clock.  Plays across the whole house on my [ChromeCast Audios](http://amzn.to/2lE9gNu)

**Time Based Automation TimeLine**
```
ALL DAY LONG:
Checks to see if we are away.
Cuckoo Clock goes off each hour and on the half.

SUNRISE minus 1 hour
     Turn off ALL SWITCHES
     Turn off ALL LIGHTS
05:00 AM ** Light Brightness helper 50 Brightness **
06:00 AM ( on school days) : Turn on Dining Room lights, Kitchen Accents and start Kid's bedroom [Hue Go](http://amzn.to/2iB36Ii) wake up lights.
06:51 AM Turn on Dinette lights, Turn off Dining Room Lights and Kitchen Accents
07:51 AM Turn on Kitchen Lights
08:00 AM ** Light Brightness helper FULL 255 Brightness **
08:31 AM (on school days) Turn off ALL interior lights.
09:00 AM Speech Notifications are enabled for the house.

SUNSET:
     Turn on Den Outlet, Living Room Outlet, Dining Room Outlet, Outdoor Bathroom light, TV lights
     Activate Monthly Front Lighting Scene
     Check if Garage Door is open (Every 60 minutes)
     ** Kitchen Light/Accent Helper Activated **

08:00 PM ** Late Night Helper is active **
08:00 PM ** Light Brightness helper 35 Brightness **
08:00 PM TV time Scene triggered if the TV is on.
09:00 PM Turn on [Hue Go](http://amzn.to/2iB36Ii) lights for the kid's rooms and start fading down.
10:00 PM Speech Notifications are disabled for the house. (except under ALERT mode) and AMP is shut.
02:00 AM ** Late Night Help Deactivated **
02:31 AM Heal ZWave Network
02:35 AM Clear out daily TTS cache
```

#Todo List
I've moved this entire section to the [issues section](https://github.com/CCOSTAN/Home-AssistantConfig/issues) on github.
Feel free to join the conversations there.

![Screenshot of Home View](https://i.imgur.com/UlUiKTX.png)
![Screenshot of Garage Door View](https://i.imgur.com/zotvUKp.png)
![Screenshot of Lights](https://i.imgur.com/KKCPaLJ.png)
![Screenshot of More](https://i.imgur.com/rg6lhJz.png)
![Screenshot of Even More](https://i.imgur.com/SlglNh3.png)
![Screenshot of Last one](https://i.imgur.com/sTsYQi4.png)

**All files are now being edited with [Atom](https://atom.io/).**

**All of my configuration files are tested against the most stable version of home-assistant using [Travis](https://travis-ci.org/CCOSTAN/Home-AssistantConfig).**

#Still have questions on my Config?
Message me on twitter : [@CCostan](https://twitter.com/ccostan) -->