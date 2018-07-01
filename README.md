# FoodTruckFinder

FoodTruckFinder is a command line program that displays San Francisco food trucks' name and address that are open at this moment.
 - Retrieve currently open food truck's name and address
 - Display 10 records each time
 - Records are sorted alphabetically by the name and address

The data is provided by [San Francisco Data API](https://dev.socrata.com/foundry/data.sfgov.org/bbb8-hzi6)


## How to run
0. Clone or download the zip file, and enter the directory
```
https://github.com/jiguan/FoodTruckFinder.git
cd FoodTruckFinder
```
1. Build
```
javac -cp lib/jackson-annotations-2.9.5.jar:lib/jackson-core-2.9.5.jar:lib/jackson-databind-2.9.5.jar FoodTruckFinder.java
```
2. Execute:
```
java -cp lib/jackson-annotations-2.9.5.jar:lib/jackson-core-2.9.5.jar:lib/jackson-databind-2.9.5.jar:. FoodTruckFinder
```

## Notice
- This app is supposed to use within a short amount of time.
App displays food trucks' infor based on the time when we send the request. If a user sends a request, but view the next page infor 1 hour later, the result is not accurate anymore.
- Do not send requests too often.
This app has been registered and there should be no throttle API requests that are using an application token. However, if the app prints out an exception showing the response code is ```429```, that means you are considered as a malicious user.
