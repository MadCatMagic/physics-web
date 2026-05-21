---
tags:
  - circuits/capacitor
date-created: 2026-02-03
template-version: m.0
---
A capacitor with capacitance $C$ has the following relations:
- parallel plate capacitance is given by $C=\frac{\epsilon A}{D}$ for dielectric constant $\epsilon$, area of plates $A$ and separation $d$.
- stores charge according to $Q=CV$ which implies $I=C \frac{dV}{dt}$ for use in KCL. 
- capacitors combine capacitance in the opposite way to resistors
- [[Complex Impedance]] is given by $Z=\frac{1}{i\omega C}$
- Energy stored in capacitor is $E=\frac{1}{2} \frac{Q^{2}}{C}=\frac{1}{2}CV^{2}=\frac{1}{2}QV$

In more detail for different types of capacitor (the results in question can be found from [[Electromagnetism#Guass's law]]):
#### Parallel plate capacitor
Is the simplest, has
$$
E=\frac{Q}{\epsilon_{0}A}
$$
in between the plates, and
$$
V=\frac{Qd}{\epsilon_{0}A}
$$
for the potential. It then has the result above of $C=\frac{\epsilon_{0}A}{d}$ for capacitance.
#### Cylindrical capacitor
For an inner radius $a$ and outer radius $b$, we have
$$
\vec{E}=\frac{Q}{2\pi\epsilon_{0}rl}\hat{r}
$$
where we assume $l\gg a,b,r$, for $a\leq r\leq b$. Also,
$$
V=\frac{Q}{2\pi\epsilon_{0}l}\ln \frac{b}{a}
$$
and the capacitance is given in terms of $C'=C /l$ capacitance per unit length as
$$
C=\frac{2\pi\epsilon_{0}}{\ln \frac{b}{a}}
$$
#### Spherical capacitor
Using the same inner/outer radii, we find
$$
\vec{E}=\frac{Q}{4\pi\epsilon_{0}r^{2}}\hat{r}
$$
for $a\leq r\leq b$ and then
$$
V=\frac{Q}{4\pi\epsilon_{0}}\left( \frac{1}{a}-\frac{1}{b} \right)
$$
so the capacitance is given by
$$
C=4\pi\epsilon_{0} \frac{ab}{b-a}
$$
Note that if $b\to \infty$, $C\to 4\pi\epsilon_{0}a$ so a charged sphere still has a capacitance.
### Energy and forces
Capacitors obey energy conservation equation
$$
dU_{C}=dU_{B}+dU_{M}
$$
for the energy stored in the capacitor, the energy supplied by the battery, and the mechanical work done in moving the plates. Hence the force between the plates is
$$
F=-\frac{dU_{M}}{dx}=\frac{dU_{B}}{dx}-\frac{dU_{C}}{dx}
$$
and the energy is the integral of the force w.r.t. distance as expected. This can be evaluated under any initial conditions using $U_{C}= \frac{1}{2}Q^{2} /C$ or equivalent and $\frac{dU_{B}}{dt}=P=IV=\frac{dQ}{dt}V$ where $V=Q /C$. [[Lecture 2026-02-03 10am.excalidraw|(some more details)]]. 

Note that while work is done to pull the plates apart (for constant V case), the energy stored in the capacitor decreases - this is because work is being done on the battery so energy is transferred to the battery both from the mechanical work and the energy stored in the capacitor.