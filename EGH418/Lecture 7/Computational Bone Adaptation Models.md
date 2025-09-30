Computational models are used to simulate [[Bone Modelling and Remodelling]] over time, predicting how bone density and geometry will change in response to mechanical loading. These models are often implemented using Finite Element Analysis (FEA).

## The Core Algorithm
Most adaptation models are iterative and follow a similar logic based on [[Wolff's Law and Mechanostat Theory]].

> The model simulates a feedback loop where the local mechanical stimulus directs changes in bone properties, which in turn alters the subsequent mechanical stimulus.

The typical simulation steps are:
1.  **Define Initial State**: Start with an initial bone geometry and density distribution at time $t=0$.
2.  **Apply Loads**: Apply realistic loads to the FE model (e.g., from an [[Inverse Dynamics in 3D]] simulation).
3.  **Calculate Stimulus**: Solve the FE model for the stress/strain field and use it to calculate the [[Mechanical Stimulus for Bone Adaptation]] ($\psi$) at every point in the bone.
4.  **Compare to Target**: Compare the calculated stimulus $\psi$ to a target or "attractor state" stimulus ($\psi_{AS}$). This target represents the physiological or homeostatic loading zone.
5.  **Adapt Bone**: Use a rate law to change the local bone density.
    - If $\psi > \psi_{AS}$ (overload), add bone density (formation).
    - If $\psi < \psi_{AS}$ (disuse), remove bone density (resorption).
    - If $\psi \approx \psi_{AS}$ ("lazy zone"), make no change.
6.  **Update and Repeat**: Update the material properties of the FE model based on the new density distribution. Advance the time step ($t = t + \Delta t$) and repeat from step 2 until an equilibrium state is reached.

![[Screenshot 2025-09-30 at 12.02.07 pm.png|300]]
*Image Reference: From bone_adaptation-1.pdf, Page 41.*

This approach has been used to successfully simulate bone development during growth, changes in density around orthopaedic implants (stress shielding), and the effects of exercise or disuse.