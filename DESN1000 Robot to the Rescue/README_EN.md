# DESN1000 Search-and-Rescue Tracked Robot "Wall-F"

UNSW first-year "Industrial Design & Manufacturing" course (DESN1000) group project · **Ranked #1 in year cohort**

## Brief

Design a rescue robot that can traverse simulated disaster terrain, map the terrain via ultrasonic radar, and grab "survivors" (tennis balls).

## My Role

CAD design, manufacturing, hardware iteration, software architecture and testing.

## Design Journey — Version 1.0

Started from concept sketches to settle on a tracked-drive chassis:

![Concept drawing](Concept%20drawing.jpg)
*Concept sketch*

![Tank drive design of version 1.0](Tank%20drive%20design%20of%20version%201_0.jpg)
*V1.0 tank-drive mechanism design*

**The biggest cost innovation**: instead of buying off-the-shelf rubber tracks (expensive, and the course budget was tight), we laser-cut nylon fabric as track links and hand-sewed 3D-printed track plates together with clear fishing line — bringing the entire track system in **under AUD 5**, the lowest-cost tracked solution in the course's history.

![Sewing together the tank tracks](Sewing%20together%20the%20tank%20tracks.jpg)
*Sewing 3D-printed track plates with fishing line*

![Still sewing tank tracks](Still%20sewing%20tank%20tracks.jpg)
*Track-sewing in progress*

![Tank tread prototype](Tank%20tread%20prototype.jpg)
*Track plate prototype*

![Tank tread tensioning system prototype](Tank%20tread%20tensioning%20system%20prototype.jpg)
*Track tensioning system prototype*

![Tank tracks complete](Tank%20tracks%20complete.jpg)
*Completed track assembly*

![Tank drive components](Tank%20drive%20components.jpg)
*Tank drive components*

![Version 1.0 chassis](Version%201_0%20chasis.jpg)
*V1.0 chassis*

![Version 1.0 complete](Version%201_0.jpg)
*V1.0 complete*

**Demo video:** [Design montage of version 1.0.mp4](Design%20montage%20of%20version%201_0.mp4)

## Sensing & Software Architecture

The whole robot was designed to be highly modular for fast iteration and re-purposing. Software was split across three layers:

- **Onboard Arduino**: logs ultrasonic radar and IMU data, relays it to a laptop over Bluetooth; drives the gripper to grab "survivor" tennis balls; controls motor steering on both sides
- **Onboard ESP32 camera**: streams live video over WiFi
- **Laptop**: reconstructs the terrain map from the Bluetooth-relayed radar/angle data, auto-generates a path, and sends drive commands back to the Arduino; also receives the WiFi video feed

![IR capture logic 1](IR%20capture%20logic%201.jpg)
![IR capture logic 2](IR%20capture%20logic%202.jpg)
![IR capture logic 3](IR%20capture%20logic%203.jpg)
*IR/grabbing logic design*

![Front assembly prototype](Front%20assembly%20prototype.jpg)
*Front gripper assembly prototype*

![Omni adaptor panel](Omni%20adaptor%20pannel.jpg)
*Omni-wheel adaptor panel*

## Design Journey — Version 2.0 "Wall-F"

Iterated on V1.0 into a more structurally complete V2.0:

![Version 2.0 CAD prototyping](Version%202_0%20CAD%20prototyping.jpg)
*V2.0 CAD prototyping*

![Version 2.0 CAD complete](Version%202_0%20CAD%20complete.jpg)
*V2.0 complete CAD model*

![Version 2.0 chassis complete](Version%202_0%20Chasis%20complete.jpg)
*V2.0 chassis complete*

![Wall-F Version 2.0](Wall-F%20Version%202.0.jpg)
![Wall-F Version 2.0 closeup](Wall-F%20Version%202.0%20closeup.jpg)
![Wall-F Version 2.0 is live](Wall-F%20Version%202.0%20is%20live.jpg)
*Wall-F V2.0 — full view and details*

**Demo video:** [She moves!!!!.mp4](She%20moves!!!!.mp4)
