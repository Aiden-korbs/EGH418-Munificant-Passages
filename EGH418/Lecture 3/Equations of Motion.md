
The motion of a rigid body can be described by:

**Translation:**
$$
\sum \vec{F} = m \vec{a}_{G}
$$

**Rotation about COM:**
$$
\sum \vec{M}_G = I_G \vec{\alpha}
$$

For multi-segment systems in biomechanics:
$$
M(\theta) \ddot{\theta} + C(\theta,\dot{\theta}) + G(\theta) + E = T
$$
where:
- $M$ = inertia matrix
- $C$ = centrifugal/Coriolis terms
- $G$ = gravity terms
- $E$ = other external effects
- $T$ = joint torques/moments

Two main problems:
1. **Inverse dynamics**: given motion ($\theta, \dot{\theta}, \ddot{\theta}$), solve for $T$ and forces.
2. **Forward dynamics**: given forces/torques, solve for resulting motion.

**Link to [[Rigid Body]] in Kinematics:** these are the dynamic counterparts of the rigid-body kinematic equations.

