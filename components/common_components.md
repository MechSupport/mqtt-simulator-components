# Common Components
This file is to document common components to be used in the designs. These components are to be used in as many designs as possible to reduce individial cost through bulk buying and to make maintenance replacements more accessible.

## Electronic Components

### Microcontrollers (I/O)
* ATTiny212: This small microcontroller is to be used for I/O devices requiring no more than 2 control signals (not including SPI pins, 8 available total)
* ATTiny214: This small microcontroller is to be used for I/O devices requiring no more than 8 control signals (not including SPI pins, 12 available total)
* ATTiny416: This small microcontroller is to be used for I/O devices requiring no more than 14 control signals (not including SPI pins, 18 available total)
* ATTiny417: This small microcontroller is to be used for I/O devices requiring no more than 18 control signals (not including SPI pins, 22 available total)

### Microcontrollers (Panel Controller)
* ESP32: This microcontroller board is to be used for wireless panel controllers
* Teensy 4.1: This microcontroller board is to be used for ethernet panel controllers

### MQTT Server
* RPi 4: Easily accessible and maintainable

## Passive Components
* 0603 SMD Profile: Use this size for as many of the components as possible

## Indication and Optoelectronic
* IN-PI55QATPRPGPBPW-40: Any 5050 addressable RGB will do. Using addressable LEDs decreases component cost and modularity (e.g. indicators can be any color, as defined by a server command)

## Mechanical Components
