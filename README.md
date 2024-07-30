# ESP-Assistant
An ESP32 S3 voice assistant for Home Assistant. Light weight and should compile on low end systems.

The main goal of this project was to create a voice assistant (VA) for HA that is not depending on external files*. A second requirement was that for compiling you don't need much resources. This yaml compile many times faster then the ESP32-S3_box bersion. This version of the voice assistant is also capable to set timers.

_* There is one small dependency in the code if you want a sound when a timer is finished. This dependecy is only there when compiling. A future release may solve this. For now this isn't a big show stopper_

**Requirements**
- Home Assistant
- ESPHome installed

Go to your config/esphome folder
Create a folder and name it sounds
Place the sounds file(s) there

Have a look at the yaml file and change the following substitution for the wake word you want.
At the moment okay_nabu, hey_jarvis and alexa are the available options

  micro_wake_word_model: okay_nabu 

And don't forget to create your secret SSID een password for the wifi section

  ssid: !secret wifi_ssid
  password: !secret wifi_password
  
