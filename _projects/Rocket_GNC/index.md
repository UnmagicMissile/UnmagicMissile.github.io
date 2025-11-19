---
layout: post
title: Rocketry Guidance Navigation and Controls
description: Development of a fin tab controlled, low power rocket based on ESP32 micro controller.
skills: 
- FDM
- ESP32
- Arduino
- Soldering
- Electronics Prototyping
- CFD
- PCB Design
- Onshape
main-image: /TwistCAD.jpg 
---

---
# Physical System
The rocket's aerostructures are almost entirely FDM 3D printed. The nosecone holds the parchute ejection hardware. The fin can holds the guidance and control systems. The parachute is held in the main body tube, and is tied into the fin can coupler.
### Cross section of the fin can with servos and fin tabs
{% include image-gallery.html images="GNC_FinCan.jpg" height="400" %}
# Hardware and Software
## Hardware
The Belle flight computer is based on an ESP 32D and uses an BNO080 for inertial measurement, a BMP 390 for barometric altitude measurement, and two step data collection with an SMT SD chip and a micro SD breakout board. The data that is collected is processed and the microcontroller sends position commands to a servo controller. The breakout boards and development boards are mounted to a custom PCB. The parchute ejection is handled by an RRC3+ to separate tasks, keeping the flight critical functions to a COTS option.
### PCB in KiCAD and after Soldering
{% include image-gallery.html images="BelleV1PCB.jpg" height="400" %}
{% include image-gallery.html images="LiveMasSolder" height="400" %}
## Software
The control script is written in arduino language. The system uses state machine logic to enter new states in the process (e.g. idle, powered flight, unpowered flight, landing, etc.) Each collects data from the hardware to predict where the rocket is, where the rocket will be, and what the rocket needs to move in order to move in the right direction. Data is sent to an SMT mounted SD card from idle through landing then to the removable SD card once the rocket is in a stable environment, preventing data corruption risk commonly associated with removable SD cards due to vibration.
