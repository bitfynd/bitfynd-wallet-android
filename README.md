# Bitfynd
### Bitcoin Wallet app for Android

The app is based on decentralized P2P/SPV platform of BitcoinJ and on Bitcoin wallet app by Andreas Schildbach.

None of third-party servers are involved nor in storing, nor in transferring your Bitcoins - you're the master of your Bitcoins.

### Building the app

The source code of Bitcoin wallet app by Andreas Schildbach is transformed from Eclipse IDE format to Android Studio IDE format. Look for information online how to build an app from source code with Android Studio IDE.

Just import the source code of the app to Android Studio IDE as normal Android Studio project and you're ready to compile the code.

This source code of the app contains Gradle configuration which lets you to build 4 *flavors*  of the app *(read more about flavors: [link #1](http://goo.gl/DcX6ee), [link #2](http://goo.gl/CnIOr8))*:
- Mainnet release:
  - use the app with real Bitcoins, debugging disabled
  - ready to be uploaded to Google Play Store *(read the section below: "Releasing the app publicly")*
- Mainnet debug:
  - try the app with real Bitcoins and debug the app at the same time
  - for personal testing only
- Testnet release:
  - use the app with Tesnet Bitcoins, debugging disabled
  - ready to be uploaded to Google Play Store *(read the section below: "Releasing the app publicly")*
- Tesnet debug:
  - try the app with Tesnet Bitcoins and debug the app at the same time
  - for personal testing only

### Releasing the app publicly

To release this app on Google Play Store on your own (or just to publish it on the internet), follow these instructions:
- At first **you must to rename all instance values of *applicationId* (package name)** in Gradle configuration file *(app/build.gradle)*.

> **NOTICE:** Don't rename package name in AndroidManifest.xml file, otherwise you'll get many errors while compiling the app. Rename only *applicationId* (package name) in Grade configuration file - Gradle system will do all tasks automaticaly itself.

- Then **you must rename the app name** in string resources file *(app/src/main/res/values/values.xml - string value of "app_name")*.
- Next, **you must sign the app using your own keystore file**, because we don't provide our own keystore file publicly as only we're updating this app on Google Play Store using exactly our own unique *applicationId* (package name). So, just use your own *applicationId* (package name), app name and keystore file to publish your own app release based on this source code.

**If you won't follow the instructions above, you will run into these conflicts:**
- You won't be able to publish this app on Google Play Store, because our original app (Bitfynd) already uses the same *applicationId* (package name) and app name on Google Play Store!
- You'll confuse other users which app is the original one and which is a fork/copy released by other developers (unofficial one)!
- During installation it will overwrite existing original app (if any) on your and/or other users devices!

### Source Code

The app is based on Bitcoin wallet app for Android by Andreas Schildbach:

> Bitcoin Wallet app for your Android device. Standalone Bitcoin node, no centralized backend required.
> 
> [Source code on Github](https://github.com/schildbach/bitcoin-wallet), [Website](http://wallet.schildbach.de/)

The app is also using BitcoinJ:

> BitcoinJ library is a Java implementation of the Bitcoin protocol, which allows it to maintain a wallet and send/receive transactions without needing a local copy of Bitcoin Core.
> 
> [Source code on Github](https://github.com/bitcoinj/bitcoinj), [Website](https://bitcoinj.github.io/)

### License

This app is a free and opensource software, licensed under [GPLv3 license](http://goo.gl/jDcSYa).

### Warranty & Liability

According to GPLv3 license, there is basically no warranty and liability. It's your responsibility to audit the source code for security issues and to build, install and run the app in a secure way.
