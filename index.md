---
layout: project
title: usc-auv-batteries
subtitle: A lithium-polymer battery power distribution and charging system for an AUV with 6 underwater thrusters.
---

<img src="http://niftyhedgehog.com/usc-auv-batteries/images/battery_pack.jpg">

## Overview
This AUV is quite massive. In order to move smoothly and quickly through the water, it's six thrusters must have sufficient propulsion strength (high current draw). The AUV also contains a full embedded computer system and a variety of sensors and actuators, which all require a power source. And being "autonomous", it must run untethered to an external power supply. Thus, a hefty battery system is required to ensure sufficient operation and an extended runtime.

## Hardware
Lithium-polymer batteries were selected because of their superior energy density, allowing the most runtime with minimal size and weight. The AUV used two battery packs in parallel orientation to increase capacity (10 Ah). During periods of light usage, it could achieve up to an hour of runtime. 

<img src="http://niftyhedgehog.com/usc-auv-batteries/images/assembled_packs.jpg">

Each battery pack consisted of 6 high-discharge LiPo cells connected in series to generate the ~24V input to the power distribution board. The battery pack featured an on-board voltage monitoring and Coulomb-counting circuit to indicate the state of charge. High-power Molex connectors were used to ensure power integrity and robust connections during charging and discharging.

<img src="http://niftyhedgehog.com/usc-auv-batteries/images/lipo_cells.jpg">

It is extremely important to care for and maintain LiPo batteries. The cells should never be over-charged or over-discharged. When unused for an extended period of time, the batteries should not be stored at full capacity. Failing to care for these battery packs can result in poor performance, "bloating", or inflammation/explosion.

## Software
The Coulomb-counting state of charge information can be sent to the host processor to warn the user when battery levels are low. The information can also be used to create a power profile to understand power management and current consumption.
