---
tags:
  - elecmag/gauss-law
date-created: 2026-03-17
template-version: m.0
---
[[Maxwell's equations]]
[[Divergence theorem]] - these are just specific cases

Both Gauss's law statements describe properties about the source of each field - for electric fields, that charges are where field lines originate; and for magnetic fields, that there are no magnetic charges. They are also both Maxwell equations.
### For electric fields
Gauss's law states that for a closed surface enclosing a charge $Q$,
$$
\oint_{S}\vec{E}\cdot d\vec{a}=\frac{Q}{\epsilon_{0}}
$$
where $\vec{E}$ is the electric field at the surface point being considered, and $d\vec{a}$ is the vector normal to the surface whose value is the infinitesimal area $dA$. Hence
- If the field is known for a surface the total charge enclosed can be found;
- If there is a surface of constant $\vec{E}\cdot d\vec{a}$ then the field can be found by factoring out to get $\oint \vec{E}\cdot d\vec{a}=\vec{E}\cdot \oint d\vec{a}$. Works well for symmetrical cases.

Using the divergence theorem we can rewrite this in alternate differential forms of:
$$
\int_{\mathcal{V} }\nabla\cdot \vec{E}\,d\mathcal{V} =\frac{1}{\epsilon_{0}}\int_{\mathcal{V} }\rho\,d\mathcal{V} 
$$
for any arbitrary volume, or even simpler:
$$
\nabla\cdot \vec{E}=\frac{\rho}{\epsilon_{0}}
$$
#### Proof-ish
We begin by just considering a point charge. This proof relies on the fact that the infinitesimal flux #elecmag/electric-field-flux $d\Phi=\vec{E}\cdot d\vec{a}=\vec{E}\cdot d\vec{a}'$ where the primed $d\vec{a}'$ represents the surface area projected onto a sphere at the same distance as $d\vec{a}$. Hence
$$
d\Phi=\underbrace{ \left( \frac{q}{4\pi\epsilon_{0}} \frac{\hat{r}}{r^{2}} \right) }_{ \vec{E} }\cdot\underbrace{ (r^{2}\sin\theta \,d\theta\,d\phi\,\hat{r}) }_{ d\vec{a}' }=\frac{q}{4\pi\epsilon_{0}}\cdot\underbrace{ \sin\theta \,d\theta\,d\phi }_{ d\Omega }
$$
so integrating over $S$ gives
$$
\oint_{S}\vec{E}\cdot d\vec{a}=\frac{q}{\epsilon_{0}}\int_{S'} \frac{d\Omega}{4\pi}=\frac{q}{\epsilon_{0}}
$$
this is then generalised by superposition to any charge distribution.
### For magnetic fields
States that
$$
\oint_{S}\vec{B}\cdot d\vec{a}=0 \iff \nabla\cdot \vec{B}=0
$$
so the [[Divergence]] of $\vec{B}$ is always zero. This is also the statement that *there are no magnetic monopoles*. Another way of thinking about this is that there is no net flux through a small unit volume in a magnetic field.