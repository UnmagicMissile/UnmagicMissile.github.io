---
layout: post
title: Rocketry Guidance Navigation and Controls
description: Development of a fin tab controlled, low power rocket based on ESP32 micro controller.
skills: 
- FDM
- ESP32
- Soldering
- Perfboarding
- Breadboarding
- Embedded C
- Sensor Fusion
- CFD
main-image: /project.webp 
---

---
# Hardware and Software
## Hardware
This flight computer is based on an ESP 32D and uses an BNO080 for inertial measurement, a BMP 390 for barometric altitude measurement, and two step data collection with an SMT SD chip and a micro SD breakout board. Components are found on breakout boards and development boards supplied by vendors then mounted to a custom PCB.
### PCB Designed in KiCad
{% include image-gallery.html images="BelleV1PCB.jpg" height="400" %}
## Software
The current control script is written in embedded C. The system uses state machine logic to enter new states in the process (e.g. idle, powered flight, unpowered flight, landing, etc.) Each state will collect data from the hardware to predict where the rocket is, where the rocket will be, and what the rocket needs to move in order to move in the right direction. Data is sent to an SMT mounted SD card from idle through landing then to the removable SD card once the rocket is in a stable environment. Sending data directly to a removable chip has high risk of data corruption due to the mechanical connectors of the SD slot having the ability to lose contact under moderate G loading found during a nominal landing.
# Physical System
## CAD Model
