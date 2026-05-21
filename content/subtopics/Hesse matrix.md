---
tags:
  - calc/hesse-matrix
date-created: 2026-04-01
template-version: m.0
---
[[Vector Calculus]]

The Hesse matrix of a function $f:U\to \mathbb{R}$ with $U\in \mathbb{R}^{n}$ is given as
$$
H_{f}=\begin{pmatrix}
\partial^{2}_{1}f & \partial_{1}\partial_{2}f & \dots & \partial_{1}\partial_{n}f \\
\partial_{2}\partial_{1}f & \partial_{2}^{2}f & \dots & \partial_{2}\partial_{n}f \\
\vdots & \vdots & \ddots & \vdots \\
\partial_{n}\partial_{1}f & \partial_{n}\partial_{2}f & \dots & \partial_{n}^{2}f
\end{pmatrix}
$$
so it describes the local curvature of the function, and contains all the second partial derivatives. If all the partial derivatives are continuous then by Clairaut's theorem, the matrix is symmetric. 

We in particular have the relation to the [[Jacobi matrix]] 
$$
H_{f}=(D_{\nabla f})^{T}
$$