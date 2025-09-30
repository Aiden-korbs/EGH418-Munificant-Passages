## Principal Stresses
For any stress state, no matter how complex, there is always a special orientation where all **shear stresses are zero**. The normal stresses acting on these planes are the **principal stresses**, denoted $\sigma_1, \sigma_2,$ and $\sigma_3$.

> **Principal Stresses** are the **eigenvalues** of the [[The Stress Concept and Cauchy's Tensor|stress tensor]] matrix. They represent the maximum and minimum normal stresses at that point.

The stress tensor in the principal orientation is a simple diagonal matrix:
$$ \sigma_{principal} = \begin{bmatrix} \sigma_1 & 0 & 0 \\ 0 & \sigma_2 & 0 \\ 0 & 0 & \sigma_3 \end{bmatrix} $$

---

## Stress Invariants
Certain combinations of stress components, called **invariants**, have values that do not change when the coordinate system is rotated. The first invariant, $I_1$, is simply the trace of the stress tensor:
$$ I_1 = \sigma_{11} + \sigma_{22} + \sigma_{33} = tr(\sigma) $$

---

## Deviatoric & Volumetric Stress
Any stress state can be decomposed into two parts:
- **Hydrostatic (Volumetric) Stress**: The average of the normal stresses, $\pi = I_1 / 3$. This component is associated with a change in the material's **volume**.
- **Deviatoric Stress**: The part of the stress that remains after the hydrostatic part is removed. This component is responsible for changes in **shape** (distortion).

---

## Failure Criteria
These criteria predict when a material will yield or fracture under complex loading.
- **Maximum Stress Criterion**: Assumes failure occurs when the maximum principal stress ($\sigma_1$) exceeds the material's uniaxial tensile strength, or the minimum principal stress ($\sigma_3$) is less than its uniaxial compressive strength. This is often used for brittle materials.
- **Von Mises Yield Criterion**: Widely used for ductile materials, it suggests that yielding begins when the **von Mises equivalent stress** ($\sigma_e$) reaches the material's yield strength ($\sigma_y$). This criterion is based on the deviatoric stress (i.e., the energy of distortion).
  $$ \sigma_{e} = \sqrt{3 J_{2}} = \sqrt{\frac{1}{2}[(\sigma_1-\sigma_2)^2 + (\sigma_2-\sigma_3)^2 + (\sigma_3-\sigma_1)^2]} $$