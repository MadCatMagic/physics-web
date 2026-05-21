---
tags:
  - calc/divergence-theorem
date-created: 2026-03-17
template-version: m.0
---
[[Vector Calculus]]
[[Divergence]]

AKA *Gauss's theorem*, *Green's theorem*
Allows the changing of a volume integral to a surface/boundary integral -
$$
\int_{M}\nabla\cdot A\,d^{n}\mathbf{x}=\int_{\partial M}A\cdot d\mathbf{S}
$$
for a compact set with smooth boundary $M$, where $\partial M$ is the boundary/surface of $M$ and $d\mathbf{S}=\hat{\mathbf{n}}\,d\sigma$ where $\hat{\mathbf{n}}$ is the outer unit normal vector to $\partial M$ and $d\sigma$ is the surface volume infinitesimal.

Application of this to electromagnetism is what gives us [[Gauss's law]]s.
### Three dimensions
In three dimensions, we could write this as
$$
\int_{\mathcal{V} }(\nabla\cdot \mathbf{v})\,d\tau=\oint_{\mathcal{S} }\mathbf{v}\cdot d\mathbf{a}
$$
where we are converting a volume integral into a surface integral. We can think that if the divergence represents flow then the total flow through a volume depends only on the net flow through its surface.
### Two dimensions
Considering that the RHS integral will be a one-dimensional integral but using the normal unit vector instead of the tangent vector, we can actually convert this to a regular curve integral to find
$$
\int_{M}\text{curl}(B)\,d^{2}\mathbf{x}=\int_{\partial M}B\cdot \hat{\tau}\,d\sigma=\int_{\partial M}B\cdot d\mathbf{x}
$$
where we can find this by defining $A_{i}=\epsilon_{ij}B_{j}$ for the original field $A$. $\hat{\tau}$ is the unit tangent vector so $A\cdot \hat{n}=B\cdot \hat{\tau}$.