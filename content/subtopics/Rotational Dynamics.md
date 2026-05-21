---
tags:
  - mech/rotational-motion
date-created: 2026-01-27
template-version: m.0
---
[[Mechanics]]
[[Central forces and orbits]]
### Rotational Newton's laws
1. $\vec{\tau}=0\implies\vec{\omega}=\text{const}$
2. $\vec{\tau}=d\vec{J} /dt$ (circular: $\vec{\tau}=I\vec{\alpha}$)
3. $\vec{\tau}_{\text{in}}=-\vec{\tau}_{\text{out}}$
### Plane polar motion
If we differentiate $\vec{r}$ twice we see that
$$
\dot{\vec{r}}=\vec{v}=\underbrace{ \dot{r}\hat{r} }_{ \text{radial motion} }+\underbrace{ r\dot{\theta}\hat{\theta} }_{ \text{circular motion} }
$$
and
$$
\ddot{\vec{r}}=\vec{a}=(\underbrace{ \ddot{r} }_{ \text{radial accel} }-\underbrace{ r\dot{\theta}^{2} }_{ \text{centripetal} })\hat{r}+(\underbrace{ 2\dot{r}\dot{\theta} }_{ \text{coriolis} }+\underbrace{ r \ddot{\theta} }_{ \text{angular accel} })\hat{\theta}
$$
which are the different components of motion. This comes from the two basic plane polar unit vectors $\hat{r}$ and $\hat{\theta}$ and the fact that $\frac{d\hat{r}}{dt}=\hat{\theta}\dot{\theta}$ and $\frac{d\hat{\theta}}{dt}=-\hat{r}\dot{\theta}$
### Rotational vectors
#mech/angular-velocity #mech/angular-acceleration 
If we define that the **angular velocity** vector $\vec{\omega}=\dot{\theta}\hat{n}$ where $\hat{n}$ is the axis of rotation then this naturally leads to **angular acceleration** $\vec{\alpha}=\ddot{\theta}\hat{n}$.

#mech/angular-momentum 
From there we can define angular momentum
$$
\begin{align}
\vec{J} & =\vec{r}\times \vec{p}=I\vec{\omega}
\end{align}
$$
where $\vec{r}$ is the trajectory of the particle, $\vec{p}$ is its momentum, and $I$ is the [[Moment of inertia]], also defined as 
$$
I=mr^{2}
$$
for a point mass $m$ a distance $r$ from the axis of rotation. For more complex cases see the linked article.
#### Circular motion
#mech/torque 
In circular motion we also have that
$$
\dot{\vec{J}}=\vec{r}\times \vec{F}=\vec{\tau}
$$
is the **torque** (ignoring radial motion term).
#### Work and power
#mech/work-power-in-circular-motion 
Are analogous to regular equations in that
$$
W=\int \vec{\tau}\cdot d\vec{\theta}
$$
for $d\vec{\theta}=d\theta \hat{n}$, and
$$
P=\frac{dW}{dt}=\vec{\tau}\cdot\vec{\omega}
$$
### Systems of particles
For a system of many particles, in that absence of external torque and under *central internal forces* angular momentum is conserved. More specifically,
$$
\vec{\tau}_{\text{tot}}=\sum_{i=1}^{N} \vec{r}_{i}\times \vec{F}_{i}^{\text{ext}}=\frac{d\vec{J}_{\text{tot}}}{dt}
$$
Additionally, by considering the [[Centre of Mass]] frame we can find the relation
$$
\vec{J}_{\text{tot}}=\vec{J}'+\vec{r}_{\text{cm}}\times \vec{p}_{\text{cm}}
$$
so the total angular momentum is the sum of the angular momentum in the COM frame with respect to the centre of mass $\vec{J}'$ and the angular momentum of the COM translation in lab coordinates with respect to the lab origin.

It is therefore often convenient to choose the origin as the centre of mass to eliminate any extra angular momentum. The only other case this happens is if the object is moving radially so $\vec{r}_{\text{cm}}\parallel  \dot{\vec{r}}_{\text{cm}}$
### [[Moment of inertia]]
Includes *inertia tensor*, *common inertias*, *axis theorems*.
### [[Rotating coordinate systems]]
Includes the lagrangian in a rotating coordinate system, *centrifugal* and *Coriolis force*.
### Table of reference
Fucking hell

| Linear quantities                                                   | Equation link to plane polars                                                                                                                 | Rotational quantities                                                                     |
| ------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| Displacement $\vec{r}$ ($m$)                                        | $\vec{r}=r(\hat{i}\cos\theta+\hat{j}\sin\theta)$                                                                                              | Angular displacement $\vec{\theta}$ ($\text{rad}$)                                        |
| Velocity $\vec{v}=\dot{\vec{r}}$ ($\text{m s}^{-1}$)                | gen: $\vec{v}=\dot{r}\hat{r}+r\dot{\theta}\hat{\theta}$, circ: $\vec{v}=r\dot{\theta}\hat{\theta}=r\omega\hat{\theta}$                        | Angular velocity $\vec{\omega}=\dot{\vec{\theta}}$ ($\text{rad s}^{-1}$)                  |
| Acceleration $\vec{a}=\dot{\vec{v}}$ ($\text{m s}^{-2}$)            | gen: $\vec{a}=(\ddot{r}-r\dot{\theta}^{2})\hat{r}+(2\dot{r}\dot{\theta}+r\ddot{\theta})\hat{\theta}$, circ: $\vec{a}=-\frac{v^{2}}{r}\hat{r}$ | Angular acceleration $\vec{\alpha}=\dot{\vec{\omega}}$, ($\text{rad s}^{-1}$)             |
| Mass $m$ ($\text{kg}$)                                              | $I=\sum_{i}m_{i}r_{i}^{2}$                                                                                                                    | Moment of inertia $I$ ($\text{kg m}^{2}\text{ rad}^{-1}$)                                 |
| Momentum $\vec{p}=m\vec{v}$ ($\text{kg m s}^{-1}$)                  | gen: $\vec{J}=\vec{r}\times \vec{p}$, circ: $\vec{J}=mr^{2}\vec{\omega}=I\vec{\omega}$                                                        | Angular momentum $\vec{J}=I\vec{\omega}$ ($\text{kg m}^{2}\text{ s}^{-1}$)                |
| Force $\vec{F}=\frac{d\vec{p}}{dt}$ ($\text{N}=\text{kg m s}^{-1}$) | gen: $\vec{\tau}=\frac{d\vec{J}}{dt}=\sum_{i}\vec{r}_{i}\times \vec{F}_{i}$, circ: $\vec{\tau}=I\vec{\alpha}$                                 | Torque $\vec{\tau}=\frac{d\vec{J}}{dt}$ ($\text{kg m}^{2}\text{ s}^{-2}\text{ rad}^{-1}$) |
| Work $W=\int \vec{F}\cdot d\vec{x}$ ($\text{N m}$)                  | gen: $W=\int \vec{\tau}\cdot d\vec{\theta}+\int \vec{F}\times\vec{\theta}\cdot d\vec{r}$, circ: $W=\int \vec{\tau}\cdot\vec{\omega}\,dt$      | Work $W=\int \vec{\tau}\cdot d\vec{\theta}$ ($\text{N m}$)                                |


