---
tags:
  - mech/conservative-force
  - mech/energy-conservation
  - "#mech/potential"
date-created: 2026-01-20
template-version: m.0
---
If a force is **conservative** then it satisfies all three of these equivalent properties:
- [[Curl]] of $\vec{F}=0$: $\nabla \times \vec{F}_{\text{cons}}=0$
- Work done under any closed path is zero: $W=\oint \vec{F}_{\text{cons}}\cdot d\vec{r}=0$ (this is actually sufficient)
- The force is the [[Gradient]] of a scalar potential $U(\vec{r})$: $\vec{F}_{\text{cons}}=-\nabla U(\vec{r})$

Note that if a [[Vector Calculus|field]] $F=\nabla U$ is conservative then we can write
$$
\partial_{j}A_{i}=\partial_{j}\partial_{i}f=\partial _{i}\partial_{j}f=\partial_{i}A_{j}\iff \partial_{i}A_{j}-\partial _{j}A_{i}=0
$$
which is just the statement that the curl of $F$ is zero. These properties are not sufficient for $A$ to be conservative, but usually they are good enough.

[[Central forces and orbits]] are always conservative.
### Work done by forces
There is zero net work done around any closed path, so we can find that
$$
W_{ab}=\int_{C}\vec{F}\cdot d\vec{r}=U(a)-U(b)
$$
*if and only if* the force is conservative. This fact is sometimes called the *fundamental theorem of calculus for gradients*.

For any force though we also have the looser fact that
$$
W_{ab}=\frac{1}{2}mv_{a}^{2}-\frac{1}{2}mv_{b}^{2}
$$
At a potential maximum we say it is an unstable equilibrium, and for a potential minimum it is a stable equilibrium.