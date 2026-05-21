---
tags:
  - elecmag/induction
date-created: 2026-03-17
template-version: m.0
---
[[Electromagnetism]]
[[Inductor]] - circuit component designed to utilise inductance.

Considering a wire moving at a velocity $\vec{v}$ through a perp $\vec{B}$ field (and wire direction $\hat{\epsilon}$ is perp to both), free charges in the wire experience a [[Motion in electromagnetic fields#Lorentz force law|lorentz force]] along the wire which causes an #elecmag/electromotive-force 
$$
\epsilon=\int_{C} \frac{dW}{q}=\int_{C} \frac{\vec{F}\cdot d\vec{l}}{q}=\int_{C}(\vec{v}\times \vec{B})\cdot d\vec{l}
$$
using Lorentz force $\vec{F}=q(\vec{v}\times \vec{B})$. $\epsilon$ is the **electromotive force** (is a potential difference, also called emf or electromotance sometimes).
#### Faraday's law
#elecmag/faradays-law 
Considering instead time-varying magnetic fields and "motional emf" due to the motion of a coil, we can derive **faraday's law** (aka *Faraday's flux rule*, or the *Faraday–Lenz law*)
$$
\epsilon=-\frac{d\Phi}{dt}
$$
which is *always true* in general. This is related to the [[Maxwell's equations#Maxwell-Faraday equation|Maxwell-Faraday equation]] but is distinct in that it accounts for motional emf as well as time-varying magnetic fields, of which the Maxwell-Faraday equation only accounts for the latter.

#elecmag/lenzs-law
Embedded in this is **Lenz's law** which effectively represents the minus sign in the equation and simply states that induces emf gives rise to a current whose magnetic field opposes the original change in magnetic flux that caused it.
#### Self-inductance
#elecmag/self-inductance 
Recalling the inductor relation $V=\frac{dI}{dt}L$ we can rewrite the self-inductance $L$ as
$$
L=\frac{\Phi}{I}=\frac{d\Phi}{dI}=-\frac{\epsilon}{\dot{I}}
$$
i.e. it is is the emf induced due to the changing current in an object, and $L$ depends only on the geometry of the system.
#### Mutual inductance
#elecmag/mutual-inductance 
We define the mutual inductance of two objects as $M=M_{12}=M_{21}=\frac{\Phi_{2}}{I_{1}}=\frac{\Phi_{1}}{I_{2}}$ is a purely geometric property of two wires and is mutual hence $M_{12}=M_{21}$ - this fact is *Neumann's theorem* #elecmag/neumanns-theorem and a short proof is as follows. Sometimes it is simpler to evaluate one than the other so this fact is useful.
##### Neumann's theorem proof
Consider two loops $C_{1}$ and $C_{2}$, the flux $\Phi_{2}$ through area of $C_{2}$ due to $I_{1}$ in $C_{1}$ is
$$
\Phi_{2}=\int \vec{B}_{1}\cdot d\vec{a}_{2}=\int(\nabla \times \vec{A}_{1})\cdot d\vec{a}_{2}=\oint_{C_{2}}\vec{A}_{1}\cdot d\vec{l}_{2}
$$
where $\vec{A}_{1}$ is [[Magnetic potential#Vector potential|vector potential]] of $\vec{B}_{1}$, and applying [[Stokes theorem]]. Using definition of vector potential from Biot-Savart, this becomes:
$$
\Phi_{2}=\frac{\mu_{0}I_{1}}{4\pi}\oint_{C_{1}}\oint_{C_{2}} \frac{d\vec{l}_{1}\cdot d\vec{l}_{2}}{r_{12}}
$$
so we get *Neumann's formula*:
$$
M_{12}=\frac{\mu_{0}}{4\pi}\oint_{C_{1}}\oint_{C_{2}} \frac{d\vec{l}_{1}\cdot d\vec{l}_{2}}{r_{12}}=\frac{\mu_{0}}{4\pi}\oint_{C_{2}}\oint_{C_{1}} \frac{d\vec{l}_{2}\cdot d\vec{l}_{1}}{r_{21}}=M_{21}
$$
hence $M_{12}=M_{21}$.
##### Relation between mutual and self inductances
In general it is true that
$$
M=k\sqrt{ L_{1}L_{2} },\quad k<1
$$
where $k$ is the **coefficient of coupling** #elecmag/coefficient-of-coupling - so the mutual inductance is proportional to the geometric mean of the self-inductances between two configurations.