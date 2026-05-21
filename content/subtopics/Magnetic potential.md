---
tags:
  - elecmag/magnetic-scalar-potential
  - elecmag/magnetic-vector-potential
date-created: 2026-03-17
template-version: m.0
---
[[Magnetostatics]]

There are multiple different ways of defining a potential function for magnetic fields, since magnetic fields are not always conservative so cannot always be simply represented by a scalar function potential.
### Vector potential
Is the value $\vec{A}$ such that
$$
\vec{B}=\nabla \times \vec{A}
$$
such an $\vec{A}$ always exists. Then by the properties of [[Vector Calculus]], we find that
$$
\nabla\cdot \vec{B}=\nabla\cdot(\nabla \times \vec{A})=0
$$
so divergence of $\vec{B}$ is zero as expected. Inserting into amperes law for magnetostatics:
$$
\nabla \times \vec{B}=\nabla(\nabla\cdot \vec{A})-\nabla^{2}\vec{A}=\mu_{0}\vec{J}
$$
we have a degree of freedom in $\vec{A}$ so by choosing $\nabla\cdot \vec{A}=0$ we get **Poisson's equations for magnetostatics**
$$
\nabla^{2}\vec{A}=-\mu_{0}\vec{J}
$$
One solution for this is in fact [[Electromagnetism#Biot-Savart law|biot-savart]]:
$$
\vec{A}=\frac{\mu_{0}}{4\pi}\int_{\mathcal{V}} \frac{\vec{J}}{|r-r'|}\,d\mathcal{V} 
$$
### Scalar potential
Is not as useful but is defined
$$
\vec{B}=-\mu_{0}\nabla V_{m} \iff V_{m}=-\frac{1}{\mu_{0}}\int_{A}^{B} \vec{B}\cdot d\vec{l} 
$$
so is pathway-dependent and hence not single valued because $\vec{B}$ is not conservative. It can be used sometimes in simply connected, current-free regions.