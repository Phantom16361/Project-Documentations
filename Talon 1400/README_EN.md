# Talon 1400 Fixed-Wing UAV

Personal independent project · Built from the open-source [Flightory Talon 1400](https://flightory.com/product/talon-1400) fixed-wing kit

## Overview

The entire fuselage is 3D-printed in foam material, fitted with a SpeedyBee flight controller and a WalkSnail digital FPV system + camera.

![3D CAD exploded view](3D%20CAD%20exploded%20view.png)
*Fuselage CAD exploded view*

## Build Process

![Fuselage in progress](Fuselage%20in%20progress.jpg)
*Fuselage printing/assembly*

![Fuselage complete](Fuselage%20complete.jpg)
*Fuselage complete*

![Adding some color schemes](Adding%20some%20color%20schemes.jpg)
*Paint scheme*

![Paintjob complete](Paintjob%20complete.jpg)
*Paintjob complete*

![Front assembly](Front%20assembly.jpg)
![Front assembly complete](Front%20assembly%20complete.jpg)
*Nose assembly*

## Avionics

Fitted with a SpeedyBee flight controller plus a WalkSnail digital FPV system and camera:

![Setting up flight controls](Setting%20up%20flight%20controls.jpg)
*Flight controller setup*

**Video:** [Camera mount ready.mp4](Camera%20mount%20ready.mp4) — camera mount installed

## Maiden Flight & Failure Analysis

![Ready for takeoff!](Ready%20for%20takeoff!.jpg)
*Ready for takeoff*

**Video:** [Waaay too much power.mp4](Waaay%20too%20much%20power.mp4) — powertrain test, throttle set too high

**Video:** [Liftoff!!! Crashes immediately.mp4](Liftoff!!!%20Crashes%20immediately.mp4) — crashed immediately on the maiden flight

![Unfortunate ending](Unfortunate%20ending.jpg)
*Post-crash fuselage*

**Root cause:** The crash was caused by excessive throttle applied at takeoff, producing a torque spike high enough that the 3D-printed material at the affected joint failed under the resulting shear stress.

**Fix:** Pre-set a throttle ramp-up curve before takeoff to avoid torque spikes, and locally increased infill density at the stress-concentrated area to improve shear strength there.

## My Role

Independently handled the fuselage's 3D-printing design and build, avionics installation and setup, and flight testing. After the crash, independently carried out the failure analysis (linking torque to shear failure) and proposed the two-part fix: throttle-curve limiting plus localised infill reinforcement.
