---
layout: post
title: Turbopump Project
description: Development of a 4 inch diameter turbopump
skills: 
- FDM
- Arduino
- Pump Design
- Onshape
main-image: /PumpPrinted.jpg
---

---
# Intro
Inspired by another hobby rocketeer, I started this project to gain more understanding of turbopumps and produce my first prototype. Reddit user akarin9527 made a turbopump and pumped liquid oxygen to a small rocket engine. 
### Cross Section of the Turbopump
{% include image-gallery.html images="PumpCrossSec.jpg" height="400" %}
# Impeller Design and Analysis
Targeting a pressure rise of 500 psi, a flow rate of 30 GPM, and an operation speed of 20,000 RPM, I started to roughly shape the overall dimenions of the impeller to try to acheive my goals. Iteratively drafting my basic dimentions and performing hand calculations for velocity triangles got me a pressure rise of about 501 PSI. 

The resulting impeller from hand calculations shown below:
{% include image-gallery.html images="Impeller180Sec.jpg" height="400" %}
# Volute Section
Using Bernoulli's equation and the velocities expected at the exit of the impeller and the housing, the calculated pressure delta across the housing is -0.94 PSI. Bringing the total system pressure to just over 500 PSI.
{% include image-gallery.html images="Impeller1VoluteCrossSec.jpg" height="400" %}
# Testing
Pressure vs RPM data was collected for various flowrates to create a pump curve.

# Results
Basic fit and low RPM testing using a 3D printed shaft revealed the shaft seal was melting to the PETG. After replacing those seals and using a metal shaft that the seals were still melting. This is likely due to the high RPM. More research is needed to find how high RPM systems are sealed.

Although post test inspections reveal no signs of wear on the impeller, it is suspectedd that the high speed is casuing cavitation. More run time may be needed to see noticable effects.
