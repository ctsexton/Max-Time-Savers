# Max-Time-Savers
A collection of Max/MSP abstractions that have saved me a lot of time. Currently have only tested on Mac OS X but they should work on PC.

buffer_loader: _this patch creates and loads buffers for all the WAV files in a folder. All buffers are assigned a name accessible in the buffer_items _coll object - click on Buffer List to view.

enc_to_range: takes directional values (1 and -1) and creates a virtual slider between 0. and 1. Default resolution is 100 steps but optional arguments set number of steps, initial step and exponential scaling. i.e. [enc_to_range 1000 500 2] defines a slider range of 1000 steps from 0. to 1. beginning halfway through the range but exponentially scaled with a base value of 2 (so output begins around 0.25). 
