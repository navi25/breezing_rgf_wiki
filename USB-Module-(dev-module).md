This module is an interface for [UART(Universal Asynchronous Receiver/Transmitter)](https://en.wikipedia.org/wiki/Universal_asynchronous_receiver-transmitter) on the user's system. 

UART Serial library for node used 

* Start with connection parameters which are:
  * ..
  * ..

* Get all list of Com Ports (Communication Ports) available on the device.

* Find out which one of the ports, the mask device is using. It can be found using **TAG - Prolific Serial**

* Give the user a dropdown to select between the ports with the **Prolific Serial** tag. (If there are multiple mask device are added then we will have multiple ports with this tag.)

* Connect button to connect with this port.

* We will get one transmission buffer and one receiver buffer. Both of these buffers will be of ASCII char streams.


### Remarks

This module caused a lot of problem in setup. (I was using [**"node-serialport"**](https://github.com/node-serialport/node-serialport) module. Tried with [**"usb"**](https://github.com/tessel/node-usb) too but the former is better.) 
The reasons are:
 - None of the usb modules work with browsers for security reasons and so make calls from electron module instead of react.

