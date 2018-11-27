This modules get the device name (Breezing Pro Mask Device) and generate a barcode.

### Step-by-Step Working

1. Use USB Command to get the device name which will be of the format:
   * **B<8 numbers>** - This denotes that the device has a name
   * **FFFFFFFFF (9 Fs)** - This denotes that the device doesn't have a name and so it should be named first.

2. In case of **noName**, generate name in the format - **B<8 numbers>** as described below
   * First Letter should be **B**.
   * The first four letter is user input which can also be auto incremented with starting from 0000.
   * The last four letter is last four letter of the MAC Id of the Breezing Mask Device.

3. Generate Barcode which can also be printed. The input string for the barcode generator will be the device name.

