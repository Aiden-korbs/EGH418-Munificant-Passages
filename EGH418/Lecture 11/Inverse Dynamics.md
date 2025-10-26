["Analytical Modelling", "Muscle Redundancy Problem", "Static Optimisation"]

**Inverse Dynamics** is an _analytical_ process, working backward from observed motion to the forces that caused it. It answers the question: "Given a specific measured movement, what were the net forces and moments acting at the joints, and how did individual muscles contribute?" This is the most common workflow in clinical biomechanics.

- _See Slide 30 for summary workflow diagram._
    

## Workflow (Motion to Forces)

1. **Input:** Experimental marker trajectories recorded using a motion capture system (e.g., Vicon optical system, IMUs, fluoroscopy).
    
    - _See Slide 24 for images of motion capture technologies and marker setup._
        
2. **[[EGH418 - MSK Modelling - 5. Validation and Subject-Specific|Model Scaling]]**: A generic MSK model (bones, joints, muscle paths) is scaled to match the specific subject's body size.
    
    - Uses static pose marker data to adjust segment lengths.
        
    - _See Slide 25 for scaling diagram._
        
3. **Inverse Kinematics (IK):** An optimisation step that calculates the **Joint Angles (**$q(t)$**)** over time that best reproduce the experimental marker trajectories.
    
    - Minimizes the weighted squared error between experimental markers ($x^{exp}$) and model markers ($x(q)$):
        
    - `$min_{q}\sum_{i\in markers}w_{i}||x_{i}^{exp}-x_{i}(q)||^{2}$`
        
    - _See Slide 26 for IK concept._
        
4. **Inverse Dynamics (ID):** Uses the calculated joint angles ($q$), angular velocities ($\dot{q}$), and angular accelerations ($\ddot{q}$), along with external forces (e.g., Ground Reaction Forces from force plates), to calculate the **Net Joint Moments (**$\tau_m(t)$**)** required to produce the motion.
    
    - Rearranges the Equation of Motion:
        
    - `$\tau_{m} = M(q)\ddot{q} + C(q,\dot{q}) - G(q) - F$`
        
    - _See Slide 23 for equations._
        
5. **Static Optimisation (SO) / Muscle Force Distribution:** Solves the **[[EGH418 - MSK Modelling - 4. Inverse Dynamics#The Muscle Redundancy Problem|Muscle Redundancy Problem]]** to estimate the contribution of individual **Muscle Forces (**$f_m(t)$**)** to the net joint moment.
    
6. **Joint Reaction Analysis (JRA):** Calculates the **Joint Reaction Forces (JRF)** (bone-on-bone forces) by considering the net joint moments, muscle forces, and external forces acting across the joint.
    

## The Muscle Redundancy Problem

- **The Problem:** There are typically more muscles crossing a joint than there are degrees of freedom (DOFs) at that joint (e.g., shoulder: ~18 muscles vs 9 DOFs).
    
- **The Consequence:** An infinite number of combinations of individual muscle forces could produce the _same_ required net joint moment ($\tau_m$). The system is mathematically _indeterminate_.
    
- _See Slide 27 for shoulder example._
    

### Solutions to Redundancy

1. **Static Optimisation (SO):** Assumes muscles coordinate to achieve a goal, represented by minimizing a mathematical cost function. Common cost functions:
    
    - Minimize sum of muscle activations squared: `$\min \sum a_{j}^{2}$`
        
    - Minimize sum of muscle forces squared: `$\min \sum f_{j}^{2}$`
        
    - Minimize sum of muscle stresses squared: `$\min \sum (\frac{f_j}{PCSA_j})^{2}$`
        
    - _See Slide 28 for elbow example illustrating how different forces satisfy the same moment requirement._
        
2. **EMG-Assisted / EMG-Driven Modelling:** Uses experimentally measured Electromyography (EMG) signals from surface or fine-wire electrodes as an indicator of muscle activation timing and intensity. This data is used to _constrain_ the optimisation, leading to a more physiologically realistic solution.
    
    - Requires careful EMG processing (rectification, filtering, normalization to MVC).
        
    - _See Slide 29 for EMG processing pipeline and electrode placement example._