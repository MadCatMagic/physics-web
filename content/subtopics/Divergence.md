---
tags:
  - calc/divergence
date-created: 2026-04-02
template-version: m.0
---
[[Vector Calculus]]

Divergence $f=\nabla\cdot A$ represents the net flow of the vector field $A$ in and out of a given small volume around $\mathbf{x}$. Hence we have
$$
\text{div}\,A=\nabla \cdot A=\sum_{i=1}^{n} \frac{ \partial A_{i} }{ \partial x_{i} } \,\quad(\,\,=\partial_{i}A_{i})
$$
using [[Summation notation]] at the end. 

We can express the divergence in terms of the [[Jacobi matrix]] as so:
$$
\nabla\cdot A=\sum_{i}\partial_{i}A_{i}=\text{tr}(D_{A})
$$
so divergence is the trace of the Jacobi matrix.

The product rule for divergence is
$$
\nabla\cdot(fA) =(\nabla f)\cdot A+f(\nabla\cdot A) 
$$