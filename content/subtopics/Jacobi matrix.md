---
tags:
  - "#calc/jacobi-matrix"
  - calc/jacobian
date-created: 2026-04-01
template-version: m.0
---
[[Vector Calculus]]

$f:U\to \mathbb{R}^{m},\, U\in \mathbb{R}^{n}$ is totally differentiable at $\mathbf{x}\in U$ if there exists a matrix $A$ s.t.
$$
f(\mathbf{x}+\boldsymbol{\epsilon})=f(\mathbf{x})+A\boldsymbol{\epsilon}+O(|\boldsymbol{\epsilon}|^{2})
$$
for all $\boldsymbol{\epsilon}\in \mathbb{R}^{n}$ in a small ball $B_{r}(0)$. This matrix $A$ is called the total derivative or **Jacobi matrix**. It is also denoted $D_{f}(\mathbf{x})$. This form has several properties:
- $Df$ is linear
- $Df$ is given by the following matrix - it represents all the partial derivatives of all the components of the function $f_{i}$:
$$D_{f}(\mathbf{x})=\begin{pmatrix}
\partial_{1}f_{1} & \dots & \partial_{n}f_{1} \\
\vdots & \ddots & \vdots \\
\partial_{1}f_{m} & \dots & \partial_{n}f_{m}
\end{pmatrix}$$
- Another way of expressing $D_{f}$ more explicitly is
$$
D_{f}(\mathbf{x})=\frac{ \partial (f_{1},\dots ,f_{m}) }{ \partial (x_{1},\dots,x_{n}) } (\mathbf{x})
$$
#### m=1 case
In this case, for a scalar function, the Jacobi matrix reduces to the [[Gradient]] $\nabla$:
$$
D_{f}(\mathbf{x})=\left( \frac{ \partial f }{ \partial x_{1} },\dots,\frac{ \partial f }{ \partial x_{n} }   \right)=\nabla f(\mathbf{x})
$$
### Jacobian
The Jacobian is the determinant of the Jacobi matrix
$$
\det(D_{f}(\mathbf{x}))
$$