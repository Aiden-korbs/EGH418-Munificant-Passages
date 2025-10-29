["Predictive Modelling", "Equation of Motion"]

**Forward Dynamics** is a _predictive_ simulation. It answers the question: "If I apply these neural commands, what motion will occur?"

_(See Slides 18-22 in `MSK+modelling+lecture.pdf`)_

## Workflow

Neural Command ($u(t)$) $\rightarrow$ Contraction Dynamics $\rightarrow$ Muscle Activation ($a(t)$) $\rightarrow$ Musculo-tendon Dynamics $\rightarrow$ Muscle Force ($f$) $\rightarrow$ Multi-body Dynamics $\rightarrow$ Joint Torques ($\tau_m$) $\rightarrow$ Solve Eq. of Motion $\rightarrow$ Joint Accelerations ($\ddot{q}$).

- **Contraction Dynamics:** Models the delay and non-linear transformation from neural command $u(t)$ to muscle activation $a(t)$.
    
- **Musculo-tendon Dynamics:** Calculates muscle force $f(t)$ from $a(t)$ using the [[Modelling Assumptions|Hill-Type Model]].
    
- **Multi-body Dynamics:** Calculates net joint torques $\tau_m$ from all muscle forces.
    

## Equation of Motion

The core of forward dynamics is solving the equation of motion for angular acceleration ($\ddot{q}$), which is then integrated to find velocity and position ($q$):

$\ddot{q} = M(q)^{-1} \{ \tau_{m}(a,l,\dot{l}) - C(q,\dot{q}) + G(q) + F \}$` Where:

- $M(q)$: Mass matrix
    
- $\tau_m$: Muscle-generated joint moments
    
- $C(q,\dot{q})$: Coriolis and centripetal forces
    
- $G(q)$: Gravitational forces
    
- $F$: External forces _(See Slide 21 in `MSK+modelling+lecture.pdf`)_
    

## Use Cases & Challenges

- **Use:** Predictive "what-if" scenarios, testing control strategies, learning/ML. _(See Slide 22 for simulation examples)_
    
- **Challenges:**
    
    - Very sensitive to model parameters and errors.
        
    - Computationally costly.
        
    - Access to realistic neural commands ($u(t)$) is extremely difficult.
        

(Linked from [[MSK Modelling]])