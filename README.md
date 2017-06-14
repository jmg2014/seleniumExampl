# Selenium Grid

	This is an example of a Selenium Grid

## Run the hub

```java
java -jar selenium-server-standalone-3.0.1.jar -role hub &
``` 

## Run a node
```java
java -jar selenium-server-standalone-3.0.1.jar -role node -nodeConfig Grid-Node.json &
``` 

## Example of a node
```json
{
  "capabilities":
  [
    {
      "browserName": "firefox",
      "maxInstances": 5,
      "platform": "WIN10",
       "seleniumProtocol": "WebDriver",
      "webdriver.gecko.driver": "geckodriver.exe"
    },
    {
      "browserName": "chrome",
      "maxInstances": 5,
      "platform": "WIN10",
      "seleniumProtocol": "WebDriver",
      "webdriver.chrome.driver": "chromedriver.exe"
    },
    {
      "browserName": "MicrosoftEdge",
      "maxInstances": 5,
      "platform": "WIN10",
      "seleniumProtocol": "WebDriver",
      "webdriver.edge.driver": "MicrosoftWebDriver.exe"
    },
    {
      "browserName": "internet explorer",
      "maxInstances": 5,
      "platform": "WIN10",
      "version":11,
      "seleniumProtocol": "WebDriver",
      "webdriver.ie.driver": "IEDriverServer.exe"
    }
  ],
  "proxy": "org.openqa.grid.selenium.proxy.DefaultRemoteProxy",
  "maxSession": 5,
  "port": 5555,
  "register": true,
  "registerCycle": 5000,
  "hub": "http://192.168.0.106:4444/grid/register/",
  "nodeStatusCheckTimeout": 5000,
  "nodePolling": 5000,
  "role": "node",
  "unregisterIfStillDownAfter": 60000,
  "downPollingLimit": 2,
  "debug": false,
  "servlets" : [],
  "withoutServlets": [],
  "custom": {}
}
``` 
