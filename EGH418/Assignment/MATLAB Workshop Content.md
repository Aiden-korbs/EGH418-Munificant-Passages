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