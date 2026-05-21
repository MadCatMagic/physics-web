---
tags:
  - elecmag/magnetostatics
date-created: 2026-03-17
template-version: m.0
---
[[Electromagnetism#Magnetic fields]]

This is a simplified case where we make the assumptions of time-independent charge (so $\frac{ \partial \rho }{ \partial t }=0$) and time-independent currents (so $\frac{ \partial \vec{J} }{ \partial t }=0$ with $I=JA$) given charge, current densities $\rho$, $\vec{J}$.
#### Boundary conditions
Considering the magnetic field close to a current density $k$ surface,
- perpendicular components of $\vec{B}$ are continuous - in absence of any other field, $B_{\perp}=0$.
- parallel components of $\vec{B}$ are discontinuous by $\mu_{0}k$
- this is the *opposite* behaviour to electrostatics.
### Biot-Savart law
#elecmag/biot-savart-law 
Is the statement that the magnetic flux density $d\vec{B}$ generated due to a length of wire $d\vec{l}$ with current $I$ travelling through a distance $\vec{r}$ from the wire is given
$$
d\vec{B}=\mu_{0}I \frac{d\vec{l}\times \hat{r}}{4\pi r^{2}}
$$
so the total field at that point is
$$
\vec{B}=\mu_{0}\int \frac{\vec{I}\times \hat{r}}{4\pi r^{2}} \, dl=\frac{\mu_{0}I}{4\pi}\int \frac{d\vec{l}\times \hat{r}}{r^{2}}
$$
for a current through a linear wire. Naturally for current surfaces and volumes analogous expressions exist (although not for a discrete set of points due to assumption of constant current)
$$
\vec{B}=\mu_{0}\int _{\mathcal{S} } \frac{\vec{k}\times \hat{r}}{4\pi r^{2}} \, d\mathcal{S} =\mu_{0}\int _{\mathcal{V} } \frac{\vec{J}\times \hat{r}}{4\pi r^{2}}\,d\mathcal{V} 
$$
with $\vec{I}=\vec{J}\cdot d\vec{a}$ (current per unit area) and $\vec{k}=\frac{d\vec{I}}{dl_{\perp}}$ where $dl_{\perp}$ is parallel to flow (current per unit length).
### [[Magnetic Dipoles]]
Including *torque*, *stored energy* in dipole.
### [[Magnetic potential]]
Including *vector* and *scalar* potential.