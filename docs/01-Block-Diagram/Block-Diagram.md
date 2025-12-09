---
title: Individal Block Diagram
tags:
- tag1
- tag2
---

## Overview

This block diagram shows the light sensor subsystem and how it will connect to the teams system. The 5V regulated power supply will provide power to the op-amps aswell as the light sensor itself. A signal from the photodiode will be amplified by an op-amp, and then ran through the microcontrollers ADC to then be manipulated on the software side, before being sent back as an analog signal through the DAC to be read by the lighting subsytem.

## Block Diagram 
![Indivial Block diagram ](<Individual Block Diagram.png>)

## Explanation

The photodiode will read light intensity of the room and generate a current based on how bright it is. This current goes into an op-amp, and is amplified into a 0-5V signal. This signal can then be read and used to turn on or off a grow light based on a plants needs, fullfilling the product requirements.

Photodiode Light Sensor Block Diagram | [PDF Download](<Individual Block Diagram.pdf>)