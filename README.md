# ESP8266-OTA-Blink-Blink

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

## Usage

* Install the SDK via http://docs.platformio.org/en/latest/ide/vscode.html
* Create a new empty github project (with README.md and LICENSE, if you like)
* Copy the files `src/main.cpp platformio.ini .gitignore` into the checkout folder of your new project.
* `git add * .gitignore`
* Start `code` -> locate 'PIO Home' (if it is not there, click on the Alien Face on the left, that should open it.
* Click 'PIO Home' -> open Project -> locate your new checkout folder -> open.
* Click open platformio.ini -> check if `upload_port` and `upload_protocol` are commented. That defines if we use USB or OTA.
* Click open src/main.cpp -> change the hostname "BlinkBlink_" and the accesspoint name "BlinkBlink_AutoAP" to match your project.
* At the bottom blue bar, hit the checkmar icon to 'Build'. The initial build takes long.
* At the bottom blue bar, hit the right arrow icon to 'Upload'.
* The LED should start blinking, when all is done, and the chip got its reset.
* Connect via HTTP and change the blinking.
* Happy hacking!
