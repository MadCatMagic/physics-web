---
tags:
  - elecmag/laplaces-equation
date-created: 2026-05-02
template-version: m.0
---
[[Electrostatics]]
[[Complex Numbers]]

Is the partial differential equation
$$
\nabla^{2}f=0
$$
using the [[Laplacian]].
#### Uniqueness theorem
#elecmag/uniqueness-theorem 
States that the solution to Poisson's equation is uniquely determined in a volume $\mathcal{V}$ if $V$ is specified on the boundary surface $\mathcal{S}$, for a given charge distribution $\rho$. Proof in [[Lecture 2026-02-02 10am.excalidraw|notes]].
#### Harmonic functions
#calc/harmonic-function
It turns out that if $f=u+iv$ satisfies Cauchy-Riemann then
- $u$, $v$ are **harmonic functions**, which means they solve *Poisson's equation* $\nabla^{2}f=0$, specifically in 2D:
$$
\begin{align}
\nabla^{2}u=0\quad\text{and}\quad \nabla^{2}v=0
\end{align}
$$
We can proof this fact by direct application of Cauchy-Riemann and switching partial differentiation variable:
$$
\begin{align}
\frac{ \partial^{2} u }{ \partial x^2 }  &  =\frac{ \partial  }{ \partial x } \frac{ \partial v }{ \partial y } =\frac{ \partial  }{ \partial y } \frac{ \partial v }{ \partial x }  =-\frac{ \partial^{2} u }{ \partial y^2 }  \\
 & \implies \nabla^{2}u=\frac{ \partial^{2} u }{ \partial x^2 } +\frac{ \partial u }{ \partial y } =0 \\
\frac{ \partial^{2} v }{ \partial x^2 } & =-\frac{ \partial  }{ \partial x } \frac{ \partial u }{ \partial y } =-\frac{ \partial  }{ \partial y } \frac{ \partial u }{ \partial x } =-\frac{ \partial^{2} v }{ \partial y^2 }   \\
 & \implies \nabla^{2}v=\frac{ \partial^{2} v }{ \partial x^2 } +\frac{ \partial v }{ \partial y } =0 \\
\end{align}
$$
Therefore we can easily generate harmonic functions by finding the real and imaginary parts of $f(z)$. In fact, all harmonic functions defined on the plane are of this form. *Wikipedia*

Additionally, if we consider contours of the form
$$
\begin{align}
u(x,y) & =C_{1} \\
v(x,y) & =C_{2}
\end{align}
$$
then if they satisfy CR, the lines are always orthogonal to each other. We again prove this using CR, by letting the normal vectors to the lines be $n_{u}=\nabla u$, $n_{v}=\nabla v$ so their dot product is
$$
(\nabla u)\cdot(\nabla v)=\frac{ \partial u }{ \partial x } \frac{ \partial v }{ \partial x } +\frac{ \partial u }{ \partial y } \frac{ \partial v }{ \partial y } =-\frac{ \partial u }{ \partial x } \frac{ \partial u }{ \partial y } +\frac{ \partial u }{ \partial y } \frac{ \partial u }{ \partial x } =0
$$
so the lines must be orthogonal since they exist in 2D.
### Solving BVP with complex functions
#complex/boundary-value-problems
Since both parts of a complex function are harmonic, we could express some potential function $\Phi$ satisfying Poisson's equation as a part of a complex function, and matching the boundary conditions. Then we gain additional information about the corresponding lines that are perpendicular to every constant potential lines - these can be field lines or flow lines, etc.

*For example*, considering a conducting radius $R$ cylinder in a uniform electric field $\vec{E}=(E,0)$ then for large $x,y$ we know $f(z)\to-Ez$ since the constant field is the only significant part and $\vec{E}=-\nabla \Phi$. Given also that $\Phi=0$ along the cylinder, we can deduce a valid form for $f(z)$ as
$$
f(z)=-E\left( z-\frac{R^{2}}{z} \right)
$$
which satisfies the boundary condition (is pure imaginary on boundary), so
$$
\Phi=\mathrm{Re}(f)=-E\left( x-\frac{R^{2}x}{x^{2}+y^{2}} \right)
$$
and we can deduce also the electric field lines by finding $\mathrm{Im}(f)=C$.
#### Conformal transformations
Given analytic functions act as [[Complex Numbers#Conformal transformations|conformal transformations]] (with $f'(z)\neq0$) we can transform a more complex problem into a simpler one and retain the transformed coordinates being harmonic. This can be proven by expanding out $\nabla^{2}\Phi$ in terms of the chain rule, applying CR and using $|f'(z)|^{2}=(\partial_{x}u)^{2}+(\partial_{y}u)^{2}=(\partial_{x}v)^{2}+(\partial_{y}v)^{2}$ which eventually gives
$$
\nabla^{2}_{xy}\Phi=|f'(z)|^{2}\,\nabla^{2}_{uv}\Phi=0
$$
when transforming under conformal $f(z)$.

*For example*, supposing we have a plate on the $+x$ and $+y$ axes held at $\Phi=\Phi_{0}$ then we can transform this to a much simpler problem by applying $w=f(z)=z^{2}$ which is a conformal transformation (at $z\neq0$) so in the new coordinates we have
$$
\Phi=\Phi_{0}-\frac{\sigma}{\epsilon_{0}}v(x,y)
$$
so $f(w)=\Phi_{0}+i \frac{\sigma}{\epsilon_{0}}w$ and in original coordinates we have
$$
\Phi=\mathrm{Re}(f)=\mathrm{Re}\left( \Phi_{0}+i \frac{\sigma}{\epsilon_{0}}z^{2} \right)=\Phi_{0}-2 \frac{\sigma}{\epsilon_{0}}xy
$$
so the equipotentials are hyperbola in the upper left quadrant which makes sense. This makes a difficult BVP a lot simpler.