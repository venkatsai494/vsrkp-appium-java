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

Other appium commands can be used as below

| Flag                      | Description                                    | Use Case                                                               | Example                                                |
|---------------------------|------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------|
| --address                 | IP address for the server to listen on         | Bind to specific network interface or make accessible on other devices | appium --address 192.168.1.100                         |
| --port                    | Port number for the server to listen on        | Change default port (4723) or for network configuration                | appium --port 4724                                     |
| --session-override        | Allow multiple sessions with same capabilities | Run multiple tests on same device/emulator simultaneously              | appium --session-override                              |
| --log-level               | Set log level for the server                   | Control amount of information logged (debug, info, etc.)               | appium --log-level debug                               |
| --log-timestamp           | Prefix log lines with timestamps               | Easier tracking of events in the log                                   | appium --log-timestamp                                 |
| --local-timezone          | Set server's time zone                         | Ensure accurate timestamps, especially for different time zones        | appium --local-timezone America/Los_Angeles            |
| --chromedriver-executable | Path to ChromeDriver executable                | For Chrome or Chromium-based web automation                            | appium --chromedriver-executable /path/to/chromedriver |
| --allow-insecure          | Enable specific insecure features              | Use carefully as it introduces security risks                          | appium --allow-insecure get_server_logs                |
| --relaxed-security        | Enable all insecure features                   | Only use in development or with trusted apps                           | appium --relaxed-security                              |

The above table is generated using [this](https://www.tablesgenerator.com/markdown_tables#) website.