# Install Apache Cordova

This tutorial describes the necessary steps to install and prepare Apache Cordova on Ubuntu 14.04.

## Install NodeJS

Instructions are based in the following tutorial:  
https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions

```bash
$ sudo apt-get install curl
$ curl -sL https://deb.nodesource.com/setup_4.x | sudo -E bash -
$ sudo apt-get install -y nodejs

# verify that nodejs was installed correctly
$ node -v
v4.2.4
```

This tutorial is based on the Apache Platform Guide:  
https://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html

## Install JDK
Install JDK **manually**:  
http://askubuntu.com/a/55960/260035

and add the following line to the ~/.profile file (**paths may vary**):
```text
JAVA_HOME=/usr/lib/jvm/jdk1.8.0_65
```

and reload environment variables:
```bash
source ~/.profile
```

## Install the Android SDK
Download and unzip the SDK for linux (android-sdk_r*-linux.tgz):  
http://developer.android.com/sdk/index.html#Other
