---
tags:
  - calc/curl
date-created: 2026-04-02
template-version: m.0
---
[[Vector Calculus]]

The curl is a differentiable operator which is defined in three dimensions as
$$
\text{curl}\,A=\nabla \times A\iff(\nabla \times A)_{i}=\epsilon_{ijk}\partial_{j}A_{k}
$$
using [[Summation notation#Levi-civita tensor|levi-civita]] notation. Curl represents how much a vector field $A$ locally 'curls' around a given point $\mathbf{x}$, where as in [[Rotational Dynamics]], the resulting vector field $B$ points along the axis of 'curling' with a magnitude representing the amount of 'curling'.

We have the usual product rule identity:
$$
\nabla \times(fA)=(\nabla f)\times A+f(\nabla \times A)
$$
### General definition
The components of the general curl are labelled by two indices and are given by
$$
(\text{Curl}\,A)_{ij}=\frac{ \partial A_{j} }{ \partial x_{i} } -\frac{ \partial A_{i} }{ \partial x_{j} } =\partial_{i}A_{j}-\partial_{j}A_{i}
$$
this expression is anti-symmetric in $(ij)$ so we could think of it as an anti-symmetric $n\times n$ [[Linear Algebra#Matrices|matrix]], (although actually a [[Tensor]]). 

In specifically 2 dimensions, we have the curl being a scalar, so
$$
\text{curl}\,A=\partial_{1}A_{2}-\partial_{2}A_{1}=\epsilon_{ij}\partial_{i}A_{j}
$$
and in three dimensions we reduce to the above definition in three dimensions. 

We can express the general curl in terms of the [[Jacobi matrix]] as so:
$$
(\text{Curl}\,A)_{ij}=\partial_{i}A_{j}-\partial_{j}A_{i}=(D_{A})_{ji}-(D_{A})_{ij}\iff \text{Curl}\,A=(D_{A})^{T}-D_{A}
$$
so the curl is given by the anti-symmetric part of the Jacobi matrix.