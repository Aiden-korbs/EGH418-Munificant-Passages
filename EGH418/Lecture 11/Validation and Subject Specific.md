["MSK Model Validation", "Subject-Specific Modelling"]

Ensuring model accuracy and relevance to an individual.

## 1. Validation: "How do we trust the model?"

We compare model outputs to "gold standard" _in vivo_ measurements.

- **Joint Angles (from IK):** Validated against **Bi-plane Fluoroscopy** (dynamic X-ray).
    
    - _(See Slide 31 in `MSK+modelling+lecture.pdf`)_
        
- **Moment Arms (from Model):** Validated against **Cadaveric Tendon Excursion** methods.
    
    - _(See Slide 32 in `MSK+modelling+lecture.pdf`)_
        
- **Muscle Activations/Forces (from SO):** Validated against **surface EMG** (normalized to Max Voluntary Contraction, MVC).
    
    - _(See Slide 33 in `MSK+modelling+lecture.pdf`)_
        
- **Joint Forces (from JRA):** Validated against data from **Instrumented Orthopaedic Implants** (e.g., OrthoLoad, Knee Grand Challenge).
    
    - _(See Slides 34, 35 in `MSK+modelling+lecture.pdf`)_
        

## 2. Subject-Specific Modelling

Moves beyond generic, scaled models to create a model unique to the patient.

- **Generic Scaling:** Standard method. Scales a template model's segment lengths based on marker positions. _(See Slide 25 in `MSK+modelling+lecture.pdf`)_
    
- **Subject-Specific:** Uses **Medical Imaging (MRI/CT)** to create models with:
    
    - Patient-specific bone geometry.
        
    - Patient-specific joint mechanics.
        
    - Patient-specific musculotendon pathways.
        
    - Patient-specific muscle physiological properties.
        
- Combines with **Motion Capture** data (kinematics, EMG) for a highly personalized simulation.
    
- _(See Slide 36 in `MSK+modelling+lecture.pdf` for workflow)_
    

(Linked from [[MSK Modelling]])