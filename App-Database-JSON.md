The database for the app is handled by [**electron-store**](https://github.com/sindresorhus/electron-store) npm module which in turn is just a JSON file-based database system.

There are major 4 kinds of top-level data needed for the application:-

* Device - This contains information about a specific device (currently connected with the application) such as device name, device MAC Address etc.
* Flow - This contains information about flow data for the device for the various flows.
* Sensor - This contains information about sensor data for the device.
* PD - This contains information about PD data for the device.