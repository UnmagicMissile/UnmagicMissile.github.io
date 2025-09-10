---
layout: post
title: Aerosol Jet Printing Research
description: Redesigned aersol jet printing atomizers and particle density counter for research lab at Iowa State University
skills: 
- Product Prototyping
- Soldering
- Electronics Prototyping
- Python
- Solidworks
- 4 axis CNC
- MasterCAM
main-image: /
---

---
# Atomizers
## Ultrasonic Atomizer Redesign
Early revisions of the ultrasonic atomizer are SLA 3D printed from Formlabs clear resin. These atomizers work well, but degrade over time and do not withstand some of the harsh print media being used. Additionally, ultrasonic atomization generates a fair amount of heat and can create spikes in particle generation. Aluminum was used for the redesign and prototypes. It has high thermal conductivity allowing for quick heat disipation and it is non reactive with a majority of the media used in the lab. Additionally, I had easy and imediate access to copious amounts of aluminum for low cost.

As testing occured, the aluminum was found to be too thermally conductive. However, this opened up the possibilty to beter control media temperature and associate temperature to deposition rates.

## Particle Counter Redesign
The particle counter, also known as the optic cell, is used to track particle density within the carrier flow stream. This is done by letting a laser's beam scatter off the particulate in the flow and into one of two photodiodes. Depending on the media density in the carrier flow, the photodiodes will read different amounts of light and thus allow the user to guage how much media they are dispensing onto their print surface.

The planar tolerance between the laser mount and the photodiode mounts is critical to signal clarity. Poor planar tolerance leads to more reflections in the cavity, leading to the baseline light detected being higher than intended. To remedy this, the choice to manually machine the part was avoided to remove human error. This choice led to the use of 4th axis machining.


