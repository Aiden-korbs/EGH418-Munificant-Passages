["Computational Mechanobiology", "Joint Morphogenesis Models"]

This lecture presents computational studies that simulate the theories of mechanobiological growth.

## Case Study 1: Heegaard (1999) - Finger Joint

- **Hypothesis:** Stresses from normal function modulate cartilage growth to create congruent (interlocking) joint surfaces.
    
- **Model:** 2D Finite Element (FE) model of a fetal finger (PIP) joint.
    
- **Simulation:**
    
    1. **Biology Only:** Both joint surfaces grew and remained convex (incongruent). _(See Slide 53 in `skeletal-growth&adaptation.pdf`)_
        
    2. **Biology + Mechanobiology:** The model correctly predicted the formation of one convex and one concave surface, matching the adult shape. _(See Slide 54 in `skeletal-growth&adaptation.pdf`)_
        
- **Conclusion:** Supports the hypothesis that [[Historical Foundation|mechanobiology]] is crucial for [[Joint Development|joint morphogenesis]].
    
- _(See Slides 47-55 in `skeletal-growth&adaptation.pdf` for study details)_
    

## Case Study 2: Giorgi (2014) - Hinge vs. Ball-Socket

- **Hypothesis:** The _type_ of motion dictates the _type_ of joint shape.
    
- **Model:** 3D FE model of abstract joint rudiments. _(See Slide 57 in `skeletal-growth&adaptation.pdf`)_
    
- **Simulation:**
    
    1. **Hinge Motion (Planar):** The rudiments developed into a hinge-like (convex/concave) joint. _(See Slide 60 in `skeletal-growth&adaptation.pdf`)_
        
    2. **Rotational Motion (3D):** The rudiments developed into an interlocking **ball-and-socket** shape. _(See Slide 61 in `skeletal-growth&adaptation.pdf`)_
        
- **Conclusion:** Provides new insights into how _type_ of prenatal movement drives specific joint morphogenesis.
    
- _(See Slides 56-61 in `skeletal-growth&adaptation.pdf` for study details)_
    

## Case Study 3: Kainz (2021) - Femoral Growth in Cerebral Palsy (CP)

- **Aim:** Investigate why some children with CP develop femoral deformities.
    
- **Model:** Multi-scale mechanobiological simulation using motion capture data from typically developing (TD) children and children with CP.
    
- **Findings:**
    
    - The CP-Pathological growth group had abnormal joint kinematics (e.g., increased knee flexion).
        
    - This led to altered loading characteristics (e.g., less posteriorly-oriented **Hip Joint Contact Forces (JCF)**).
        
    - The **sagittal plane Hip JCF orientation** seems to be the dominant factor driving pathological vs. typical femoral growth.
        
- _(See Slides 62-66 in `skeletal-growth&adaptation.pdf` for graphs and summary diagram)_
    

## Case Study 4: Lipphaus (2025) - Juvenile Femur Growth

- **Aim:** Simulate comprehensive growth of an 8-year-old's femur.
    
- **Model:** FE model combining _all_ growth mechanisms: epiphyseal, apophyseal, appositional, and remodeling (Wolff's Law). _(See Slide 72 in `skeletal-growth&adaptation.pdf` for workflow diagram)_
    
- **Simulation:** Used muscle forces from a dynamic gait cycle.
    
- **Result:** The simulation predicted realistic changes in femur length, neck-shaft angle, anteversion, etc., showing high agreement with anthropometric data. [Image comparing simulated vs anthropometric bone growth changes]
    
- _(See Slides 67-72 in `skeletal-growth&adaptation.pdf` for stress plots and results table)_
    

(Linked from [[Skeletal Growth]])