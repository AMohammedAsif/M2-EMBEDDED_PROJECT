# Requirements

## Introduction

------------>>>>>>>>>>>   WATER LEVEL INDICATOR   <<<<<<<<<<<<--------------

The Water Level Indicator employs a simple mechanism to detect and indicate the water level in an overhead tank or any other water container.
The sensing is done by using a set of nine probes which are placed at nine different levels on the tank walls (with probe 9 to probe 1 placed in increasing order of height, common probe (i.e. a supply carrying probe) is placed at the base of the tank). The level 8 represents the “tank full” condition while level 0 represents the “tank empty” condition.
When the water-level is below the minimum detectable level (MDL), the seven segment display is arranged to show the digit 0, indicating that the tank is empty, when the water reaches level1 (but is below level2) the connection between the probes gets completed (through the conducting medium – water) and the base voltage of transistor increases.
This causes the base-emitter junction of transistor to get forward biased, this switches transistor from cut-off to conduction mode thus PIN (B7) of microcontroller is pulled to ground hence, the corresponding digit displayed by the seven segment display is 1.
The similar mechanism applies to the detection of all the other levels. When the tank is full, all input pins of microcontroller become low. This causes the display to show 8 and also in this case a buzzer sound is given, thereby indicating a “tank full” condition.
Most water level indicators are equipped to indicate and detect only a single level. The Water Level Indicator implemented here can indicate up to nine such levels and the microcontroller displays the level number on a seven segment display.
So, the circuit not only capable of cautioning a person that the water tank has been filled up to certain level, but also indicates that the water level has fallen below the minimum detectable level. This circuit is important in appliances such as the water cooler where there is a danger of motor-burnout when there is no water in the radiator used up also it can be used in fuel level indication.

## Components used
ATMEGA8 microcontroller 
A constant 5v power supply is given to the microcontroller and rest of the circuit from a battery.
The tank has 9 conductive type sensors (other types of sensors have been mentioned earlier but in our project only conductive type are used) embedded into it and 8 wires of sensors out of 9 are connected to transistors and the 9th is connected to 5v+ supply.
The use of transistor is it acts as inverter (i.e. in on state gives low voltage at output and in non conducting state gives high voltage at its output), all transistors outputs are connected to PORTB of microcontroller.
Seven segment display is connected to PORTD. It is connected in common cathode fashion.
The Output for the 7th level is not only shown on seven segment display but also indicated with a discontinuous buzzer sound.
Output for the 8th level (i.e. tank full condition) is not only shown in seven segment display but also indicated with a continuous buzzer sound.
## Software used

SimulIDE

GCC Compiler for AVR

Vs code

## Features
Easy installation.
Low maintenance.
Compact elegant design.
The Automatic water level controller ensures no overflows or dry running of pump there by saves electricity and water.
Avoid seepage of roofs and walls due to overflowing tanks.
Fully automatic, saves man power.
Consume very little energy, ideal for continuous operation.
Automatic water level controller provides you the flexibility to decide for yourself the water levels for operations of pump set.
Shows clear indication of water levels in the overhead tank.

## SWOT - Strengths, Weakness, Opportunities and Threats

### Strengths

Compact elegant design

Shows clear indication of water levels in the overhead tank

Easily accessible by the any person

High efficiency

### Weakness

This system can be used at low to moderate temperature.

### Opportunities

This system can be expanded by adding few more features depending on the user requirement. 

### Threats

This system cannot be used for very high water levels.

## 4W's and 1H

*What* - Water level indicator in tanks

*Where* - Usefull in almost all of the houses

*When* -  When the waterpump is ON/OFF

*Why* - To Indicate the water level in the tanks

*How* - By using sensors &Transistors


## Detail Requirements

### High Level Requirements


| **ID** | **Description** |
| :- | :- |
|HLR1|Microcontroller unit    |
|HLR2|Sounder for audio out|
|HLR3|9 conductive type sensors|
|HLR4|Transistor|
|HLR5|7 segment LED|

### Low Level Requirements


| **ID** | **Description** | **HLR ID** |
| :- | :- | :- |
|LLR1|ATMEGA328|HLR1|
|LLR2|Buzzer|HLR3|
|LLR3|inverter|HLR4|
|LLR4|LED|HLR5|
