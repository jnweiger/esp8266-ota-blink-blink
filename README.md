# esp8266-ota-blink-blink

The last program you flash per USB - Everything else works over-the-air -- until you break it.
Then you come here again.

Done with visual-studio code and platformio.

This code enables OTA (over-the-air) programming of a wemos or esp8266 device.
It features the standard wlan-chooser procedure via an initial access-point (SSID: BlinkBlinkAutoconnectAP).
I have not yet found a way to become a permanent access point (That would be good for robustness, currently
it seems we always need another WLAN to connect to.)

The code also features a crude HTML generator and response parser. That might server as a template for 
simple web applications. (Avoiding the need of an android or iphone app, for simplicity).

The builtin web-app can choose differnt blinking patterns on the onboard LED of the ESP8266.



