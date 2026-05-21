---
tags:
  - mech
date-created: 2025-12-17
template-version: m.0
---
#mech/centre-of-mass 
The centre of mass of a system is defined in mechanics by 
$$
\int_{V} (\vec{v}-\vec{v}_{cm})dm=0
$$
which for a system of particles reduces to
$$
\vec{r}_{cm}=\frac{\sum_{i=1}^{n} m_{i}\vec{r}_{i}}{\sum_{i=1}^{n} m_{i}}
$$
One thing to note is that if we have a system of two particles with internal forces acting in [[Harmonic Oscillators|simple harmonic motion]] we can treat it as one system with the reduced mass
$$
\mu=\frac{m_{1}m_{2}}{m_{1}+m_{2}}
$$
This is because internal forces do not change the velocity of the centre of mass, only external forces do. See [[Central forces and orbits#2 body problem]].

### COM frame
#mech/centre-of-mass-frame 
If we transition to the centre of mass frame by boosting by
$$
\Delta v=-v_{cm}=-\dot{x}_{cm}=\frac{1}{M}\sum_{i=1}^{n} m_{i}v_{i}
$$
the total momentum of the frame is now zero. We also have the relation that
$$
E^k_{\text{lab}}=E^k_{\text{cm}}+\frac{1}{2}Mv_{cm}^{2}
$$
Additionally for the system we have that
$$
M \ddot{\vec{r}_{}}_{\text{cm}}=\sum_{i=1}^{N} \vec{F}^{\text{ext}}_{i}
$$
so internal forces can be ignored due to N3. Similar relations exist for [[Rotational Dynamics]].