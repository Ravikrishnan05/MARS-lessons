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
crystal oscillator are essential for generating clock signal in microcontroller
when ac voltage of particular frequency is applied the piezoelectric material oscillates with same frequncy it is 
inverse piezo electric effect.
//# Jetson AGX Orin Developer Kit

//# stm32 family
//## blackpill

PID Controller 
open loop system ![Screenshot 2023-10-29 193717](https://github.com/Ravikrishnan05/MARS-lessons/assets/134152503/a5a69193-50e9-428f-8c78-0fe3d67c6f60)
speed depends on accelerator position 
problem with open loop system :
*if we are going uphill car slows down even if accelerator is in same position 
*in down hill car is goin to speed up so we need to let off the gas pedal in order to maintain the same speed.
this thing cant be done with open loop system.
closed loop system ![Screenshot 2023-10-29 193126](https://github.com/Ravikrishnan05/MARS-lessons/assets/134152503/abef884d-c792-48fc-acf1-601280e9efaf)

