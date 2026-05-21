---
tags:
  - "#mech/two-body-collisions"
date-created: 2025-12-17
template-version: m.0
---
### Impulse
#mech/impulse 
Impulse is defined as a change/exchange in momentum due to a force between two bodies. Specifically:
$$
\Delta \vec{p}=I=\int _{t_{1}}^{t_{2}}\vec{F} \, dt 
$$
### Collisions
We classify collisions into:
- elastic (energy conserved)
- inelastic (energy lost)
- superelastic (energy gained)
But really the first two are the only important ones. Examples found in notes for different types of collisions. It is often useful to solve these in the [[Centre of Mass]] frame.
#mech/inelastic-collisions 

#### Coefficient of restitution
#mech/coefficient-of-restitution 
This is simply defined as the change in relative velocity:
$$
e=\frac{{|v_{1}-v_{2}|}}{|u_{1}-u_{2}|}
$$
which is especially useful in the [[Centre of Mass]] frame. We also have that
$$
e=\sqrt{ 1-\frac{\Delta E}{T_{cm}^\text{inital}} }
$$