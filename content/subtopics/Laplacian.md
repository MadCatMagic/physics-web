---
tags:
  - calc/laplacian
date-created: 2026-04-02
template-version: m.0
---
[[Vector Calculus]]

In arbitrary dimensions we can consider a scalar $f:\mathbb{R}^{n}\to \mathbb{R}$. Composing [[Divergence]] and [[Gradient]] gives the definition of the Laplacian, namely
$$
\nabla^{2}f=\Delta f=\nabla\cdot(\nabla f)=\sum_{i=1}^{n} \frac{ \partial^{2} f }{ \partial x_{i}^2 } 
$$
so we have the actual Laplacian is $\nabla^{2}=\Delta$ (giving the two most common symbol representations). This is used in many places for example [[Electrostatics#Poisson's and Laplace's equations|Poisson's and Laplace's equations]] in electromagnetism.
### Vector Laplacian
The Laplacian as defined above is $\nabla^{2}:\mathbb{R}\to \mathbb{R}$ but we can generalise this to vector fields, simply by defining the vector form as
$$
\nabla^{2}A=\begin{pmatrix}
\nabla^{2}A_{1} \\
\vdots \\
\nabla^{2}A_{n}
\end{pmatrix}=\sum_{i=1}^{n} \mathbf{e}_{i}\nabla^{2}A_{i}
$$
