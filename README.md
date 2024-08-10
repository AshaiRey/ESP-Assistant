# ESP-Assistant
An ESP32 S3 voice assistant for Home Assistant. Light weight and should compile on low end systems.

The main goal of this project was to create a voice assistant (VA) for HA that is not depending on external files*. A second requirement was that for compiling you don't need much resources. This yaml compile many times faster then the ESP32-S3_box version. This version of the voice assistant is also capable to set multiple timers.

_* There is one small dependency in the code if you want a sound when a timer is finished. This dependecy is only there when compiling. A future release may solve this. For now this isn't a big show stopper_

**Hardware needed**
- CPU: ESP32-S3 N16R8
- Mic: INMP441
- Amp: MAX9835A
- Led: 3 WS2812B leds.
- Speaker: 40mm Headset Driver Hifi Headphone Speaker Unit 32ohm [AliExpress](https://www.aliexpress.com/item/1005001352277084.html)

I've include the schematic that I used and placed it in the media folder. It follows to general approach for this setup but i had to use 2 diffentent pins to get it working reliably.
(Schematic is based on the one found [here](https://smarthomecircle.com/How-to-setup-on-device-wake-word-for-voice-assistant-home-assistant#circuit-diagram-for-esp32-s3-with-inmp441-microphone--max98357a-audio-amplifier)

**Requirements**
- Home Assistant
- ESPHome installed

**Setup**
Go to your config/esphome folder
Create a folder and name it sounds
Place the sounds file(s) there

Have a look at the yaml file and change the following substitution for the wake word you want.
At the moment okay_nabu, hey_jarvis and alexa are the available options

_  micro_wake_word_model: okay_nabu _

And don't forget to create your secret SSID een password for the wifi section

  ssid: !secret wifi_ssid
  
  password: !secret wifi_password

  
I've include the 3D print files for the body and the cover. I used a resin printer for these
![VoicePuck-top](https://github.com/user-attachments/assets/860735a3-23ba-4d62-90ca-2ab0160d5e5d)

![VoicePuck-bottom](https://github.com/user-attachments/assets/b499539f-c70a-4596-942c-3c0e93b9055e)

For comparison this is a Voice puck with with a dark cover which is perforated to let the light shine through.
Left the Google home version, right the ESP Assistand
![VoicePuck-GoogleHome](https://github.com/user-attachments/assets/5bf028dc-2269-41cd-9bdd-1a9a011f9e1a)

You can choose your cover freely. This one has a light wooden vineer cover. 
This thin wood let the light shine through without a problem.

![VoicePuck-white](https://github.com/user-attachments/assets/48c8b008-5497-4cdd-bbc0-d8b4e1e2929a)


![VoicePuck-double](https://github.com/user-attachments/assets/48c8b008-5497-4cdd-bbc0-d8b4e1e2929a)

The entities that are available in Home Assistant

![HA-device](https://github.com/user-attachments/assets/dca3b294-eca2-4e0a-87b3-f8b0228a2dab)
