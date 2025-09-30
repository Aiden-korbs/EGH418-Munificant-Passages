## Fracture Fixation
**Compression plating** is a surgical technique that uses metal plates to provide absolute stability for simple, transverse fractures.

### The Tension Band Principle
Bones are often loaded eccentrically, which creates both compression and tension. For example, the curved femur experiences tension on its lateral side and compression medially during vertical loading.

> A fixation plate is most effective when placed on the **tension side** of the bone. It acts as a **tension band**, converting the destructive tensile forces into beneficial compression at the fracture site.


---

## Composite Beam Theory
A bone fixed with a plate is a **composite beam**—a structure made of two or more different materials (e.g., bone and titanium). To analyze it, we must convert it into an "equivalent beam" made of a single material.

### The Transformation Factor ($n$)
The key to this process is the **transformation factor, $n$**, which is the ratio of the materials' Young's Moduli.
$$ n = \frac{E_{stiff}}{E_{less\_stiff}} $$

To create an equivalent beam made of the less-stiff material (e.g., bone), we mathematically "widen" the stiffer material (the plate) by a factor of $n$. This widened section mimics the higher stiffness of the original plate.
$$ \text{width}_{\text{transformed}} = n \times \text{width}_{\text{original}} $$

### Stress Calculation
1.  **Transform**: Create the equivalent beam by changing the width of one material using $n$.
2.  **Analyze Geometry**: Find the centroid and second [[Moments of Area]] ($I$) of the new, combined shape.
3.  **Calculate Equivalent Stress**: Apply the flexure formula ($\sigma = My/I$) to the equivalent beam.
4.  **Correct for Real Stress**: The stress in the transformed section must be corrected. To find the true stress in the original, stiffer material, you must multiply the result by $n$.
    > $$ \sigma_{\text{real}} = n \times \sigma_{\text{equivalent}} $$