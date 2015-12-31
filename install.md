# Install Apache Cordova

This tutorial describes the necessary steps to install and prepare [Apache Cordova](https://cordova.apache.org/) on **Ubuntu 14.04**. Apache Cordova requires de following programs:

1. [NodeJs](https://nodejs.org/en/)
2. [Node Package Manager (npm)](https://www.npmjs.com/)
3. [Java Development Kit 7 or later (JDK)](http://www.oracle.com/technetwork/java/javase/downloads/index.html)

Instructions are based in the following turorial:  
https://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html

## Install NodeJS

Instructions are based on:  
https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions

```bash
$ sudo apt-get install curl
$ curl -sL https://deb.nodesource.com/setup_4.x | sudo -E bash -
$ sudo apt-get install -y nodejs

# verify that nodejs was installed correctly
$ node -v
v4.2.4
```

## Install Node Package Manager (npm)
Instruction are based on (Fancy Install section):  
https://www.npmjs.com/package/npm

```bash
$ sudo su
curl -L https://npmjs.org/install.sh | sh

# verify that npm was installed correctly
$ npm -v
3.5.2
```

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
