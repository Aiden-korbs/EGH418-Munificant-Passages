When a bone is loaded, internal forces and moments develop within it to maintain equilibrium. In beam theory, we analyze these by imagining a cut through the bone's cross-section.

> In beam theory, we work with **internal forces**, which are simply the stresses integrated over the cross-sectional area.

## Definitions
- **Normal Force ($N$)**: The force acting perpendicular to the cut surface, causing tension or compression.
  - $$ N = \int_A \sigma_x dA $$
- **Shear Forces ($Q_y, Q_z$)**: Forces acting parallel to the surface, causing shear.
  - $$ Q_y = \int_A \tau_{xy} dA $$
- **Bending Moments ($M_y, M_z$)**: Moments that cause the bone to bend.
  - $$ M_z = -\int_A y \sigma_x dA $$

---

## Bernoulli's Hypothesis & Axial Stress
A key assumption of beam theory is **Bernoulli's hypothesis**.

> **Bernoulli's Hypothesis**: A cross-section that is flat before bending remains flat after bending.

This simple assumption has a powerful consequence: the axial strain ($\epsilon_x$), and therefore the axial stress ($\sigma_x$), must vary linearly across the cross-section.

For a general loading case where the coordinate axes are the [[Moments of Area|principal axes]] ($\eta, \zeta$), the **axial stress** at any point is given by:
$$ \sigma_x = \frac{N}{A} - \frac{M_\zeta}{I_\zeta}\eta + \frac{M_\eta}{I_\eta}\zeta $$

This elegant equation is powerful because it connects the overall forces and moments on the bone (which can be found using [[Inverse Dynamics in 3D]] from measured [[3D Kinematics]]) to the stress experienced by the tissue at any point.