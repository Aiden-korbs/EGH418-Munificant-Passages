# Summary
Study of human body dimensions, mass distribution, and inertial properties for biomechanical analysis.

## Applications
- [[Link Segment Model]] parameter estimation
- Ergonomics and product design
- Injury biomechanics
- Sports performance analysis

---

## Basic Definitions

- **Anthropometry**: measurement of human body size, shape, proportion, and composition.
- **Static anthropometry**: measurements when body is in a fixed position.
- **Dynamic anthropometry**: measurements during movement.

---

## Key Quantities

- **Body mass (m)**: total mass of the body.
- **Segment mass**: mass of individual body segment.
- **Center of mass (COM)**: point where segment’s mass is evenly distributed in all directions.
- **Moment of inertia (I)**: resistance to angular acceleration about an axis.

---

## Segmental Parameters

From cadaver studies (e.g., Dempster’s data), the following are estimated for each segment:

1. **Mass fraction**: segment mass / total body mass
2. **COM location**: distance from proximal joint as % of segment length
3. **Radius of gyration (k)**: 
$$
I = m k^2
$$
where $k$ is relative to a specified axis through COM.

---

## Estimation Methods

1. **Cadaver-based**:
   - Classical datasets: Dempster (1955), Clauser et al. (1969)
   - Provide % body mass, COM location, radius of gyration

2. **Imaging-based**:
   - MRI, CT scans
   - Can measure living subjects

3. **Mathematical modelling**:
   - Regression equations from population datasets

---

## Example Data (Dempster, adult male)

| Segment   | Mass (%) | COM location (% of length from proximal) | Radius of gyration (% length) |
|-----------|----------|------------------------------------------|--------------------------------|
| Head      | 8.26     | 50.0                                     | 50.0                           |
| Trunk     | 49.70    | 50.0                                     | 50.0                           |
| Thigh     | 14.16    | 43.3                                     | 32.3                           |
| Shank     | 4.33     | 43.3                                     | 30.3                           |
| Foot      | 1.37     | 44.0                                     | 24.0                           |

---

## Scaling to Individual Subjects

If subject’s mass $m_{\text{subject}}$ and segment length $L_{\text{segment}}$ are known:

Segment mass:
$$
m_{\text{segment}} = \text{(mass fraction)} \times m_{\text{subject}}
$$

COM distance from proximal joint:
$$
d_{\text{COM}} = \text{(COM fraction)} \times L_{\text{segment}}
$$

Moment of inertia about COM:
$$
I_{\text{COM}} = m_{\text{segment}} \left(k \times L_{\text{segment}}\right)^2
$$

---

## Relation to [[Link Segment Model]]

These parameters are essential inputs for:
- Calculating net joint moments via [[Lecture 3/Inverse Dynamics]]
- Estimating segmental forces and accelerations from [[-Kinematics-]]
