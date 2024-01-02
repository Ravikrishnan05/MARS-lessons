# MARS-lessons
control system of rover.

## MCU  
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

 stm32 family
//## blackpill


GPIO
GPIO pin is customizable and can be controlled by the software.
Pin Mode:
~ input or output
~ analog
~ alternate function (AF)
Naming GPIO pins
PA7 -Port A,pin 7
PE15 -Port E,pin 15
## Fuses 
In general, the fuse should be rated at least 125% of the motor's full-load current (FLA)
xceeding 225% of the FLA is generally not recommended

Fast-acting fuses: These blow quickly in response to high currents, offering excellent protection against short circuits.
However, they *might also trip during temporary inrush currents during motor startup, leading to *nuisance tripping.

"*Time-delay fuses: These tolerate short-term overloads better than fast-acting fuses, making them suitable for motors and other applications with expected current surges. They offer a better balance between protection and operational continuity.

Dual-element fuses: These combine a fast-acting and a time-delay element, providing rapid short-circuit protection while allowing for temporary overloads. They're ideal for circuits with sensitive components and high inrush currents.


Minimum recommended fuse size: 1.25 * 18.7 Amps ≈ 23.4 Amps
Maximum recommended fuse size: 2.25 * 18.7 Amps ≈ 42.3 Amps


## PID Controller 
open loop system ![Screenshot 2023-10-29 193717](https://github.com/Ravikrishnan05/MARS-lessons/assets/134152503/a5a69193-50e9-428f-8c78-0fe3d67c6f60)
speed depends on accelerator position 
problem with open loop system :
*if we are going uphill car slows down even if accelerator is in same position 
*in down hill car is goin to speed up so we need to let off the gas pedal in order to maintain the same speed.
this thing cant be done with open loop system.
closed loop system ![Screenshot 2023-10-29 193126](https://github.com/Ravikrishnan05/MARS-lessons/assets/134152503/abef884d-c792-48fc-acf1-601280e9efaf)

motor driver lm298n
esp32
pid 
power

## BMS
In general, the BMS does the following tasks:

* Detects unsafe operating conditions and ensures the safety of the host application and its user.
* Protects the cells of the battery from abuse.
* Enhances the life of the battery.
* Maintains the battery in a state which can fulfill the host application’s requirements

## TB6600 stepper motor driver
![TB6600-Stepper-Driver-Module](https://github.com/Ravikrishnan05/MARS-lessons/assets/134152503/1bb58911-1d24-4287-b037-cc90a6b2d6fd)
These modules have several safety functions as follows:

Overcurrent protection
under-voltage shutdown
overheating protection

High Voltage  

VCC: Motor power supply – 9-42V for 4A type 
GND: Ground
A+: Positive pin of coil 1
A-: Negative pin of coil 1
B+: Positive pin of coil 2
B-: Negative pin of coil 2
Signal  

PUL(CLK): Pins for controlling rotation steps
DIR(CW): Pins for controlling rotation steps
ENA: Enable the driver pin
5V: Voltage – 5V
## ROS
![image](https://github.com/Ravikrishnan05/MARS-lessons/assets/134152503/980e282d-7173-45a5-9fe7-622e436134d4)
https://www.youtube.com/watch?v=3A5xH2b5beg&list=PLPdFwncBNrd0mA9uOdKaTossDczzI_EQG&index=3
https://www.youtube.com/watch?v=9qZUjEsVWts
The rosserial ROS package uses Arduino’s universal asynchronous receiver/transmitter (UART) communication and converts the board to a ROS node that can publish ROS messages and subscribe to messages as well

Node:
 $ node really isn't much more than an executable file(either python or c++ script) within a ROS package. 
 $ ROS nodes use a ROS client library to communicate with other nodes. 
 $ Nodes can publish or subscribe to a Topic. 
 $ Nodes can also provide or use a Service.
Messages:
$ nodes communicate each other with a message it can be of any datatype
$ what ever messages you send can be are named 
Topic:
to communicate between 2 nodes we need topics 
A------>TOPIC----->B
A----->TOPIC----->B1,B2,B3,B4,B4 etc...(there can be many nodes.the nodes which subscribe to topic will get the data)
A is a PUBLISHER
B is a subscriber



## OOPS
### Names space
Namespace provide the space where we can define or declare identifier i.e. variable,  method, classes.
namespace  namespace_name 
{
    // code declarations i.e. variable  (int a;)
    method (void add();)
    classes ( class student{};)
}
## Linux commands

ls -used to identify the files and directories in the working directory
The pwd command is mostly used to print the current working directory on your terminal
This mkdir command allows you to create fresh directories in the terminal itself.

mkdir GeeksforGeeks/projects creates directory inside directory 
