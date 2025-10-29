["Analytical Modelling", "Muscle Redundancy Problem", "Static Optimisation"]

**Inverse Dynamics** is an _analytical_ process. It answers the question: "Given this _measured_ movement, what forces and moments must have _caused_ it?" This is the most common workflow in biomechanics.

_(See Slide 30 in `MSK+modelling+lecture.pdf` for workflow diagram)_

## Standard Workflow (Motion to Forces)

1. **Input:** Experimental marker trajectories from a motion capture system (e.g., Vicon) and external forces (e.g., force plates).
    
    - _(See Slide 24 in `MSK+modelling+lecture.pdf` for motion capture setup)_
        
2. **[[Validation and Subject Specific|Model Scaling]]**: A generic model is scaled to the subject's anatomy.
    
    - _(See Slide 25 in `MSK+modelling+lecture.pdf` for scaling diagram)_
        
3. **Inverse Kinematics (IK):** An optimisation process that finds the **Joint Angles (**$q$**)** that best match the experimental marker positions.
    
    - `$min_{q}\sum_{i\in markers}w_{i}||x_{i}^{exp}-x_{i}(q)||^{2}$`
        
    - _(See Slide 26 in `MSK+modelling+lecture.pdf`)_
        
4. **Inverse Dynamics (ID):** Uses the joint angles ($q$), angular velocities ($\dot{q}$), and angular accelerations ($\ddot{q}$) from IK, along with external forces ($F$), to solve the Equation of Motion for the **Net Joint Moments (**$\tau_m$**)**.
    
    - `$\tau_{m} = M(q)\ddot{q} + C(q,\dot{q}) - G(q) - F$`
        
    - _(See Slide 23 & 27 in `MSK+modelling+lecture.pdf`)_
        
5. **Static Optimisation (SO):** Solves the **Muscle Redundancy Problem** to distribute the net joint moment $\tau_m$ among individual **Muscle Forces (**$f_m$**)**.
    
    - _(See Slide 28 in `MSK+modelling+lecture.pdf`)_
        
6. **Joint Reaction Analysis (JRA):** Calculates the **Joint Reaction Forces** (JRF) acting at the joint (e.g., hip contact force) by summing muscle forces and joint moments.
    

## The Muscle Redundancy Problem

The core challenge: there are more muscles crossing a joint than there are DOFs at that joint (e.g., shoulder has 18 muscles for 9 DOFs). This means `$\tau_m = \sum (f_m \cdot L_{MA})$` is an **indeterminate system** with an infinite number of possible muscle force combinations.

### Solutions to Redundancy

1. **Static Optimisation:** Finds one "optimal" solution by minimizing a physiological cost function (e.g., `$\min \sum a_{j}^{2}$`, or minimize sum of muscle stress).
    
2. **EMG-Assisted Modelling:** Uses experimental Electromyography (EMG) data to constrain the optimisation, providing a solution that is more specific to the subject's actual muscle activation patterns.
    
    - _(See Slide 29 in `MSK+modelling+lecture.pdf` for EMG setup and processing steps)_
        

(Linked from [[MSK Modelling]])