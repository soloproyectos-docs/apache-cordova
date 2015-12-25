# Lightweight Emulators

You can either install [ripple](https://www.npmjs.com/package/ripple-emulator), a web based emulator, or [GenyMotion](https://www.genymotion.com/), a desktop application. Personally, I recommend using GenyMotion.

## Installing GenyMotion

GenyMotion **is not a free** application. But, for personal use or training, you can download a free version:
https://www.genymotion.com/#!/download

Change the permissions to allow execution and double click.

## Installing Ripple

Instructions based on the following tutorials:
* https://bradb.net/blog/testing-ionic-cordova-apps-with-ripple/
* https://khangdinh.wordpress.com/tag/cordova/

**Installs, prepares and launches the ripple emulator in a new browser window**
```bash
# Install ripple emulator globaly via npm (Node Package Manager)
sudo npm install -g ripple-emulator

# Copies the static files
cordova prepare android

# Launches ripple in a new browser window
ripple emulate
```

**Fixing common problems**
```plaintext
Error:
    GET http://localhost:4400/config.xml 404 (Not Found)`
Solution:
    cp config.xml www/config.xml
```

```bash
Error:
    cordova :: Your application does not appear to match the platform you have selected. The version number in your configuration might not match the selected platform version or your configuration file has errors in it.
Solution:
    Edit the www/config.xml file and adds the following attribute to the widget node:
    xmlns:gap="http://phonegap.com/ns/1.0"
```
