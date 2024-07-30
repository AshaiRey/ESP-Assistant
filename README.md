# ESP-Assistant
An ESP32 S3 voice assistant for Home Assistant. Light weight and should compile on low end systems.

The main goal of this project was to create a voice assistant (VA) for HA that is not depending on external files*. A second requirement was that for compiling you don't need much resources. This yaml compile many times faster then the ESP32-S3_box bersion. This version of the voice assistant is also capable to set timers.

_* There is one small dependency in the code if you want a sound when a timer is finished. This dependecy is only there when compiling. A future release may solve this. For now this isn't a big show stopper_
