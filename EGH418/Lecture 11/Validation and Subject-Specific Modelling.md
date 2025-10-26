It's crucial to validate the outputs of [[EGH418 - MSK Modelling - Main|MSK models]] against real-world measurements to ensure their accuracy and reliability.

## 1. Model Scaling vs. Subject-Specific Modelling

- **Generic Model Scaling:** Starts with a model based on cadaveric data and scales segment lengths based on participant's marker positions in a static pose. Anthropometric tables might be used for mass/inertia properties. This is the standard approach.
    
    - _See Slide 25 for scaling diagram._
        
- **Subject-Specific Modelling:** A more advanced approach that uses medical imaging (MRI, CT) to create a model with the participant's _exact_ bone geometry, joint parameters, muscle origins/insertions, and potentially muscle physiological properties.
    
    - _See Slide 36 for components required for subject-specific modelling._
        

## 2. Validation Techniques

Outputs at various stages of the [[EGH418 - MSK Modelling - 4. Inverse Dynamics|Inverse Dynamics]] workflow can be validated:

- **Validation of Joint Angles (IK Output):**
    
    - **Gold Standard:** Bi-plane Fluoroscopy (dynamic X-ray).
        
    - **Purpose:** To quantify the accuracy of [[EGH418 - MSK Modelling - 4. Inverse Dynamics|Inverse Kinematics]] calculated using skin-based markers, which are prone to soft tissue artefact.
        
    - _See Slide 31 for bi-fluoroscopy setup diagram._
        
- **Validation of Muscle Moment Arms (Model Geometry):**
    
    - **Method:** Cadaveric testing using the "tendon-excursion method" (measuring tendon displacement for a given joint rotation).
        
    - **Purpose:** To verify that the geometric relationship between muscles and joints in the model matches reality.
        
    - _See Slide 32 for cadaver rig diagram and moment arm comparison graphs._
        
- **Validation of Muscle Activations/Forces (SO/EMG-Driven Output):**
    
    - **Method:** Compare model-predicted muscle activations against experimentally measured **Electromyography (EMG)** signals.
        
    - **Requires:** Normalizing EMG signals using **Maximum Voluntary Contraction (MVC)** trials.
        
    - _See Slide 33 for EMG setup photo and activation comparison graphs._
        
- **Validation of Joint Forces (JRA Output):**
    
    - **Gold Standard:** _In-vivo_ measurements from **instrumented implants** (e.g., hip, knee, shoulder prostheses with built-in force sensors).
        
    - **Databases:** OrthoLoad (Germany), Knee Grand Challenge (USA).
        
    - **Purpose:** To directly compare the final calculated bone-on-bone forces with measured forces during activities like walking.
        
    - _See Slide 34 for instrumented implant photo and joint force comparison graphs._
        
    - _See Slide 35 for Knee Grand Challenge data._