## What is Stress?
**Stress** ($\sigma$) is a measure of the internal forces acting within a deformable body. It's a macroscopic abstraction of the complex interatomic forces at play.

> Stress has the physical dimension of **force per unit area** ($N/m^2$ or Pascals). It's the key metric for assessing a material's resistance to yielding or fracture.

---

## Euler-Cauchy Stress Principle
This principle describes how forces are transmitted across imaginary internal surfaces within a body.
- **Traction Vector ($T^{(n)}$)**: At any point on an internal surface with a normal vector **n**, the force per unit area is called the traction or stress vector.
- **Decomposition**: The traction vector can be broken down into:
  1.  **Normal Stress ($\sigma_n$)**: The component perpendicular to the surface.
  2.  **Shear Stress ($\tau_n$)**: The component parallel to the surface.



---

## The Cauchy Stress Tensor
The complete state of stress at a single point is defined by the **Cauchy Stress Tensor** ($\sigma$), a 3x3 matrix.

> The stress tensor is a mathematical object that relates the normal vector of *any* plane passing through a point to the traction vector acting on that plane.
> $$ T^{(n)} = n \cdot \sigma $$

The tensor contains all 9 stress components (3 normal, 6 shear):
$$ \sigma = [\sigma_{ij}] = \begin{bmatrix} \sigma_{xx} & \tau_{xy} & \tau_{xz} \\ \tau_{yx} & \sigma_{yy} & \tau_{yz} \\ \tau_{zx} & \tau_{zy} & \sigma_{zz} \end{bmatrix} $$
- **Symmetry**: Due to the conservation of angular momentum, the stress tensor must be **symmetric** ($\tau_{xy} = \tau_{yx}$, etc.). This reduces the number of independent components from 9 to 6.