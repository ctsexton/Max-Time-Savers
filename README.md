# Max-Time-Savers
A collection of Max/MSP abstractions that have saved me a lot of time. 

cts.buffer_loader: this patch creates and loads buffers for all the WAV files in a folder. All buffers are assigned a name globally accessible via the buffer_items coll object - click on Buffer List to view.

cts.enc_to_range: takes directional values (1 and -1) and creates a virtual slider between 0. and 1. Default resolution is 100 steps but optional arguments set number of steps, initial step and exponential scaling. i.e. [enc_to_range 1000 500 2] defines a slider range of 1000 steps from 0. to 1. beginning halfway through the range but exponentially scaled with a base value of 2 (so output begins around 0.25). 

cts.patt_rec: interface to the [seq~] object. Attach a momentary button to the right inlet (1 pressed down, 0 on release). Press once to arm the recorder, then input gestural or control data to be sequenced in left inlet, recording begins when the first piece of data is received until the momentary button is pressed again - and looping is engaged. Press the momentary button again to stop/start looping. Hold the button down for 1 second to delete the data and reset the pattern recorder. The object state is reported out of the right outlet, which is useful to assign colours to an LED on a hardware control interface. Sequence position (signal) is reported out the middle outlet. 
