
## Absolute segment angle (from endpoints)
Given points $(x_1,y_1)$ (proximal) and $(x_2,y_2)$ (distal),
use:
$$\theta = \operatorname{atan2}(y_2 - y_1,\ x_2 - x_1)$$
(atan2 handles correct quadrants; anticlockwise positive.)

## Joint angles (examples)
Knee:
$$\theta_{\text{knee}} = \theta_{\text{thigh}} - \theta_{\text{shank}} \quad\text{(positive = flexion)}$$

Ankle:
$$\theta_{\text{ankle}} = \theta_{\text{shank}} - \theta_{\text{foot}} + 90^\circ \quad\text{(positive = plantarflexion)}$$

## Gait cycle
Joint angles plotted over % gait cycle show characteristic phases of flexion/extension.
