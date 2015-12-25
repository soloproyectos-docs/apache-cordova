# Installing lightweight emulators

You can either install ripple, a web based emulator, or GenyMotion, a desktop application.

## Installing Ripple

Instructions based on the following tutorials:
* https://bradb.net/blog/testing-ionic-cordova-apps-with-ripple/
* https://khangdinh.wordpress.com/tag/cordova/

**Installs, prepares and launches the ripple emulator in a new browser window**
```bash
sudo npm install -g ripple-emulator
cordova prepare android
ripple emulate
```
