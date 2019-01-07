This module tests the Photo Diodes present in the BreezingPro Mask Device against various testing Conditions.
There are a total of 5 various testing conditions and a total of 4 Photo Diodes which all will be tested simultaneously against those 5 testing conditions. Also, there are low and high values for voltage of photodiodes and if the voltage is within the range then the test pass else fails.

### Step-by-Step Working

1. The five testing conditions are:
   * Blank Cartridge
   * Black Cartridge
   * Empty Cartridge
   * New/Fresh Cartridge
   * Used Cartridge

2. There are default low and high voltage values for each photodiode as per the testing conditions which are:
   * **Blank Cartridge** - LOW - XX V ;  High - XX V
   * **Black Cartridge** - LOW - XX V ;  High - XX V
   * **Empty Cartridge** - LOW - XX V ;  High - XX V
   * **New/Fresh Cartridge** - LOW - XX V ;  High - XX V
   * **Used Cartridge** - LOW - XX V ;  High - XX V

3. A user can also enter a specific value for a particular Photo-Diode for a particular testing condition.

4. Get the data for time input by the user itself. Have a slider or input for the time from 1 sec to 60 sec.

5. Once the setup is done, the User can select one of the test conditions and press **Start** button. The module will start getting Voltage values for all the 4 diodes simultaneously which is then stored in 4 different CSV for 4 diodes with all the details. The CSV file will have the following columns:-
   * S.No - Serial Number
   * PD Id - Id of Photo Diode
   * Test Id - Id of Test Condition
   * PDL - Lower Voltage value of PD (In V units)
   * PDH - Upper Voltage value of PD (In V Units)
   * PDC - Current Voltage value of PD (In V units)
   * Result - Pass/Fail (depending upon if PDC lies between PDL and PDH or not).

6. The data will be plotted also.

7. There will be a button to generate CSV which will generate 4 CSV for 4 different photodiodes