## Why We Need Constitutive Equations
In continuum mechanics, we have more unknowns than equations. For a 3D problem, we have:
- **15 Unknowns**: 3 displacements, 6 stress components, 6 strain components.
- **9 Equations**: 3 equations of motion, 6 strain-displacement relations.

> We need 6 additional equations to solve the system. These are the **constitutive relations** (or material laws), which describe the specific mechanical behavior of a material by linking stress to strain.
> $$ \sigma_{ij} = f(\epsilon_{ij}) $$

---

## Generalized Hooke's Law
For **linear, elastic, isotropic** materials, the constitutive relation is the generalized Hooke's Law. An "isotropic" material has the same mechanical properties in all directions.

The behavior of such a material can be described by just two independent constants:
1.  **Young's Modulus ($E$)**: A measure of stiffness.
2.  **Poisson's Ratio ($\nu$)**: Describes the material's tendency to deform in the transverse directions when stretched or compressed in one direction.

Hooke's Law can be written elegantly in matrix form:
$$ \underline{\sigma} = [C] \underline{\epsilon} $$
Where:
- $\underline{\sigma}$ and $\underline{\epsilon}$ are the stress and strain vectors.
- $[C]$ is the 6x6 symmetric **stiffness matrix**, which is a function of E and $\nu$.

The inverse relationship uses the **compliance matrix**, $[S] = [C]^{-1}$:
$$ \underline{\epsilon} = [S] \underline{\sigma} $$

---

## Representative Volume Element (RVE)
For complex, heterogeneous materials like bone, the measured properties (like E) depend on the scale of measurement.

> Properties measured on a large sample are often called **apparent properties** ($E_{app}$) because they average out the effects of the underlying microstructure (like porosity) over a **Representative Volume Element (RVE)**.