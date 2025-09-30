Mathematical models are essential tools for understanding spine biomechanics, as they allow us to estimate internal forces and stresses that cannot be easily measured *in vivo*.

## Why We Need Models
- To estimate loads on spinal structures like discs and facets during different activities.
- To understand the mechanisms of injury and pathology.
- To design and evaluate spinal implants and surgical procedures.
- To analyse complex human movements.

---

## Types of Models

### Simple Models
For analysing basic principles of balance and stability, the spine and upper body can be simplified.
- **Single Inverted Pendulum**: Represents the entire trunk as a single rigid body rotating about the hip or ankle.
- **Double Inverted Pendulum**: A more complex model representing the trunk and legs as two separate linked segments. These models are inherently unstable and are used to study motor control and balance strategies.

### Complex Musculoskeletal Models
To accurately calculate muscle forces and joint loads, detailed musculoskeletal models are required.
- **Static Indeterminacy**: The spine has many more muscles than degrees of freedom. This means there are infinite possible combinations of muscle forces that could produce a given movement. This is known as the "redundancy problem".
- **Solving the Problem**: Computational platforms like OpenSim use [[Inverse Dynamics in 3D]] to calculate the net joint moments from motion capture data. Then, an **optimisation** algorithm is used to solve the redundancy problem by distributing the net moment among the individual muscles, usually by minimising an objective function like the sum of muscle activations squared.
- **EMG-Informed Models**: A more advanced approach that uses electromyography (EMG) data to inform the model about the actual muscle recruitment strategy used by a person, overcoming some limitations of pure optimisation.