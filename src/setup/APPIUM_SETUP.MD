Open the command promt and check for appium version using `appium --version`.

In case the version is not returned we need to install it using the command `npm install -g appium@latest` here even if you do not mention latest, the latest will get downloaded and if we need any specifi version then we need to mention it after @ (Eg: appium@2.11.2)

Point to be noted Installing Appium 2.0 only installs Appium serve but not the drivers since all the drivers have been isolated from Appium server app. We will install the Appium UIAutomator2 Driver for Android and Appium XCUITest Driver for iOS separately.

In order to start the appium server we need to run the command `appium`
and once the appium server is up and running in order to stop it we need to use Ctrl+C on both Windows and Mac

There is another tool called as [appium-doctor](/src/setup/APPIUM_DOCTOR_SETUP.MD)

To list out all the drivers for appium we can use the command `appium driver list` Once you run this command you would be getting an output like below

```
√ Listing available drivers
- uiautomator2 [not installed]
- xcuitest [not installed]
- espresso [not installed]
- mac2 [not installed]
- windows [not installed]
- safari [not installed]
- gecko [not installed]
- chromium [not installed]
```

To install any of the driver we can use the command `appium driver install uiautomator2` (this would install the uiautomator2 driver for appium)
In case you want to check any of the driver updates you can use the command `appium driver list -updates`

