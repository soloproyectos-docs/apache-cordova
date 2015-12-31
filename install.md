# Install Apache Cordova CLI

This tutorial describes the necessary steps to install and prepare [Apache Cordova CLI](https://cordova.apache.org/) on **Ubuntu 14.04**. Apache Cordova requires de following programs:

* [Git client](https://git-scm.com/)
* [NodeJs](https://nodejs.org/en/)
* [Node Package Manager (npm)](https://www.npmjs.com/)
* [Java Development Kit 7 or later (JDK)](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
* [Android SDK tools](http://developer.android.com/sdk/installing/index.html)
* [GenyMotion](https://www.genymotion.com/#!/) (Optional)

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

and change the environment `PATH` path variable by adding the following line to the `~/.profile` file (**replace `<jdk-dir>` by the correct directory**):
```bash
export JAVA_HOME=/usr/lib/jvm/<jdk-dir>
```

and finally re-logging to make the changes persistent.

## Install Android SDK tools

1. Download the Stand-alone SDK tools (or, if you prefer, the Android Studio bundle):  http://developer.android.com/sdk/installing/index.html

2. Unzip the file in an appropriate place. **From now on `<android-sdk-dir>` refers to the Android SDK installation directory.**

3. Open Android Manager (`<android-sdk-dir>/tools/android`) and install 'Android SDK Platform-tools', 'Android SDK Build-tools', 'Android Support Repository (Extras)' and 'Android 5.1.1' (API 22). This process may take several hours and it requires, at least, a lot of available gigabytes.

4. Change the environment `PATH` variable include the `<android-sdk-dir>/tools` and `<android-sdk-dir>/platform-tools` directories:

  Open the `~/.profile` file with your preferred editor and add the following line to the end (**replace `<android-sdk-dir>` by the correct directory.**):
  ```bash
  export PATH=$PATH:<android-sdk-dir>/tools:<android-sdk-dir>/platform-tools/
  ```

  and finally re-logging to make the changes persistent.
  
## Install GenyMotion (Optional)

The Android SDK emulator is slow, heavy and buggy. That's the reason why I decided to install [GenyMotion](https://www.genymotion.com). **It is not a free program**. It requires a monthly subscription payment. But for trying purposes you can use a free version.

1. Install VirtualBox:
  ```bash
  sudo apt-get install virtualbox
  ```

2. Download and install GenyMotion (free version). **From now on `<genymotion-dir>` refers to the GenyMotion installation directory**:  
https://www.genymotion.com/#!/download

3. Open GenyMotion (`<genymotion-dir>/genymotion`) and add a virtual device.

## Install Apache Cordova CLI
Instructions are based on:  
https://cordova.apache.org/docs/en/latest/guide/cli/index.html#link-2

1. Install the command line interface (CLI):

  ```bash
  # install the command line interface (CLI) globaly (-g)
  $ sudo npm install -g cordova
  
  # verify that cordova was installed correctly
  $ cordova -v
  5.4.1
  ```
  
## Test Apache Cordova CLI

1. Create and compile a test project

  ```bash
  # create a project
  $ cordova create test com.my_domain.test Test
  $ cd test
  
  # add, compile the android platform
  $ cordova platform android
  $ cordova build android
  ```
2. Open GenyMotion (`<genymotion-dir>/android`), start an emulator and run the test application

  Using GenyMotion is optional. You can run the following command directly. In that case Apache Cordova will open the Android SDK Emulator. But I prefer to use GenyMotion for the reasons commented previously.
  
  ```bash
  $ cordova run android
  ```
