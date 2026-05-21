---
tags:
  - calc/stokes-theorem
date-created: 2026-04-02
template-version: m.0
---
[[Vector Calculus]]
[[Curl]]

This is the fundamental theorem for Curls. For the usual $n=3$ case, we have
$$
\int_{S}\nabla \times A\cdot d\mathbf{S}=\int_{\partial S}A\cdot dx
$$
note that this converts a surface integral into a curve integral around the boundary $\partial S$ of that surface. $d\mathbf{S}=\hat{n}\,d\sigma$ as with [[Divergence theorem]]. A friendlier way to write this would be
$$
\int_{\mathcal{S} }(\nabla \times \mathbf{v})\cdot d\mathbf{a}=\oint_{\mathcal{P} }\mathbf{v}\cdot d\mathbf{l}
$$
this can be thought of as measuring the total flow through $S$ by considering how much flow is 'curling' through $S$ - that is, around $\partial S$.