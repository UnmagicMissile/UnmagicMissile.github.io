---
layout: post
title: Turbopump Project
description: Development of a 3 inch diameter pump
skills: 
- FDM
- Arduino
- Pump Design
- Onshape
main-image: /PumpPrinted.jpg
---

---
# Intro
Inspired by another hobby rocketeer, I started this project to gain more understanding of turbopumps and produce my first prototype.
### Cross Section of the Turbopump
{% include image-gallery.html images="PumpCrossSec.jpg" height="400" %}
# Impeller Design and Analysis
Targeting a pressure rise of 500 psi, a flow rate of 30 GPM, and an operation speed of 30,000 RPM, I started to roughly shape the overall dimenions of the impeller to try to acheive my goals. Iteratively drafting my basic dimentions and performing hand calculations for velocity triangles got me a pressure rise of about 501 PSI. 

The resulting impeller from hand calculations shown below:
{% include image-gallery.html images="Impeller180Sec.jpg" height="400" %}
# Volute Section
Using Bernoulli's equation and the velocities expected at the exit of the impeller and the housing, the calculated pressure delta across the housing is -0.94 PSI. Bringing the total system pressure to just over 500 PSI.
{% include image-gallery.html images="Impeller1VoluteCrossSec.jpg" height="400" %}
# Testing
Flowrate testing was done by the timing of emptying and refilling a 2 gallon bucket multiple times and averaging the flowrate. A flowrate of 26.5 Gallons per minute was found. Attempts to record pressure rise at the outlet were unseccesful. Nearly 0 pressure rise was found at multiple valve positions and only about 1 PSI of pressure rise occured at the fully closed and 90% closed position.
# Results
Basic fit and low RPM testing using a 3D printed shaft revealed the shaft seal was melting to the PETG. After replacing those seals and using a metal shaft that seals were still deteriorating significantly. This is likely due to the high RPM.
