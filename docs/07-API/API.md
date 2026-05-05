---
title: Human Machine Interface API
tags:
- tag1
- tag2
---

## Overview

The Human Machine Interface subsystem is using a ESP32 running MicroPython, paired with an OLED display. It is intended to be used to send commands to the Motor subsystem, and receive sensor readings from the Hall Effect subsystem. 

The subsystem relays all information passed through on the OLED display for debugging purposes. It follows the required message protocols defined by our team, using the correct team ID, sender ID, and receiver ID. 

Below are all the messages intended to be used by the time the project was due. Due to the final state of our project, we were not able to have very many.


| Message Type | Full Message Format | Payload Description | Byte Count | Purpose |
|--------------|----------------------|---------------------|------------|---------|
| Sensor Data | AZTCvalueYB | value is the reading from the sensor as a string | 2 bytes for AZ + 2 bytes for TC + N bytes for value + 2 bytes for YB | Receives the most recent sensor reading |
| Data Request | AZTCREQYB | REQ indicates a request for sensor data | 2 bytes for AZ + 2 bytes for TC + 3 bytes for REQ + 2 bytes for YB | Requests the current Hall effect sensor reading |
| Motor Command | AZCKgoYB | go indicates a request for motor action | 2 bytes for AZ + 2 bytes for CK + 2 bytes for go + 2 bytes for YB | Tells the motor when to go |
| Motor Stop | AZCKstopYB | stop indicates a request to stop the motor | 2 bytes for AZ + 2 bytes for CK + 4 bytes for stop + 2 bytes for YB | Tells the motor when to stop |

This API makes sure that the Human Machine Interface subsystem can communicate properly with the motor module, the wireless module, and the sensor module. This API reflects the final functionality of the subsytem.