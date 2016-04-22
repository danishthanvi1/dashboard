[![Build Status](https://travis-ci.org/netbeast/dashboard.svg)](https://travis-ci.org/netbeast/dashboard)
![dependencies](https://david-dm.org/netbeast/dashboard.svg)

# Netbeast dashboard – Desktop Version
### Connect everything. Regarless its brand or technology,

This is a web panel from you can install, manage or publish IoT applications. For every platform. Mac, Windows & Linux app/repo. Check out our http://docs.netbeast.co for builds for Raspberry Pi, Beagle Bone and Arduino.

[<img src="https://slack.com/img/slack_hash_128.v1442100037.png" height="24px" width="auto"/> Join us in Slack!](https://netbeastco.typeform.com/to/VGLexg)

## Current Status :rocket:

Dashboard code will be updated continually. Take that into account to update your applications until auto-updating system is implemented (you can also collaborate with it) :smile:

Application is currently available for the following OS:

##### MAC :apple:

######Download [here](http://bit.ly/1TgUVhO) now!

#####LINUX :rocket:

######32 bits version [here](http://bit.ly/1VglPtE)

######64 bits version [here](http://bit.ly/22KDZTv)

#####WINDOWS :package:

######32 bits version [here](http://bit.ly/23Wcc4W)

######64 bits version [here](http://bit.ly/1VglOWD)


## Run it locally
This is the desktop version of the Netbeast dashboard. If you want to run the desktop version locally run:

```
git clone -b electron --single-branch https://github.com/netbeast/dashboard
cd dashboard
npm install  #Installing all dependencies
npm start
```

After that, an Electron window of the Netbeast dashboard will appear.

## Compile the desktop version for MACOS

If you want to create the Netbeast dashboard application for mac, follow these steps:

##### 1. Install last Nodejs version (In this example I have v5.7.1) & npm packages

```
# Install electron-packager
npm install -g electron-packager

# Install appdmg
npm install -g appdmg

#Install node-gyp
npm install -g node-gyp

# Clone the Netbeast dashboard
git clone -b electron --single-branch https://github.com/netbeast/dashboard

# Install all dependencies
cd dashboard
npm install
```

- You can find more information about how these packages work: [electron-packager](https://github.com/electron-userland/electron-packager) [appdmg](https://github.com/LinusU/node-appdmg)

- We also recommend having the last version of Nodejs. You can download it from [here](https://nodejs.org/en/)

##### 2. Create the Mac App

```
electron-packager dashboard Netbeast --platform=darwin --arch=x64 --version=0.37.2 --icon=dashboard/desktop_app/icon.icns --version-string.CompanyName=Netbeast --version-string.ProductName=NetbeastDashboard
```

-  Check the electron version ```./node_modules/.bin/electron -v```in my case: 0.37.2

##### 3. Create the Mac dmg

Once you have created the Netbeast dashboard app you can run the following command:


```
cd Netbeast-darwin-x64

#Copy files from dashboard folder to the new one
cp ../dashboard/desktop_app/icon.icns ../dashboard/desktop_app/appdmg.json ../dashboard/desktop_app/background.png .

#Package to .dmg
appdmg appdmg.json ~/Desktop/Netbeast.dmg
```

- Then you will have the Netbeast.dmg file on your desktop :smile:

##Compile the desktop version for Linux

##### 1. Install last Nodejs version (In this example I have v5.7.1) & npm packages

```
# Install electron-packager
npm install -g electron-packager

#Install node-gyp
npm install -g node-gyp

# Clone the Netbeast dashboard
git clone -b electron --single-branch https://github.com/netbeast/dashboard

# Install all dependencies
cd dashboard
npm install
```

##### 2. Create the Linux App

```
electron-packager dashboard Netbeast --platform=linux --arch=all --version=0.37.2 --icon=dashboard/desktop_app/icon.icns --version-string.CompanyName=Netbeast --version-string.ProductName=NetbeastDashboard
```

- The result will be two folders: 
  - Netbeast-linux-ia32 : 32 bits version
  - Netbeast-linux-x64: 64 bits version

Now if you want to run the application go to the folder and double click on "Netbeast" :smile:

## Compile the desktop version for Windows

##### Building Windows apps from non-Windows platforms

Building an Electron app for the Windows platform with a custom icon requires editing the Electron.exe file. Currently, electron-packager uses node-rcedit to accomplish this. A Windows executable is bundled in that node package and needs to be run in order for this functionality to work, so on non-Windows host platforms, Wine needs to be installed. On OS X, it is installable via Homebrew.

You can find more information [here](https://github.com/electron-userland/electron-packager)

##### Create the Windows App

```
electron-packager dashboard Netbeast --platform=win32 --arch=all --version=0.37.2 --icon=dashboard/desktop_app/icon.ico --version-string.CompanyName=Netbeast --version-string.ProductName=NetbeastDashboard
```

- The result will be two folders: 
  - Netbeast-win32-ia32 : 32 bits version
  - Netbeast-win32-x64: 64 bits version

Now if you want to run the application go to the folder and double click on "Netbeast.exe" :smile:

## Problems

#####Sqlite3

Sometimes you can have some problems with sqlite3 npm package when electron tries to run it. In order to solve this problem you should follow these steps:

```
cd node_modules/sqlite3
npm run prepublish
node-gyp configure --module_name=node_sqlite3 --module_path=../lib/binding/node-v47-darwin-x64
node-gyp rebuild --target=0.37.2 --arch=x64 --target_platform=darwin --dist-url=https://atom.io/download/atom-shell --module_name=node_sqlite3 --module_path=../lib/binding/node-v47-darwin-x64
```

## Contribute

Take a look to our CONTRIBUTING file in order to see how you can be part of this project. [Contribue](https://github.com/netbeast/dashboard/blob/master/CONTRIBUTING.md)

If you are part of the Netbeast community don't forget to write down your name on the AUTHORS file. [Authors](https://github.com/netbeast/dashboard/blob/master/AUTHORS)

## Contact
* Visit our site [https://netbeast.co](https://netbeast.co)
* Mail us: staff [at] netbeast.co
* Report a bug or enter discussion at [issues](https://github.com/netbeast/docs/issues)
* Other resources: [Docs](https://github.com/netbeast/docs/wiki), Netbeast [API](https://github.com/netbeast/API)

[<img src="https://slack.com/img/slack_hash_128.v1442100037.png" height="24px" width="auto"/> Join us in Slack!](https://netbeastco.typeform.com/to/VGLexg)


<img src="https://github.com/netbeast/docs/blob/master/img/open-source.png?raw=true" height="140px" width="auto"/>
<img src="https://github.com/netbeast/docs/blob/master/img/open-hw.png?raw=true" height="140px" width="auto"/>
