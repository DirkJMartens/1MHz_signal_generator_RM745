# 1MHz_signal_generator_RM745
Implementation of the RM745 1MHz sine/triangle/square wave signal generator with added DRO 

- The model is a ROGEMA, RMa745, originally designed in 1985
- PCB is double-sided THT with a mix of various CMOS and TTL ICs. 
- Uses a 1MHz crystal as a starting frequency, which is divided down to 100Hz. 
- This is used as one of the input signals for a CD4066 PLL.
- The other input signal is a CD4059 "divide-by-N" counter.
- Four thumbwheel switches allow the setting of the actual divider setting.
- Using this, a frequency between 100Hz and 1MHz is generated.
- This can be selected to be divided further by 10 and 100.
- Final result is a square wave between 1Hz and 1MHz.
- This square wave is used as an input signal of an XR2206.

- Since 1MHz crystals are quite hard to find nowadays, it was replaced with a 10MHz version.
- A CD4510 (dual BCD counter) was added to divide to 1MHz and a 74LS04 as a signal shaper. 

- An addition to the original design is an ATMega328p microcontroller as a frequency meter.
- This drives an 8-digit 7-segment display based on a MAX7219 via I2C.
- The output frequency is thus shown on a digital readout.
- Note the frequency displayed is measured from the square wave output, not merely displaying the desited value. 
