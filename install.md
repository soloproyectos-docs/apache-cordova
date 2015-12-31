# Install Apache Cordova

This tutorial describes the necessary steps to install and prepare [Apache Cordova](https://cordova.apache.org/) on **Ubuntu 14.04**. Apache Cordova requires de following programs:

* [Git client](https://git-scm.com/)
* [NodeJs](https://nodejs.org/en/)
* [Node Package Manager (npm)](https://www.npmjs.com/)
* [Java Development Kit 7 or later (JDK)](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
* [Android SDK](http://developer.android.com/sdk/installing/index.html)

Instructions are based in the following turorials:  
https://cordova.apache.org/docs/en/latest/guide/cli/index.html
https://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html

## Install Git client

```bash
$ sudo apt-get install git

# verify that nodejs was installed correctly
$ git --version
git version 1.9.1
```

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
$ curl -L https://npmjs.org/install.sh | sh

# verify that npm was installed correctly
$ npm -v
3.5.2
```

The following command **won't work**:
```bash
$ sudo curl -L https://npmjs.org/install.sh | sh
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
$ source ~/.profile
```

## Install Android SDK (Software Development Kit)

1. Download the Stand-alone SDK tools (or, if you prefer, the Android Studio bundle):  http://developer.android.com/sdk/installing/index.html

2. Unzip the file in an appropriate place.  
**From now on `<android-sdk-dir>` refers to the Android SDK directory.**

3. Change the environment `PATH` variable to point to `<android-sdk-dir>/tools`
Open `~/.profile` with your preferred editor and adds the following line at the end of the file:
```bash
export PATH=$PATH:<android-sdk-dir>/tools
```
**Do not forget to replace <android-sdk-dir> by the Android SDK directory.**

And finally reload the user profile settings:
```bash
source ~/.profile
```

4. Open the android manager (`<android-sdk-dir>/tools/android`) and install the packages marked by default.
The previous action will install 'Android SDK Platform-tools', 'Android SDK Build-tools' and the latest Android API.

## Install Apache Cordova CLI
Instructions are based on:  
https://cordova.apache.org/docs/en/latest/guide/cli/index.html#link-2

```bash
# install command line interface (CLI) globaly (-g)
$ sudo npm install -g cordova

# verify that cordova was installed correctly
$ cordova -v
5.4.1
```
