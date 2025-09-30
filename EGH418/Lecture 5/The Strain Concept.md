**Strain** ($\epsilon$) is the measure of deformation, representing the relative displacement between particles in a body. It's a dimensionless quantity that describes how much an object's size or shape has changed.

## Normal Strain ($\epsilon$)
Normal strain describes the change in length of a line segment per unit length.

> **Average Normal Strain**: The total change in length ($\delta$) divided by a reference length ($L_{ref}$).
> $$ \epsilon_{av} = \frac{\delta}{L_{ref}} $$

At a specific point, the normal strain is the partial derivative of the displacement field ($u$) with respect to position ($x$):
$$ \epsilon_{xx} = \frac{\partial u}{\partial x} $$
The **volumetric strain ($\epsilon_v$)** is the change in volume per unit volume, which for small strains is simply the sum of the normal strains: $\epsilon_v \approx \epsilon_{xx} + \epsilon_{yy} + \epsilon_{zz}$.

---

## Shear Strain ($\gamma$)
Shear strain describes a change in **shape** caused by a change in the angle between two lines that were originally perpendicular.

> **Shear Strain** is defined as the **change in the angle** between two originally perpendicular lines.



For a point, the shear strain in the x-y plane is related to the gradients of the displacement field:
$$ \gamma_{xy} = \frac{\partial u}{\partial y} + \frac{\partial v}{\partial x} $$

---

## The Strain Tensor
Just like stress, the complete 3D state of strain at a point is described by the symmetric **strain tensor**.
- The diagonal terms are the **normal strains** ($\epsilon_{xx}, \epsilon_{yy}, \epsilon_{zz}$).
- The off-diagonal terms are the **shear strains**.
- **Tensor Notation**: To ensure proper tensor transformation, the shear terms are defined as $\epsilon_{xy} = \frac{1}{2}\gamma_{xy}$.
  $$ \epsilon_{ij} = \begin{bmatrix} \epsilon_{xx} & \frac{1}{2}\gamma_{xy} & \frac{1}{2}\gamma_{xz} \\ \frac{1}{2}\gamma_{yx} & \epsilon_{yy} & \frac{1}{2}\gamma_{yz} \\ \frac{1}{2}\gamma_{zx} & \epsilon_{zy} & \epsilon_{zz} \end{bmatrix} $$