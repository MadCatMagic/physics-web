---
tags:
  - calc/taylor-series
date-created: 2026-04-01
template-version: m.0
---
[[Calculus]]
[[Partial Differentiation]]

**Taylor's theorem** states we may write the equality
$$
f(a+h)=f(a)+hf'(a)+\frac{h^{2}}{2!}f''(a)+\dots+\frac{h^{n-1}}{(n-1)!}f^{(n-1)}(a)+R_{n}(h)
$$
where the *remainder* of the approximation is given by
$$
R_{n}(h)=\frac{h^n}{n!}f^{(n)}(\zeta),\quad \zeta \in[a,a+h]
$$
given that the function is $n$ times differentiable, and therefore continuous on the interval being considered. Setting $x=a+h$ yields the more conventional approximation around a point $a$:
$$
f(x)=f(a)+(x-a)f'(a)+\frac{(x-a)^{2}}{2!}f''(a)+\dots+\frac{(x-a)^{n-1}}{(n-1)!}f^{n-1}(a)+\frac{(x-a)^{n}}{n!}f^{(n)}(\zeta)
$$
 #calc/maclaurin-series 
Taylor series around x=0 are Maclaurin series.
### In 2 dimensions
$$
f(x,y)=\sum_{n=0}^{\infty} \frac{1}{n!}\left[ \left( \Delta x\frac{ \partial  }{ \partial x } +\Delta y\frac{ \partial  }{ \partial y }  \right)^{n}f(x,y) \right]_{x_{0},y_{0}}
$$
where $\Delta x=x-x_{0}$, $\Delta y=y-y_{0}$ and the partial derivatives only operate on $f(x,y)$, not $\Delta x$ or $\Delta y$.
### General case
For $f:U\to \mathbb{R}$ where $U\subset \mathbb{R}^{n}$ is an [[Topology#Open sets|open set]] we can use multi-index notation to write the full expansion as
$$
f(\mathbf{x}+\boldsymbol{\xi})=\sum_{|K|\leq \kappa}\frac{ \partial^{K}f(\mathbf{x}) }{ K! } \boldsymbol{\xi}^{K}+\mathcal{O} (|\boldsymbol{\xi}|^{\kappa+1})
$$
where we have a set of indices $K=(k_{1},\dots,k_{n})$ for which we define exponentiation $\mathbf{x}^{K}=x_{1}^{k_{1}}x_{2}^{k_{2}}\dots x_{n}^{k_{n}}$ and $K! =k_{1}!k_{2}!\dots k_{n}!$ so the total degree of any particular term is $|K|=k_{1}+k_{2}+\dots+k_{n}$. 

Writing this out explicitly for $\kappa=2$ yields
$$
\begin{align}
f(\mathbf{x}+\boldsymbol{\xi}) & =f(\mathbf{x})+\sum_{i=1}^{n} \partial_{i}f(\mathbf{x})\xi_{i}+\frac{1}{2}\sum_{i,j=1}^{n} \partial_{i}\partial_{j}f(\mathbf{x})\xi_{i}\xi_{j}+\mathcal{O} (|\boldsymbol{\xi}|^{3}) \\
 & =f(\mathbf{x})+\nabla f(\mathbf{x})\cdot \boldsymbol{\xi}+\frac{1}{2}\boldsymbol{\xi}^{T}H_{f}(\mathbf{x})\boldsymbol{\xi}+\mathcal{O} (|\boldsymbol{\xi}|^{3})
\end{align}
$$
where we are expressing in terms of the [[Gradient]] and the [[Hesse matrix]] of $f$ at $\mathbf{x}$.