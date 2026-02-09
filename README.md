# Antenna Tracker ESP32

## Overview
This project is a **PCB-based antenna tracker** originally developed as a recruitment project for the **Rocket Experiment Division (RED)** at Instituto Superior Técnico. 

The system is designed to track a flying rocket in real time and orient an antenna towards it, minimizing telemetry loss during launches and flight operations. Tracking is achieved by computing the relative azimuth and elevation angles between the ground station and the rocket, and actuating two servo motors accordingly.

## System Architecture
1 - The rocket transmits its position to the ground station
2 - The tracker’s local GPS module provides its own position
3 - The ESP32 computes Azimuth amd Elevation and converts these angles into PWM signals
4 - The two servo motors rotate the antenna to maintain alignment with the rocket

## Hardware Specifications

### Core Components
- **Microcontroller**: ESP32-C3 SoC (Wi-Fi / Bluetooth capable)
- **GPS Module**: u-blox NEO-M9N-00B
- **Actuators**: 2 × High-torque servo motors (azimuth & elevation)
- **RF Receiver**: RFD868x (or compatible)
- **Power**: 2S Li-ion battery (7.4 V)
- On-board 5 V and 3.3 V regulation

### PCB
- Designed in KiCad
- Dimensions: 76 × 56 mm
- All components placed on the top layer

## Current Status
- **Hardware design**: Completed
- **PCB layout**: Ongoing improvements and minor revisions
- **Firmware**: In development
- **Assembly & testing**: Pending

## Future Improvements
- Improved PCB routing 
- Redundant antenna configurations (directional + omnidirectional)
- MAVLink integration
