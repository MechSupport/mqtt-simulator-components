# mqtt-simulator-components
Components that use MQTT to quickly and efficiently build full or partial cockpit simulators.

# What is this project?
This project will create modular devices and designs for a variety of similator systems. The overall intent of the project is to reduce the amount of time needed to make a simulator from months-years to days. To do this, the simulator needs to be broken into modular parts that can be quickly programmed and connected.

# What are the components?
The simulator architecture is broken into four discrete elements consisting of; the *simulator software*; the *MQTT server*; the *panel controller*, and; the *input/output devices*.

## Simulator Software
This is the software that runs the simulation. Note that this does not have to be intentionally designed as a simulator. The software chosen for the initial build of this system was Mechwarrior 5: Mercenaries, as it has many controls and a good support system through both modders and the original developers.

## MQTT Server
This is a standard MQTT server. It takes information from the simulator software and provides it to the panel controllers via IP messages.

## Panel Controller
The panel controller connects the I/O devices to the ethernet network. It can be either an off the shelf RPi, an ESP32 or any other IoT device with SPI support. It operates as the SPI master while the I/O devices are the SPI slaves.

The name 'Panel Controller' comes from the physical layout of a cockpit. Panels are sections of the cockpit that have similar gauges or switches, all affixed to one solid surface. Each of these surfaces would have a dedicated panel controller that is then connected to the network.

## Input / Output Devices

# Design Principles

These principles are up for discussion, however the reasoning for including or not including them are stored here.

## Software / Communication Protocols

### MQTT
MQTT was implemented becuase it requires a small amount of computational and network traffic. Many microcontrollers with built in WiFi or Ethernet have MQTT support in their libraries and a plethora of documentation on how to make them IoT connected.

## Physical Components

### EveryI/O Device Has a Microcontroller
A dedicated microcontroller for each I/O device increases the overall useability of the system while decreasing the number of connections from the panel controller to the I/O device. In essence, the microcontroller allows for serial communication over parallel for components that may have a large number of switches (e.g. MFD or buttonbox) or a complicated output (e.g. altimeter). The increase in cost for each I/O device is outweighed by the increase in modularity. 

This also means that a gauge could be unplugged from one panel controller, moved to another panel (or even another cockpit entirely if on the same network), and plugged in via the SPI connection and it would start to work right away.


## 
