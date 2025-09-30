Bone is a natural composite material, primarily composed of a soft, ductile organic phase (mostly collagen) and a hard, brittle mineral phase (hydroxyapatite). This composite nature is key to its unique combination of stiffness and toughness.

## Apparent Properties
Because it is a composite, we often speak of bone's **apparent properties** ($E_{app}$, $\rho_{app}$), which represent the bulk mechanical response of the composite structure, rather than the properties of its individual constituents.

> The apparent stiffness of a composite material depends on the properties of its individual constituents, their volume fractions, and their geometric arrangement.

---

## Rule of Mixtures
The **Rule of Mixtures** provides simple mathematical expressions to estimate the upper and lower bounds for the elastic modulus of a composite material. It considers two idealized arrangements of the constituents.

### Voigt Model (Upper Bound)
This model assumes the constituents are arranged in parallel to the loading direction. In this case, the strain is equal in both phases.
> The Voigt model predicts the **upper bound** for the composite's Young's Modulus, representing the stiffest possible configuration.
> $$ E_{Voigt} = \sum_{i=1}^{N} \phi_i E_i = \phi_f E_f + \phi_m E_m $$
> Where $\phi$ is the volume fraction and $E$ is the Young's modulus of each phase (e.g., fiber and matrix).

### Reuss Model (Lower Bound)
This model assumes the constituents are arranged in series with the loading direction. In this case, the stress is equal in both phases.
> The Reuss model predicts the **lower bound** for the composite's Young's Modulus, representing the most compliant configuration.
> $$ E_{Reuss} = \frac{1}{\sum_{i=1}^{N} \frac{\phi_i}{E_i}} = \frac{1}{\frac{\phi_f}{E_f} + \frac{\phi_m}{E_m}} $$

The true modulus of a real composite, like bone, will lie somewhere between the Voigt and Reuss bounds. The large gap between these bounds for bone highlights its [[Anisotropy and Elasticity Tensors|anisotropy]].