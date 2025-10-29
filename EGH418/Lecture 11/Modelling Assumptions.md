["Multi-body Modelling Assumptions", "Rigid Body Dynamics Assumptions"]

To create a computational model, we must make several simplifying assumptions.

1. **Rigid Segments:**
    
    - The body is a system of rigid segments (limbs) that do not deform.
        
    - Each segment has a defined **mass**, **Center of Mass (COM)**, and **Mass Moment of Inertia (**$I$**)** which are fixed in its local coordinate frame.
        
    - _(See Slide 10 in `MSK+modelling+lecture.pdf` for diagram)_
        
2. **Anthropometry:**
    
    - Segment properties (length, mass, COM, $I$) are derived from **anthropometric tables** (e.g., Winter, 1980) or calculated from **medical images** (CT/MRI).
        
    - Tables use ratios based on total body height and mass.
        
    - Medical images allow calculation of mass/inertia from tissue density ($\rho_{muscle}$, $\rho_{bone}$).
        
    - _(See Slides 11, 12 in `MSK+modelling+lecture.pdf`)_
        
3. **Ideal Joints:**
    
    - Segments articulate at **ideal joints**, which are simplified (e.g., rotational).
        
    - The **Joint Center of Rotation (JCR)** is assumed to be fixed in the local frame of both segments.
        
    - Motion is described by a **rotation matrix (**$R$**)** using Euler/Cardan sequences.
        
    - _(See Slide 13 in `MSK+modelling+lecture.pdf`)_
        
4. **Muscles Drive Motion:**
    
    - Muscles generate force ($F$) which creates a torque ($\tau$) around a joint.
        
    - This torque is a product of the force and the muscle's **lever arm (**$L_{MA}$**)**.
        
    - $\tau_{Deltoid} = F_{Deltoid} \cdot L_{MA}$
        
    - This is different from most robots, which are torque-driven.
        
    - _(See Slide 14 in `MSK+modelling+lecture.pdf`)_
        
5. **Muscle Model (Geometry & Mechanics):**
    
    - **Paths:** Muscles are simplified as linear paths (origin to insertion) or paths that wrap around obstacles (bones).
        
    - **Mechanics:** Modeled using a **Hill-Type Muscle Model**, which includes:
        
        - **Contractile Element (CE):** Active force generator (depends on length, velocity, activation).
            
        - **Parallel Elastic Element (PEE):** Passive force from fascia.
            
        - **Series Elastic Element (SEE):** Passive force from tendon.
            
    - _(See Slide 15 in `MSK+modelling+lecture.pdf` for Hill model diagram and force-length/force-velocity curves)_
        

(Linked from [[MSK Modelling]])