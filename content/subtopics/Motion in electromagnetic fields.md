---
tags:
  - "#elecmag/motion-in-electromagnetic-fields"
date-created: 2026-02-02
template-version: m.0
---
[[Electromagnetism]]

Discusses the motion of a charged particle $q$ through electromagnetic fields.
### Lorentz force law
#elecmag/lorentz-force 
We use the **Lorentz force** given by
$$
\vec{F}=q(\vec{v}\times \vec{B}+\vec{E})
$$
to determine the force on particles in an electric and magnetic field. For a length of wire $dl$ in a magnetic field $\vec{B}$, with current $d\vec{J}=I\,d\vec{l}$ we have
$$
d\vec{F}=d\vec{J}\times \vec{B}=Id\vec{l}\times \vec{B}
$$
so we can show the work done is $dW=\vec{F}\cdot d\vec{l}=0$ hence *magnetic forces do no work*.
### Only magnetic field
In the simple case of $\vec{B}\perp \vec{v}$, we intuitively find circular motion since $\vec{F}\perp \vec{v}$ so from equating the centripetal force,
$$
R=\frac{m|\vec{v}|}{q|\vec{B}|}=\frac{p}{qB}
$$
gives the *Larmor* or *gyro* or *cyclotron radius*. Then also
$$
\tau=\frac{2\pi R}{v}=\frac{2\pi m}{qB}
$$
is the *Larmor period* which is constant for a given $B$ and particle type.

The kinetic energy here is just given by
$$
T_{x}+T_{y}=\frac{1}{2} m u_{0}^{2}(\cos ^{2}\omega t+\sin ^{2}\omega t)=\frac{1}{2}m u_{0}^{2}
$$
is constant and depends on the initial velocity $u_{0}$.

If we then have that $\vec{B}$ is not perpendicular to $\vec{v}$, and assuming w.l.o.g. that $\vec{B}\perp \hat{z}$ then the force due to the magnetic force is the same, it just recedes i.e.
$$
\begin{align}
x & =R\sin\omega t \\
y+R & =R\cos\omega t \\
z & =v_{z}t
\end{align}
$$
which forms a helix.
### Including electric field
Use the [[Electromagnetism#Lorentz force law]]
If we use the assumptions that
1. $\vec{B}\perp \vec{E}$
2. $\vec{B}\perp \vec{v}$
and have the initial conditions $\vec{x}_{0}=(0,0,0)^{T},\vec{v}_{0}=(0,0,0)^{T}$ then we can solve the differential equations to find
$$
\begin{align}
x & =x_{2}(1-\cos\omega t) \\
y & =x_{2}(\sin\omega t-\omega t)
\end{align}
$$
where $x_{2}=\frac{qE_{x}}{m\omega^{2}}$. We are assuming the electric field is along the x-dir. This describes an evolving circle, a cycloid in fact.

The kinetic energy in this case is
$$
T=\frac{1}{2}m(x_{2}\omega)^{2}(\sin ^{2}\omega t+(\cos\omega t-1)^{2})=m\left( \frac{E_{x}}{B_{z}} \right)^{2}(1-\cos\omega t)
$$
so oscillates with cyclotron frequency.

If we drop the first assumption then as with only magnetic field, we simply get the cycloid receding at a constant speed. If we drop the second, there is an additional constant acceleration along the z-dir as well.