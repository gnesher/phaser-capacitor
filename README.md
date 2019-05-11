# Phaser-Capacitor boilerplate
This skeleton app allows you to easily develop a Phaser 3 game for iOS / Android / Desktop using the Ionic Capacitor library. It uses Typescript (though can also be written in JS) and Webpack

* Ionic Capacitor is still in Beta and there are some bugs / quirks that are still being ironed out. Head to https://github.com/ionic-team/capacitor to find more about it's current progress.

* important! Electron recently came out with a major release (5) which is still not supported by Capacitor at the moment. 

### Installation
Simply clone or download the repository and then run 
```npm install``` within the folder

### Development
To set up a webpack development server simply run ```npm run dev``` you can also run ```npm run build``` to create a production build

### Deployment
In order to set up a deployment target simply run ```npx cap add <platformName>``` where platformName can either be android, ios or electron - directory with the platform name will be created.

once you've set up your deployment target simply run ```npm run build-<platformName>``` - for example ```npm run build-android``` this will build the app to the dist folder, copy the files into the Android project and lunch Android Studio. Running an iOS build works similarly just with Xcode

> keep in mind - the build process will fail if you have not installed the necessery software required to develop for your requested platform (Android / iOS). 

Electron builds work a little differently as there's no IDE (like Android / Xcode) that is used to run them. Once you run ```npm run build-electron``` simply enter the Electron folder ```cd electron``` and then run ```npm run electron:start``` to have the Electron app start

> If you wish to bundle your Electron app you will need to install a seperate bundler like electron-builder https://github.com/electron-userland/electron-builder. A complete guide can be find in the supplied link and there are additional bundlers you can choose.

> Webpack exposes a global variable called BUILD_TARGET which contains the target platform (ios, android, electron or web) - web is the default when not building for a specific platform

### important
- While multiple deployment targets are supported different targets (desktop / mobile) will likely require some code changes.
- This is still a work in progress, comments & suggestions are welcome
- Some users reported problems with running the electron app in the first attempt. If you encounter a problem when running ```npm run electron:start``` You might need to run ```npm install``` within the electrong folder first.

Guy N.

