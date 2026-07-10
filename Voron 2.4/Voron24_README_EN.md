# Voron 2.4 "Pinky" — CoreXY 3D Printer Build & 4-Motor Upgrade

Personal independent project · Built from the open-source [Voron](https://vorondesign.com) design

![Pinky's full view](Pinky%27s%20full%20view.jpg)
*"Pinky" — full view*

## Overview

Everything from sourcing raw materials, frame assembly, wiring, component selection, CAN bus configuration, firmware setup, motion tuning, to input-shaping/resonance compensation was done independently.

![Bare Al frame](Bare%20Al%20frame.jpg)
*Aluminium extrusion frame build*

## Electronics

![Electronics bay view](Electronics%20bay%20view.jpg)
*Electronics bay layout*

![Electronics layout](Electronics%20layout.jpg)
*Wiring layout*

## All-Wheel-Drive Upgrade

Standard CoreXY uses two stepper motors to drive the X/Y axes. I upgraded this to a four-motor ("all-wheel-drive") configuration, raising print speed to **650mm/s** and travel speed to **1000mm/s**. On acceleration: **45000mm/s² is the stable, reliably-running value**; pushing to 55000mm/s² in testing would still run, but starts showing the missed-step issue described below, so 45000mm/s² is the production-grade setting.

Driver-wise, the setup started as TMC2209 + TMC2240, and was later upgraded to TMC5160 high-voltage drivers for better stability at high acceleration.

**Demo videos:**
- [45000mms^2 acceleration.mp4](45000mms%5E2%20acceleration.mp4) — acceleration test
- [12 min benchy.mp4](12%20min%20benchy.mp4) — printing the standard Benchy test model in 12 minutes
- [Infinite printers.mp4](Infinite%20printers.mp4) — continuous printing test

## Custom MCU & Motor Driver Mount

Designed a custom mount for the MCU and motor drivers to improve wire routing and cooling:

![MCU and Motor driver stand drawing](MCU%20and%20Motor%20driver%20stand%20drawing.png)
*Engineering drawing*

![MCU and Motor driver stand CAD](MCU%20and%20Motor%20driver%20stand%20CAD.jpg)
*CAD model*

![MCU and Motor driver stand](MCU%20and%20Motor%20driver%20stand%20.jpg)
*Physical mount*

![MCU and Motor driver stand with cooling fans](MCU%20and%20Motor%20driver%20stand%20with%20cooling%20fans.jpg)
*Mount with cooling fans added*

## Technical Issues & Diagnosis

**Issue 1: Electrostatic buildup causing driver errors**
Occasional static buildup during operation caused the stepper drivers (TMC2240 at the time) to fault and halt.

**Issue 2: Crosstalk on the mainboard at high acceleration causing missed steps**
The STM32 mainboard used showed high-frequency signal crosstalk at higher acceleration settings, causing missed steps — this is also why the production acceleration setting was locked at 45000mm/s² rather than the 55000mm/s² tested ceiling.

For both issues, I independently compiled a full technical report and sent it to the mainboard manufacturer to get the issues confirmed and followed up on.

## My Role

Independently handled the entire process from frame build, electronics design, and firmware configuration through to fault diagnosis — including the all-wheel-drive upgrade design, the custom mount design, and diagnosing/reporting the mainboard's high-frequency signal issue to the manufacturer.
