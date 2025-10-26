["Multi-body Modelling Assumptions", "Rigid Body Dynamics Assumptions"]

To computationally model the human body, we make simplifying assumptions.

1. **Rigid Segments:** Limbs are treated as rigid bodies.
    
    - Define segment **mass**, **Center of Mass (COM)**, and **Mass Moment of Inertia (**$I$**)**.
        
    - COM and $I$ are fixed in the local segment frame.
        
    - _See Slide 10 for diagram of rigid segment model._
        
2. **Anthropometry:** Segment properties (mass, COM, $I$, length) are obtained from:
    
    - **Anthropometric tables** (e.g., Winter, 1980 - scaled based on body height/mass).
        
        - _See Slide 11 for example table and scaling diagram._
            
    - Calculations from **medical images** (CT/MRI) using density functions ($\rho$) and volume integrals.
        
        - _See Slide 12 for integral formulas and typical tissue densities._
            
3. **Ideal Joints:** Limbs articulate at **ideal joints** (mostly rotational).
    
    - Joint center of rotation is fixed in the local frame.
        
    - Child frame rotation is described relative to parent frame using a rotation matrix ($R$).
        
    - Use Euler/Cardan sequences (e.g., Z-X-Y) to decompose 3D motion.
        
        - _See Slide 13 for rotation matrix examples._
            
4. **Muscles Drive Motion:** Joints are driven by muscle forces, not direct torques like robots.
    
    - Muscle force ($F$) creates a joint torque ($\tau$) based on its lever arm / moment arm ($L_{MA}$).
        
    - `$\tau = F \cdot L_{MA}$`
        
    - _See Slide 14 for diagram comparing muscle leverage to robot actuators._
        
5. **Muscle Paths:** Muscles are simplified as:
    
    - Linear paths (lines) between origin and insertion.
        
    - Sometimes including "wrapping" points or surfaces (cylinders, spheres) to simulate muscles bending around bones/joints.
        
    - _See Slide 15 for image of muscle wrapping._
        
6. **Muscle Model:** Muscles follow a **Hill-Type Mechanical Model**.
    
    - Includes: Contractile Element (CE), Parallel Elastic Element (PEE), Series Elastic Element (SEE - tendon).
        
    - Muscle force depends on its **length**, contraction **velocity**, and neural **activation**.
        
    - _See Slide 15 & 20 for Hill model diagram and force-length-velocity curves._