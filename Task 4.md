# Task 4
# Project Title:
## 7 Segment Display Counter

## Overview
The aim of this project is to create a digital counter that increments every time a push button is pressed. The count will be displayed on a 7-segment LED display. The project uses the VSD Squadron Mini microcontroller to read the button input and drive the display output.

## What is Counter:
A counter is an electronic device or a digital circuit that counts the number of occurrences of a specific event or signal. It is commonly used in various applications, such as digital clocks, frequency counters, event counters, and in various control systems. Counters can be implemented using hardware components (e.g., flip-flops, logic gates) or using software in microcontrollers and microprocessors.

## Components Required
- VSD Squadron Mini Microcontroller Board
- Push Button
- 7-Segment LED Display (Common Cathode or Anode)
- Resistors (10kΩ for pull-up resistor, 220Ω for current limiting resistors)
- Breadboard or PCB
- Connecting Wires
- Power Supply (USB or battery)

## Pin Connection
###Push Button:
One terminal of the push button connected to Digital Pin D2.
Other terminal connected to GND.
A pull-up resistor (10kΩ) connected between D2 and VCC.

###7-Segment Display:
Segment a connected to Digital Pin D3.
Segment b connected to Digital Pin D4.
Segment c connected to Digital Pin D5.
Segment d connected to Digital Pin D6.
Segment e connected to Digital Pin D7.
Segment f connected to Digital Pin D8.
Segment g connected to Digital Pin D9.
Common cathode or anode connected to GND or VCC (depending on display type).

###Power Supply:
VCC pin connected to a 3.3V or 5V power source.
GND pin connected to the ground of the power source.

