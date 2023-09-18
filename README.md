# 1MHz_signal_generator_RM745
Implementation of the RM745 1MHz sine/triangle/square wave signal generator with added DRO 

- PCB is a RMA745, designed by Roger Martens in 1985 
- Uses a 1MHz crystal as a starting frequency, which is divided down to 100Hz.
- This is used as one of the input signals for a CD4066 PLL.
- The other input signal is a CD4059 "divide-by-N" counter.
- Four thumbwheel switches allow the setting of the actual divider setting.
- Using this, a frequency between 100Hz and 1MHz is generated.
- This can be selected to be divided further by 10 and 100.
- Final result is a square wave between 1Hz and 1MHz.
- This square wave is used as an input signal of an XR2206.

- An addition to the original design is an ATMega328p microcontroller as a frequency meter.
- This drives an 8-digit 7-segment display based on a MAX7219 via I2C.
- The output frequency is thus shown on a DRO.
- Note the frequency displayed is measured from the output, not derived from the desited value.
