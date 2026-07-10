# MMAN4200 Phone Stabiliser (Flexure-Hinge Gimbal)

UNSW Additive Manufacturing Design course (MMAN4200) group project

**Team:** David Dai, Zhanxin Ye, Jia Bei (Belinda) Wong, Junyi Wang, Chenyi Zhang (Jason Tomczyk)

![CAD Exploded View](00_cad_render.jpg)

## The Problem

Course brief: design a 3D-printable mechanical component. We chose a phone stabiliser — existing solutions are either bulky/expensive tripods or motorised gimbals starting at tens of AUD (e.g. DJI OSMO Mobile SE), leaving casual users without a cheap way to get stable handheld footage.

![The Problem](01_problem.jpg)

## Our Solution

The core idea: replace conventional bearings/joints with a **3D-printed flexure structure**, printed as a single monolithic part:

- No bearing assembly or extra hardware, which removes the mechanical play that causes "wobble"
- The flexure's inherent elasticity adapts to different phone weights/sizes
- Fully 3D-printed — cheap and lightweight

![Our Solution](02_solution.jpg)

## Design Task

The component to design was a gimbal, required to:
- Use flexures to provide pitch/roll rotation
- Stay simple and compact enough to print in one piece on a desktop printer

![The Product](03_product_task.jpg)

## Working Process

I proposed and led this project:

1. Researched existing 3D-printable flexure joint designs
2. Discussed with the team and settled on **3 degrees of freedom** — just enough for handheld anti-shake, no more
3. Once the overall direction was set, split the work: the phone-mount bracket (Bell, Zhanxin) and the bottom handle (Junyi) were left to teammates to model freely; for the central rotating flexure hinge, I specified the spline thickness/height and screw-hole positions, and David did the detailed modelling
4. Integrated everyone's parts into the final CAD model

![Working Process](04_working_process.jpg)

## Design Validation & Iteration

**Spline height** sets the flexure's spring constant. I independently ran the FEA and printed multiple test samples (8mm / 10mm / 12mm) to validate the simulation — 12mm was too stiff, 8mm too weak, and 10mm was the balance point. I then handed those dimensions to David to model that part in detail.

![Testing - Spline Height](05_testing_spline_height.jpg)

Further stress/strain simulation identified the high-stress concentration region on the flexure, which directly informed the print-preparation work that followed.

![Testing - Stress & Strain](06_testing_stress_strain.jpg)

## Print Preparation

I handled the DFM (design-for-additive-manufacturing) optimisation and slicer setup for every part:

- **Bridging for heat-set insert holes**: the part needed heat-set inserts on both sides, but the printer can't reliably print a perimeter mid-air, so a bridge support structure was added to solve the overhang
- **Seam painting**: the slicer's default seam position could land on a mechanically weak spot, so I manually moved it to a lower-stress area

(The PDF only shows a subset of these considerations — the actual DFM and slicer tuning went further than what's presented there.)

![Preparation - Insert Bridge](07_preparation_insert_bridge.jpg)
![Preparation - Seam Painting](08_preparation_seam_painting.jpg)

## Final Build

![Completed Assembly](Completed%20Assembly.jpg)
*Fully assembled unit*

![With phone](With%20phone.jpg)
![With phone 2](With%20phone%202.jpg)
*Tested with an actual phone mounted*

## My Role

- Proposed this project and led the team's task allocation
- Independently ran FEA and iterative print testing on key dimensions (e.g. spline height) to validate and lock in the final design parameters
- Specified thickness, height, and screw-hole requirements for the central rotating flexure hinge; David did the detailed modelling of that part
- Independently handled DFM optimisation and slicer setup (bridge supports, seam placement, etc.) for every part
- The final report was written up by teammates; I reviewed technical terminology and steered overall direction
