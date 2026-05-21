---
tags:
  - calc/partial-diff/exact-inexact-differentials
  - calc/ODE/1st-order-exact-differential
date-created: 2025-12-30
template-version: m.0
---
[[Ordinary Differential Equations]]
[[Partial Differentiation]]
#### ODE phrasing
For an [[Ordinary Differential Equations|ODE]] in symmetric form $P(x,y)dx+Q(x,y)dy=0$, if there exists a *potential function* $\Phi(x,y)$ s.t. 
$$
\frac{ \partial \Phi }{ \partial x } =P(x,y),\quad \frac{ \partial \Phi }{ \partial y } =Q(x,y)
$$
the ODE is exact and $\Phi(x,y)=C$ is the solution.
#### Differential phrasing
A [[Partial Differentiation#Totals|differential]] $df=A(x,y)dx+B(x,y)dy$ is exact iff
$$
\frac{ \partial A }{ \partial y } =\frac{ \partial B }{ \partial x } 
$$
otherwise it is inexact - this is due to [[Partial Differentiation#Clairaut's theorem|Clairaut's theorem]] (the second derivatives must be equal, regardless of order of differentiation). (Works as expected for longer differentials - every pair of $\frac{ \partial g_{i} }{ \partial x_{j} }=\frac{ \partial g_{j} }{ \partial x_{i} }$ must hold true) This is also the condition for the ODE phrasing.
### Integrating factor
#calc/ODE/1st-order-integrating-factor 
If there is a function $\Lambda(x,y)$ that when multiplied by the ODE makes it exact, then this is the **integrating factor**.
So, $P'=\Lambda P$ and $Q'=\Lambda Q$ and our condition is
$$
\frac{ \partial (\Lambda P) }{ \partial y } =\frac{ \partial (\Lambda Q) }{ \partial x } \implies Q \frac{ \partial \Lambda }{ \partial x } -P\frac{ \partial \Lambda }{ \partial y } =\Lambda\left( \frac{ \partial P }{ \partial y } -\frac{ \partial Q }{ \partial x }  \right)
$$
At this point we must choose whether $\Lambda$ is a function of only $x$ or only $y$ - otherwise this is unhelpful. In the $x$ case, this means $\frac{ \partial \Lambda }{ \partial y }=0$ so we get
$$
\frac{1}{\Lambda} {d\Lambda}=\frac{1}{Q}\left( \frac{ \partial P }{ \partial y } -\frac{ \partial Q }{ \partial x }  \right)dx
$$
so
$$
\Lambda(x)=\exp\left( \int \frac{1}{Q}\left( \frac{ \partial P }{ \partial y } -\frac{ \partial Q }{ \partial x }  \right) \, dx  \right)
$$
is the integrating factor. Similarly if we picked the $y$ case we would would
$$
\Lambda(y)=\exp\left( \int \frac{1}{P}\left( \frac{ \partial Q }{ \partial x } -\frac{ \partial P }{ \partial y }  \right) \, dy  \right)
$$
After multiplying by $\Lambda$, solve as you would an exact differential.
#### Special case (Linear 1st order)
#calc/ODE/1st-order-linear 
The traditional special case is where
$$
y'+a(t)y=f(t)
$$
in which case we find that, using the above method,
$$
\Lambda(t)=\exp\left( \int a(t) \, dt  \right)
$$
and then the solution is
$$
y\Lambda(t)=\int \Lambda(t)f(t) \, dt+C 
$$