Companion Android Application for Hip Angle Sensor [EE4591W: Senior Design].
The application will communicate with the UUID specified in the 'values' file, using GATT profile as specified by adafruit (the module chip used). Upon connection, each data point received from the physical device is saved in the internal storage of the smartphone, under /GATT/savedValues.txt && /GATT/lastValue.txt. These values are checked every 100 miliseconds, which are updated to the user interface. 
Pressing "Analyze" button will analyze the data (average and standard deviation of the angle).
Pressing "Connect/Disconnect" will search for the specified UUID and connect/disconnect.
Pressing "Calibarate" will send "00" to the physical device, which will interpret this as a calibaration request and do that in the sensors. 
Values sent should follow "XX" format (examples: 01, 07, 10, 34, ...).

The user interface (layout) was done by Kyle Roberts.
The parts of sending/receiving data was implemented based on the code provided by adafruit for developers (check https://learn.adafruit.com/introducing-the-adafruit-bluefruit-le-uart-friend/introduction).
