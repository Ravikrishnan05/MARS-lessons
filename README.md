# MARS-lessons
control system of rover.

MCU  
*stm32f411ceu6
ground and vcc should never be swapped
dont power vbat with  other(stlink or serial monitor port) {only vbat}
analog pins if they are used as digital pins it gives 0 or 255 
pwm pins to controlling speed of motors by voltage 
dont use usb pins

//flash memory 512kb
Flash memory is made up of small-small memory cells which are made up of floating-gate transistors.
array of memory cells.
electrical signals to add memory.
//SRAM 128kb
The SRAM is volatile in nature that means the data stored in it gets all wiped out once the power supply is cut.
//crystal oscillator
It has very high quality factor.
crystal oscillator are essential for generating clock signal in microcontrollers
when ac voltage of particular frequency is applied the piezoelectric material oscillates with same frequncy it is 
inverse piezo electric effect.

# stm32 family
## blackpill
