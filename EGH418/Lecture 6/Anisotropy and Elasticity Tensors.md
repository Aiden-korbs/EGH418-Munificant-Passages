For simple isotropic materials, [[Constitutive Equations and Hooke's Law]] can be described with just two constants (E and $\nu$). However, materials like bone are **anisotropic**, meaning their properties are direction-dependent. To describe this behaviour, we need a more general framework.

## Generalised Hooke's Law
The full 3D relationship between stress and strain is described by the **fourth-order elasticity tensor**, $C$.

> In tensor notation, the law is written as:
> $$ \sigma_{ij} = C_{ijkl} \epsilon_{kl} $$

The stiffness tensor $C_{ijkl}$ contains 81 components initially. However, due to the symmetry of the [[The Stress Concept and Cauchy's Tensor|stress]] and [[The Strain Concept|strain]] tensors, this number reduces to 21 independent elastic coefficients for the most general anisotropic case.

---

## Effect of Material Symmetry
The number of independent elastic constants required to describe a material decreases as its structural symmetry increases.

- **Anisotropic (21 constants)**: No planes of material symmetry.
- **Orthotropic (9 constants)**: Three mutually orthogonal planes of symmetry. This model is commonly used for cortical bone, with axes aligned in the longitudinal, radial, and circumferential directions.
- **Transversely Isotropic (5 constants)**: An infinite number of symmetry planes around one axis (e.g., a bundle of fibers). This is sometimes used as a simpler model for cortical bone.
- **Isotropic (2 constants)**: The material has the same properties in all directions.

The compliance matrix ($S = C^{-1}$) for an orthotropic material relates the nine engineering constants ($E_x, E_y, E_z, \nu_{xy}, \nu_{xz}, \nu_{yz}, G_{xy}, G_{xz}, G_{yz}$) to the components of the stiffness matrix.