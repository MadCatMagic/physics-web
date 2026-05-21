---
tags:
  - calc
date-created: 2026-04-01
template-version: m.0
---
[[Calculus]]
[[Multivariate Calculus L_HT1]]

Principally the study of functions taking vector arguments, being vector valued, and integrating and differentiating such functions.
### Curve integrals
#calc/curve 
A continuous map $X:[a,b]\to \mathbb{R}^{n}$ is called a **curve**. If its endpoints are equal then it is *closed*. If it is differentiable then $\frac{dX}{dt}$ is the *tangent vector* and if $\frac{dX}{dt}\neq 0$ then the curve is *regular*.

#calc/curve-integral 
If we also have a vector field $A:\mathbb{R}^{n}\to \mathbb{R}^{n}$ then the curve integral of $A$ over $X$ is
$$
\int A\cdot d\mathbf{x}=\int_{a}^{b} dt\,A(\mathbf{x}(t))\cdot \frac{dX}{dt}(t)
$$
this represents finding the 'flow' in the direction of the curve. If we consider a re-parametrisation $\tilde{X}(s)=X(t(s))$ for a *diffeomorphic* (cont. diff, invertible, and inverse cont. diff as well) $t=t(s)$ with inverse $s=s(t)$ then
$$
\int_{s(a)}^{s(b)} A(\tilde{X}(s))\cdot \frac{d\tilde{X}}{ds}(s) \, ds =\int_{s(a)}^{s(b)} A(X(t(s)))\cdot \frac{dX}{dt}(t(s)) \frac{dt}{ds}(s) \, ds=\int_{a}^{b} A(X(t))\cdot \frac{dX}{dt}(t) \, dt  
$$
so the integral is invariant under a re-parametrisation as we would expected. However we have to note that if the re-parametrisation reverses the orientation of the curve, we would introduce and extra minus sign into the result. [[calculusHTlecturenotes.pdf#page=45&selection=313,0,313,44&color=important|calculusHTlecturenotes, p.44]] examples.
### Differential operators of vector calculus
- $F=\nabla f$ - [[Gradient]]
- $f=\nabla \cdot F$ - [[Divergence]]
- $\tilde{F}=\nabla \times F$ - [[Curl]]
We can combine these operations in certain ways. For example composing $\text{div}\,\circ\,\text{grad}$ gives the [[Laplacian]].

Some derivative forms of functions with vector arguments:
- [[Jacobi matrix]]
- [[Hesse matrix]]

Considering a vector field $\nabla f$ we know from [[Conservative forces]] that its curl must vanish, so
$$
\text{Curl}\,(\nabla f)=0
$$
Additionally we can in three dimensions consider that
$$
\nabla\cdot(\nabla \times A)=\partial_{i}(\nabla \times A)_{i}=\partial_{i}\epsilon_{ijk}\partial_{j}A_{k}=0
$$
where vanishing comes from anti-symmetry of $\epsilon$ and symmetry of derivatives. This means that we could find a vector field $B=\nabla \times A$ for which $A$ becomes the *vector potential*, for example [[Magnetic potential]]. A necessary condition for $B$ having a vector potential is therefore that $\nabla\cdot B=0$.

We also can introduce strange new notation, for example $(B\cdot \nabla)A$ is the directional derivative of $A$ in the $B$ direction, scaled by $B$.
#### Identities
$$
\begin{align}
\nabla\cdot(A\times B) & =B\cdot(\nabla \times A)-A\cdot(\nabla \times B) &\\[1ex]
\nabla \times(A\times B) & =(B\cdot \nabla)A+(\nabla\cdot B)A-(A\cdot \nabla)B-(\nabla\cdot A)B &\\[1ex]
\nabla \times(\nabla \times A) &=\nabla(\nabla\cdot A)-\nabla^{2}A &(*)\\[1ex]
\end{align}
$$
where important identities are starred. These identities are easy to prove using [[Summation notation]].
#### [[Poincaré's Lemma]]
Gives sufficient conditions for a vector or scalar potential to exists.
#### [[Helmholtz theorem]]
States that a vector field is uniquely determined (with some conditions) by its divergence and curl. Also, that any vector field $\mathbf{F}$ can be expressed as
$$
\mathbf{F}=-\nabla \phi+\nabla \times \mathbf{A}
$$
for scalar potential $\phi$ and vector potential $\mathbf{A}$.
### Integration in $\mathbb{R}^{n}$
We define the *support* of $f$ by
$$
\text{supp}(f)=\overline{\{ \mathbf{x}\in \mathbb{R}^{n}\mid f(x)\neq 0 \}}
$$
where the bar represents the [[Topology|closure]]. This effectively represents just the set on which $f$ is non-vanishing - $f$ has *compact support* if $\text{supp}(f)$ is compact. We also then have the *characteristic function* $\chi_{S}:\mathbb{R}^{n}\to \mathbb{R}$ of $S\subset \mathbb{R}^{n}$
$$
\chi_{S}(\mathbf{x})=\begin{cases}
1 & \text{for} & \mathbf{x}\in S \\
0 & \text{for} & \mathbf{x}\not \in S
\end{cases}
$$
#calc/riemann-integral 
We define the **Riemann integral** over $S$ as
$$
\int_{S}d^{n}\mathbf{x}\,f(\mathbf{x})=\int_{\mathbb{R}^{n}}d^{n}\mathbf{x}\,f(\mathbf{x})\chi_{S}(\mathbf{x})
$$
where RHS integral is defined in terms of boxes (see notes...). We can then define the volume of $S$ for which $\chi_{S}$ is Riemann integrable,
$$
\text{vol}(S)=\int_{\mathbb{R}^{n}}d^{n}\mathbf{x}\,\chi_{S}(\mathbf{x})=\int_{S}d^{n}\mathbf{x}
$$
this is also called the *Jordan measure* of $S$. We can then split up this integral into $n$ 1-dimensional integrals to be evaluated like so:
$$
\int_{S}d^{n}\mathbf{x}\,f(\mathbf{x})=\int_{a_{1}}^{b_{1}} dx_{1} \int_{a_{2}(x_{1})}^{b_{2}(x_{1})} dx_{2} \dots \int_{a_{n}(x_{1},\dots,x_{n-1})}^{b_{n}(x_{1},\dots,x_{n-1})} dx_{n}\,f(x_{1},\dots,x_{n})
$$
no matter what way we do this splitting up the result should always be the same.
#### Change of variables
If we have some diffeomorphism $X:V\to U$ and $f:U\to \mathbb{R}$ a bounded function with compact support. Then $f$ is Reimann integrable over $U$ iff $\mathbf{y}\mapsto f(X(\mathbf{y}))|\det(D_{X}(\mathbf{y}))|$ is Reimann integrable over $V$, in which case
$$
\int_{U}d^{n}\mathbf{x}\,f(\mathbf{x})=\int_{V}d^{n}\mathbf{y}\,|\det D_{X}(\mathbf{y})|\,f(X(\mathbf{y}))
$$
where we are taking the [[Jacobi matrix]] determinant representing the change of coordinate spaces. Symbolically,
$$
d^{n}\mathbf{x}=d^{n}\mathbf{y}\,\left|\det\left( \frac{ \partial \mathbf{x} }{ \partial \mathbf{y} }  \right)\right|
$$
## [[Manifolds]] in $\mathbb{R}^{n}$
Contains *zero locus*, *parametrisation*, *tangent space*, *hyper-surfaces*, *normal vectors*, *induced metric*.
### Integration of manifolds
#calc/manifold/integral
Defining the **integration measure** $d\sigma=\sqrt{ \det(g) }\,d^{k}t$, we find that integrating over the parameter space becomes a valid operation. Note that *importantly, this is equivalent to the change of variables Jacobian method from integration in $\mathbb{R}^{n}$*.

Rigorously, we define
$$
\int_{V\cap M}f\,d\sigma=\int_{U}d^{k}t\sqrt{ \det(g) }\,f(X(\mathbf{t}))
$$
for a $k$-dimensional manifold with parameters $\mathbf{t}=(t_{1},\dots,t_{k})^{T}$.

#calc/manifold/volume 
Also define the **volume** of a $k$-manifold as
$$
\text{vol}(M)=\int_{M}d\sigma
$$
analogously to with regular integration on $\mathbb{R}^{n}$.
#### Integrals over curves
For a curve $C\subset \mathbb{R}^n$ with parametrisation $X:[a,b]\to \mathbb{R}^{n}$ for $t\in[a,b]$ then the induced metric on the curve gives measure $d\sigma=\left\lvert  \frac{dX}{dt}  \right\rvert\, dt$ and we simply get
$$
\int_{C}f\,d\sigma=\int_{a}^{b}   dt\,\left\lvert  \frac{dX}{dt}  \right\rvert\,f(X(t)) 
$$
note this is slightly different from integrating a vector field along a curve as defined in standard curve integration. We can relate them though by defining $d\mathbf{x}=\boldsymbol{\tau}\,d\sigma$ where $\boldsymbol{\tau}=\frac{dX}{dt}\left\lvert  \frac{dX}{dt}  \right\rvert^{-1}$ are the unit tangent vectors to the curve, so if we let $f(X(t))=A(X(t))\cdot \boldsymbol{\tau}(t)$ we get the usual vector field integral
$$
\int_{C}A\cdot d\mathbf{x}=\int_{a}^{b} dt \,\frac{dX}{dt}\cdot A(X(t))
$$
#### Integral over surfaces in $\mathbb{R}^{3}$
This simple case just gives us that
$$
\sqrt{ \det(g) }=\sqrt{ \left\lvert  \frac{ \partial X }{ \partial t_{1} }   \right\rvert ^{2}\left\lvert  \frac{ \partial X }{ \partial t_{2} }   \right\rvert ^{2}-\left( \frac{ \partial X }{ \partial t_{1} } \cdot \frac{ \partial X }{ \partial t_{2} }  \right)^{2} }=\sqrt{ \left\lvert  \frac{ \partial X }{ \partial t_{1} } \times \frac{ \partial X }{ \partial t_{2} }   \right\rvert ^{2} }=|N|
$$
so $d\sigma=|N|\,dt_{1}\,dt_{2}$ where $N$ is the [[Manifolds#Hyper-surfaces and normal vectors|standard normal vector]] to the plane. But if we instead consider the zero locus of the function $f$, we can split it such that $f(x,y,h(x,y))=0$ for some function $h$, so we can then parametrise $M$ such that
$$
X(x,y)=\begin{pmatrix}
x \\
y \\
h(x,y)
\end{pmatrix}\implies \frac{ \partial X }{ \partial x } =\begin{pmatrix}
1 \\
0 \\
\frac{ \partial h }{ \partial x } 
\end{pmatrix},\quad\frac{ \partial X }{ \partial y } =\begin{pmatrix}
0 \\
1 \\
\frac{ \partial h }{ \partial y } 
\end{pmatrix}
$$
which leads directly to the induced metric and therefore measure of
$$
d\sigma=\sqrt{ 1+\left( \frac{ \partial h }{ \partial x }  \right)^{2}+\left( \frac{ \partial h }{ \partial y } \right) ^{2} }\,dx\,dy
$$
Rewriting this in terms of $f$, we can partially differentiate $f(x,y,h(x,y))$ with respect to $x$ and $y$ to eventually find that
$$
d\sigma=\left( \frac{|\nabla f|}{\left\lvert  \frac{ \partial f }{ \partial z }   \right\rvert } \right)_{z=h(x,y)}\,dx\,dy
$$
as the required measure. There are also more wishy washy ways of deriving this result. #todo 
#### Integrating vector fields over surfaces in $\mathbb{R}^{3}$
We define an analogous *vector measure* in the form
$$
d\mathbf{S}=\hat{n}\,d\sigma=N\,dt_{1}dt_{2}=\pm \frac{ \partial X }{ \partial t_{1} } \times \frac{ \partial X }{ \partial t_{2} } \,dt_{1}dt_{2}
$$
if $X$ is our chart for the manifold. If instead we have a zero locus $f$ we can use the previous result to just write that
$$
d\mathbf{S}=\hat{n}\,d\sigma=\pm \frac{\nabla f}{\left\lvert  \frac{ \partial f }{ \partial z }   \right\rvert }\,dx\,dy
$$
We call the vector field $\mathbf{A}$ integrable over an orientable surface $M$ if the scalar function $\mathbf{A}\cdot \hat{n}$ is integrable over $M$, and in this case we define the integral as
$$
\int_{M}\mathbf{A}\cdot d\mathbf{S}:=\int_{M}\mathbf{A}\cdot \hat{n}\,d\sigma
$$
Note that the surface must be orientable for $\hat{n}$ to be well defined, and the direction of $\hat{n}$ gives the orientation of the surface.

*skipping integration over hyper-surfaces in general*
### Transformation theorems
The trick here is that by applying the derivative operator to the integrand we can reduce the dimension of the integral.
- [[Divergence theorem]] (or Gauss's theorem): $k=n\to k=n-1$
- [[Stokes theorem]]: $k=2\to k=1$ for $n=3$ case
	- "general stokes theorem" allows dimension $n$, $k\to k-1$. *we don't care though*
- [[Green's theorem]] 2D stokes theorem - $k=2\to k=1$ for $n=2$ case.
