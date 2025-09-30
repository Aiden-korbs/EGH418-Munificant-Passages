The way stress is distributed in a bending bone depends entirely on the shape of its cross-section. We quantify this shape using **moments of area**.

## First Moment of Area ($S$)
The first moment of area measures the distribution of an area relative to an axis. Its most important use is to find the **centroid**.

> The **centroid** is the geometric center of the cross section. By definition, the first moment of area about any axis passing through the centroid is zero.

The centroid's coordinates ($\bar{y}_S, \bar{z}_S$) are found by dividing the first moments of area by the total area A:
$$ \bar{y}_S = \frac{S_{\bar{z}}}{A} \quad \text{and} \quad \bar{z}_S = \frac{S_{\bar{y}}}{A} $$

---

## Second Moment of Area ($I$)
The **second moment of area**, or **moment of inertia**, is a geometric property that describes a cross-section's resistance to bending and torque.
- It has units of $[length]^4$.
- A larger moment of inertia means the shape is more resistant to bending.
  $$ I_{y} = \int_A z^2 dA $$

### Parallel Axis Theorem (Steiner's Theorem)
This theorem is crucial for finding the moment of inertia of complex shapes by breaking them down into simpler parts.

> The moment of inertia about any new axis is the moment of inertia about a parallel axis through the centroid, plus the area times the squared distance between the axes.
> $$ I_{\text{new axis}} = I_{\text{centroid}} + A d^2 $$

### Principal Axes & Pure Bending
- **Principal Axes** ($\eta, \zeta$): A unique pair of orthogonal axes passing through the centroid for which the moments of inertia are maximum and minimum. An axis of symmetry is always a principal axis.
- **Pure Bending**: A simplified loading case where a beam is only subjected to a bending moment and no other forces. The stress during pure bending about a principal axis is given by the classic flexure formula:
  $$ \sigma_x = \frac{M_\eta}{I_\eta}\zeta $$
- The **neutral axis** is the line on the cross-section where the bending stress is zero. For pure bending, this is the principal axis perpendicular to the applied moment.