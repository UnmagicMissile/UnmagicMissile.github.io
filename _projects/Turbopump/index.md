---
layout: post
title: Turbopump Project
description: Development of a 4 inch diameter turbopump
skills: 
- FDM
- Arduino
- Pump Design
- Onshape
main-image: 
---

---
# Intro
Inspired by another hobby rocketeer, I started this project to gain more understanding of turbopumps and produce my first prototype. Reddit user akarin9527 made a turbopump and pumped liquid oxygen to a small rocket engine. 
### Cross section of the turbopump
{% include image-gallery.html images="" height="400" %}
# Impeller Design and Analysis
I started by looking at a specifc speed chart for impellers to get a rough idea of where I wanted to perform. I selected a specific speed of about 750, targeting a pressure rise of 550 psi and an operation speed of 30,000 RPM (a similar design RPM to akarin9527.) This leaves me at about 35 gallons per minute for volumetric flowrate.

After looking at pumps similar to my design point, I created my 3D model and approximated the blade geometry and angles. I then hand calculated the speed
### PCB Designed in KiCad
{% include image-gallery.html images="BelleV1PCB.jpg" height="400" %}
## Software
The control script is written in embedded C. The system uses state machine logic to enter new states in the process (e.g. idle, powered flight, unpowered flight, landing, etc.) Each collects data from the hardware to predict where the rocket is, where the rocket will be, and what the rocket needs to move in order to move in the right direction. Data is sent to an SMT mounted SD card from idle through landing then to the removable SD card once the rocket is in a stable environment, preventing data corruption risk commonly associated with removable SD cards due to vibration.
