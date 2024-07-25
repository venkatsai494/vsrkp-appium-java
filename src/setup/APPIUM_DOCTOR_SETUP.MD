This can be used to validate proper environment setup for Android and iOS automation, and identify any common configuration issues. This would help to diagnose and fix common Node, iOS and Android configuration issues. To install this we need to run the command `npm install -g appium-doctor`.
After successfull installation you can check the version using command `appium-doctor --version`

Let us check the missing dependency on our system by running the command `appium-doctor --android`

In case the appium-doctor is deprecated you need to uninstall appium-doctor either by using command or by manually moving to the folder C:\Users\USER\AppData\Roaming\npm and removing all the files related to appium-doctor and also the appium-doctor folder from C:\Users\USER\AppData\Roaming\npm\node_modules

Then we need to run `npm install @appium/doctor --location=global` command to install the appium-doctor and later check the version of appium-doctor (Currently used: 2.1.9)

