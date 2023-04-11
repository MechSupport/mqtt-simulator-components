# Task List
This is a list of tasks associated with this project. They are broken into disciplines and information is held here on the status and who is working on them.

# Hardware Development
For all work involving physical designs.

## PCBs and Wiring
For all PCB designs and for wiring.

### Basic Analog Gauge
**MS** - Created a base PCB that controls a x27.589 stepper motor (commonly used in automotive design) using an H bridge rectifier. Future version will include a ATTiny414 (or equivalent) to communicate with panel controller via SPI. Noted problem of a missing resistor between controller and addressable LEDs. Do not use design without a 330 Ohm resistor between signal and digital input pin of LED.

### Basic Button Box
**MS** - Created schematic.

### Full Rotation Analog Gauge
In Progress / Not started

### Illumination Panel
In Progress / Not started

### Heads-Up Display
In Progress / Not started

## I/O Device Design
For the actual design of the components that the user will see.

### Speedometer
**MS** - Made a rough layout of a speedometer to match the basic analog gauge

### Thermometer
**MS** - Made a rough layout of a thermometer to match the basic analog gauge after spending way to much time coming up with what to call it before realising that the 'heat readout' from MW5 Hud is just a thermometer.

### Ammo Counter
**MS** - Made a rough layout of an ammo counter for use with illumination panel PCB. Will have bar graphs showing ammo and reload time.

# Software Development
For all working involving coding.

## I/O Device Programming
In Progress / Not started

## Panel Controller Programming
In Progress / Not started

## MQTT Server Programming
In Progress / Not started

## Simulator Programming

Not to include the actual creation of simulators. This category is to include the progress on methods on how to get information out of a simulator and into the MQTT server.

### Mechwarrior 5: Mercenaries
**Help Requested**

**MS** - Attempted to create a pyython file that could read memory of game while it was running to forward to MQTT sever. Game variables change places within memory between missions. (e.g. Heat was tracked sucessfully in one mission, on the next mission it lost track). Memory addresses were found using Cheat Engine. It is believed that for simpler games this method may be sucessful.
