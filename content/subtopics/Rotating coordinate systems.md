---
tags:
  - mech/rotating-coordinate-system
date-created: 2026-03-09
template-version: m.0
---
[[Rotational Dynamics]]
[[Non-inertial frames]]

If we consider a rotating frame around the $z$ axis with *constant* angular speed $\omega$, we can transform to rotating coordinates like so:
$$
\begin{pmatrix}
x' \\
y' \\
z' 
\end{pmatrix}=\begin{pmatrix}
\cos\omega t & \sin\omega t & 0 \\
-\sin\omega t & \cos\omega t & 0 \\
0 & 0 & 1
\end{pmatrix}\begin{pmatrix}
x \\
y \\
z
\end{pmatrix}
$$
Inverting this and substituting into the typical [[Lagrangian Mechanics|lagrangian]] of a free particle $\mathcal{L}=\frac{1}{2}m(\dot{x}^{2}+\dot{y}^{2}+\dot{z}^{2})$ allows us to rewrite in terms of rotational coordinates as
$$
\mathcal{L}'=\frac{1}{2}m(\dot{\vec{r}}'+\vec{\omega}\times \vec{r}')^{2}
$$
since this must equal the original lagrangian, we have $\dot{\vec{r}}=\dot{\vec{r}}'+\vec{\omega}\times \vec{r}'$. Then evaluating the Euler-Lagrange equations allows us to find (after much effort)
$$
m \ddot{\vec{r}}'=-\underbrace{ m(\vec{\omega}\times(\vec{\omega}\times \vec{r}')) }_{ \text{Centrifugal force} }-\underbrace{ 2m(\vec{\omega}\times  \dot{\vec{r}}')U }_{ \text{Coriolis force} }
$$
which yields the **centrifugal** fictitious force and the **Coriolis** fictitious force #mech/coriolis-force.

It is often useful to split up $\vec{\omega}$ if we are considering some latitude $\phi$ up a spherical rotating body into parallel and perpendicular components relative to the radius vector of that latitude, $\vec{\omega}_{1}$ and $\vec{\omega}_{2}$ so
$$
\vec{F}_{\text{Cor}}=-2m\vec{\omega}_{1}\times  \dot{\vec{r}}'-2m\vec{\omega}_{2}\times  \dot{\vec{r}}'
$$
where the first term tells us motion along the surface will turn right in the northern hemisphere or turn left in the southern, and the second term tells us objects moving along the circumference or into the sphere will experience forces along the direction of the sphere rotation. The first term is what causes cyclones to form and determines their direction of rotation.