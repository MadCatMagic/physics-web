---
tags:
  - elecmag/electrostatics
date-created: 2026-03-17
template-version: m.0
---
[[Electromagnetism]]

Electrostatics specifically denotes the regime when we consider constant, static charge density, and no magnetic fields.
### [[Electric Multipoles]]
Including *general multipoles*, *dipoles*, *quadrupoles*.
### Poisson's and [[Laplace's equation]]s
#elecmag/poissons-equation #elecmag/laplaces-equation 
These follow directly from the differential form of Guass's equation. *Poisson's equation* is the relation
$$
\nabla^{2}V(\vec{r})=-\frac{\rho(\vec{r})}{\epsilon_{0}}
$$
where $\rho(\vec{r})$ is the charge density at $\vec{r}$, and $\nabla^{2}$ is the [[Laplacian]]. In the special case of $\rho=0$ this reduces to *Laplace's equation*:
$$
\nabla^{2}V=0
$$
#### Method of images
#elecmag/method-of-images 
Utilising the uniqueness theorem, if we can find any charge configuration outside a region $\mathcal{V}$ that replicates the boundary conditions of the region then the potential is identical in $\mathcal{V}$ by uniqueness theorem. Note that outside $\mathcal{V}$, the potential and forces and field and charges can be doing whatever the hell they like but so long as it is identical at the boundary (and same charge distribution in $\mathcal{V}$), it is sufficient.
### Conductors
#elecmag/conductors 
Are when one or more electrons per atom in the material are free to move. This results **in statics** with the following effects:
1. $\vec{E}=0$ inside a conductor - free charge moves to surface until internal electric field is cancelled.
2. $\rho=0$ inside a conductor - from Guass's law, no charge contained.
3. Hence any net charge is at the surface.
4. A conductor is an equipotential then.
5. At the surface of a conductor, $\vec{E}\parallel d\vec{A}$ or the field is perpendicular to the surface - if it wasn't, charges would move until it was.

This results in applied fields to a conductor being cancelled by an internal field.

Additionally, we have the facts that, for a charged surface
- components of the field perpendicular to the surface are discontinuous at the surface by $\sigma /\epsilon_{0}$;
- parallel components are continuous across the surface;
- and potential is continuous across the surface.

This leads to the important fact that if we know the field $\vec{E}$ at a point on a conductors surface, then using Guass's law we can find the charge density at that point on the surface as
$$
\sigma=\epsilon_{0}E_{\perp}=-\epsilon_{0}\frac{ \partial V }{ \partial z }\biggr\rvert_{z=0} 
$$
