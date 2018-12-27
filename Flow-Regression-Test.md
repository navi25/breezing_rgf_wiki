This test builds the flow model using the Regression Model.

* There will be total of 11 flow rates (in l/min): 0, 5, 10, 20, 40, 60, 80, 100, 120, 150
* For each flow rate, get 400 data points. Each data point will have: 
  * Pressure Sensor Value
  * Temperature sensore Value
  * Barometer Value
* For each flow rate, take average of 400 data points for each sensors and then do the following transformations:
  * Let F1, P1, T1, B1 be initial flow rate, average Pressure value, avg Temp value, avg Barometer value,
  * Use **CorrectionFunction()** which takes T1 and B1 values to caluclate correction factor which will have range- [0,1].
  * Multiply **correction factor** with original flowRate value, F1 to get new flowRate value as F1*.
  * Now Take P1 and transform each pressure value by taking square root of [P(i) - P(1)]/600 for each ith Pressure value and Name the new Pressure value as P(i)*.
  * Make a mapping from F(i)* to original P(i)*. This way we will get 11 data points for 11 flow rates.
  * Use Linear regression model to fit this data point to straight line in form of y = mx + c. 
  * Ignore value of **c** and write the value of **m** back to the mask device.

### Commands Used
* To get data
{"command":5,"length":4,"sensorcodes":"0,1,2,3","numsamples":400,"sampletime":1000}
* Data is recieved in form of JSON as
{"command":5,"length":4,"sensor0":0.573,"sensor1":0.573,"sensor2":0.573,"sensor3":0.573}\r\n

Sensor codes are:
* PhotoDiode 1 : 0 ; PhotoDiode 2 : 1 ; PhotoDiode 3 : 2 ; PhotoDiode 4 : 3
* Flow sensor: 4
* Barometer : 5
* Temperature: 6
* Humidity : 7


  


