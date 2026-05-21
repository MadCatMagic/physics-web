---
tags:
  - mech
date-created: 2025-12-17
template-version: m.0
---
[[Mechanics Textbooks]]
[[Mechanics L_MT1]]
[[Mechanics L_HT1]]
### Energy and Forces
#mech/work-done 
For a force $\vec{F}$ acting along a curve $C$ we have the **work done** $W$ as the energy transferred by that force to the object being acted on by the force is 
$$
W=\int_{C}\vec{F}\cdot d\vec{r}
$$

We also have **newtons laws**: #mech/newtons-laws 
- $\sum \vec{F}=0\iff \vec{v}=\text{const}$
- $\vec{F}=\frac{d\vec{p}}{dt}$
- $\vec{F}_{ab}=-\vec{F}_{ba}$
And the **principle of mass equivalence** that states that 
- inertial mass = gravitational mass
in the case of Newtonian gravity. #mech/principle-of-equivalence 

Usually, with rigid bodies or particles the mass is constant so $\vec{F}=\frac{d\vec{p}}{dt}$ reduces to $\vec{F}=m\vec{a}$. However if mass is not constant then more analysis is required - [[Changing Mass with Newton's Laws]].

#mech/frames-of-reference 
These operate in a particular **frame of reference**. We usually consider *classical* frames where time is absolute, specifically *inertial* frames where Newton's first law is satisfied (not an accelerating RF). In [[Special Relativity]] we also have *relativistic* frames where we have to use space-time frames that are inertial. There are also [[Non-inertial frames]] where newton's laws seem to not hold.

#mech/momentum-conservation 
Very importantly we also have that **momentum is conserved** in all frames. (for a closed system)
### [[Lagrangian Mechanics]]
General description of the formalism, as well as [[Hamiltonian Mechanics]] as a minor extension (at the moment) since we have not been taught it much.
### [[Rotational Dynamics]]
Includes *newton's laws of rotation*, *torque*, *moment of inertia*, *angular momentum*, etc. *Rotating coordinate systems*.
#### [[Central forces and orbits]] and orbits
Includes *central forces*, *orbits in central forces*, *orbit equation*, *Kepler's laws*, *two-body problem*.
### [[Harmonic Oscillators]]
Are a simple application of newtons forces and are important for many topics when considering the particular oscillatory solution in a system i.e. close to a potential energy minimum. 
#### [[Normal Modes]]
Is a generalisation of harmonic oscillators.
### [[Conservative forces]]
Includes *conservative forces*, *energy conservation*, *potential*.
### [[Centre of Mass]]
Centre of mass is the point through which forces appear to act as if it was a point particle, and the centre of mass frame is the one in which total momentum is zero.
### [[Two Body Collisions]]
Newtonian collisions between two bodies.
### Resistive forces
#mech/resistive-forces 
There are two classes of resistive forces for an object moving through a fluid:
- **laminar flow**: $F\propto v$
- **turbulent flow**: $F\propto v^{2}$
