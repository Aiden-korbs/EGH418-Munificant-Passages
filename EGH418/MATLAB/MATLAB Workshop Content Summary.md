## Week 2 – Introduction to MATLAB & Gait Analysis

- Developed **healthy MATLAB habits**: clearing workspace (`clear all`, `clc`, `close all`), using comments/sections, consistent variable naming.
- Learned to **import gait data** (WinterData.csv) and use functions like `xlsread`/`csvread`.
- Focused on **data normalisation** (expressing gait as % of stride instead of raw time).
- Practised **plot customisation**: titles, axis labels, legends, and `yyaxis` for dual axes.
- Objective: Reproduce plots showing ankle position vs. ground reaction force across a gait cycle.

---

## Week 3 – Investigating Limb Angles

- Focus: **Debugging code** (syntax, runtime, logic errors).
- Applied trigonometry to calculate **limb angles** (shank & thigh) and then **knee joint angles**.
- Debugged scripts that gave discontinuous angle plots (artefacts of `atan`).
- Practised **normalisation & plotting** of knee angle over the gait cycle to identify patterns vs. ground reaction force.

---

## Week 4 – Method of Finite Differences

- Introduced **functions** in MATLAB to reduce repetitive code (inputs/outputs, saving as `.m` files).
- Used **finite difference equations** to compute time derivatives of limb angles:
    - Angular velocity
    - Angular acceleration
- Importance: angular acceleration links to **muscle moments** and gait abnormalities.
- Practised **plotting with subplots**: comparing angle, velocity, acceleration in separate but related graphs.

---

## Week 6 – Uncertainty in Marker Positioning

- Topic: **Uncertainties of skin-mounted markers** in motion capture (palpation variability, skin motion artefacts, system error).
- Used **Winter Data** again, this time perturbing marker positions based on published inter-operator error values.
- Step-by-step tasks:
    1. Calculate **local segment axes** (e.g., thigh coordinate system).
    2. Perturb marker positions to **maximise/minimise joint angles**.
    3. Apply process to hip/knee, ankle, and foot markers.
    4. Export perturbed trajectories and re-use in earlier scripts to compute **uncertainty bounds for joint angles and moments**.

---
## Week 8 – Composite Beam Theory & Plate Fixation

This workshop applied composite beam theory to analyse the mechanics of a bone-plate system used in fracture fixation.
### Key Concepts & Skills
- **Parametric Analysis**: Used MATLAB to run a parametric study by varying plate stiffness (`E_p`) and bone diameter (`D_o`).
    
- **Composite Beam Calculations**: Implemented equations to find the **neutral axis** location and the overall **bending stiffness** of the composite system.
    
- **Data Visualisation**: Created plots to visualise how changes in material properties and geometry affect the system's mechanics.
    
- **Stress Shielding Analysis**: Plotted the resulting **stress and strain distributions** to understand and quantify the concept of stress shielding.

---

## Week 10 – Shoulder Stability Analysis

This workshop used MATLAB to visualise glenohumeral joint forces and assess joint stability using the "stability cone" concept.
### Key Concepts & Skills
- **3D Plotting**: Used advanced plotting functions like `plot3`, `surf`, and `quiver3` to create 3D visualisations.
    
- **Data Handling**: Imported and plotted multiple components of **bone-on-bone force** data against the arm's elevation angle.
    
- **Geometric Modelling**: Implemented the parametric equation of an ellipsoidal cone to model the **stability cone** of the glenoid.
    
- **Biomechanical Assessment**: Assessed joint stability by determining if the calculated joint reaction force vector remained inside the stability cone throughout the abduction motion.