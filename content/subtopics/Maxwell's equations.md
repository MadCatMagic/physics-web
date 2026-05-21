---
tags:
  - elecmag/maxwell-equations
date-created: 2026-03-17
template-version: m.0
---
[[Electromagnetism]]

Concerns the most general expression of classical electromagnetism, specifically the four *Maxwell equations* listed below.
### [[Gauss's law]]
Are actually two of the Maxwell equations: $\nabla\cdot \vec{E}=\frac{\rho}{\epsilon_{0}}$ for E-fields, and for B-fields, (also the statement of no magnetic monopoles) $\nabla\cdot \vec{B}=0$.
### Ampere's Law
#elecmag/amperes-law 
Analogous to Gauss's law for electric fields, it states that
$$
\oint \vec{B}\cdot d\vec{l}=\mu_{0}I_{\text{encl}}
$$
**only for magnetostatics**, where we are integrating around an *amperian loop* and $I_{\text{encl}}$ is the total current passing through the surface whose boundary is the loop - we could also write $I_{\text{encl}}=\int_{S}\vec{J}\cdot d\vec{a}$. 

Similarly to Gauss's law, it is useful to find symmetries when evaluating this integral, and usually we just have a circular or straight (rectangular) loop. In differential form, this becomes
$$
\nabla \times \vec{B}=\mu_{0}\vec{J}
$$

#elecmag/displacement-current 
The *most general form* includes a **displacement current** term because in its current form, Ampere's law does not agree with charge conservation. However if we add a displacement current term we can fix that to get the most general form:
$$
\nabla \times \vec{B}=\mu_{0}\left( \vec{J}+\epsilon_{0} \frac{ \partial \vec{E} }{ \partial t }  \right)\iff \oint_{C} \vec{B}\cdot d\vec{l}=\mu_{0}\int_{S}\vec{J}\cdot d\vec{a}+\underbrace{ \mu_{0}\epsilon_{0}\int_{S}\frac{ \partial \vec{E} }{ \partial t } \cdot d\vec{a} }_{ \text{displacement current} }
$$
Hence time varying E-fields generate B-fields.
### Maxwell-Faraday equation
#elecmag/maxwell-faraday-equation
This states that
$$
\oint_{C}\vec{E}\cdot d\vec{l}=-\int_{S}\frac{ \partial \vec{B} }{ \partial t } \cdot d\vec{a} \iff \nabla \times \vec{E}=-\frac{ \partial \vec{B} }{ \partial t } 
$$
in both integral and differential form. This captures the effect of time-varying magnetic fields creating electric fields, but if we combine it with [[Motion in electromagnetic fields#Lorentz force law|lorentz force law]] we can derive the more general [[Electromagnetism#Faraday's law|Faraday's law]] which includes motional emf.
### Energy density 
#elecmag/energy-density 
The energy density in an E-field $u$ is given by
$$
u=\frac{1}{2}\epsilon_{0}E^{2}\implies U=\frac{1}{2}\epsilon_{0}\int _{\mathcal{V}}E^{2} \, d\mathcal{V}  
$$
where $U$ is then the total energy due to the E-field over all space ($\mathcal{V}=\mathbb{R}^{3}$).

Considering a B-field instead, we find the energy density $u$ as
$$
u=\frac{1}{2} \frac{B^{2}}{\mu_{0}}\implies U=\frac{1}{2\mu_{0}}\int_{\mathcal{V} }B^{2}\,d\mathcal{V} 
$$
where again $U$ is the total energy due to the B-field over all space.

Note that in both these cases we are required by the derivation to take the integral over all space otherwise we need an extra boundary term.
### Poynting vector
#elecmag/poynting-vector 
Summing the total energies above and differentiating w.r.t time, we can substitute in some Maxwell equations to find
$$
\frac{dU}{dt}=-\oint_{S}\left( \frac{1}{\mu_{0}}\vec{E}\times \vec{B} \right)\cdot d\vec{a}
$$
where the inner expression $\vec{N}=\frac{1}{\mu_{0}}\vec{E}\times \vec{B}$ is defined as the **Poynting vector** $\vec{N}$. It represents the power per unit area flowing through the surface bounded by $S$ and the direction of flow. Hence $[\vec{N}]=Wm^{-2}$.

For [[Electromagnetic wave]]s the intensity is the time average of $|\vec{N}|$ which using the plane wave formulation described in the link gives
$$
P=\langle |\vec{N}| \rangle =\frac{1}{\mu_{0}}E_{0}B_{0}\left( \frac{1}{2} \right)=\frac{1}{2\mu_{0}c}E_{0}^{2}
$$
