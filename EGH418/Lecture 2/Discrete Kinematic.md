# Finite Difference

Let samples be equally spaced with timestep $\Delta t$.

## Position → velocity (central difference)
$$v_i = \frac{x_{i+1} - x_{i-1}}{2\,\Delta t}$$

## Velocity → acceleration (central difference)
$$a_i = \frac{x_{i+1} - 2x_i + x_{i-1}}{\Delta t^2}$$

## Angular equivalents
$$\omega_i = \frac{\theta_{i+1} - \theta_{i-1}}{2\,\Delta t}, \qquad \alpha_i = \frac{\theta_{i+1} - 2\theta_i + \theta_{i-1}}{\Delta t^2}$$

(Use forward/backward differences at the first/last sample if needed.)
