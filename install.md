# Install Apache Cordova

This tutorial is based on the Apache Platform Guide:  
https://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html

## Install JDK
Install JDK manually:  
http://askubuntu.com/a/55960/260035

Edit the ~/.profile file by adding the following lines:
```text
PATH=$PATH:$HOME/Programs/android-sdk-linux/tools:$HOME/Programs/android-sdk-linux/platforms
JAVA_HOME=/usr/lib/jvm/jdk1.8.0_65
```

And updates the user profile:
```bash
source ~/.profile
```
