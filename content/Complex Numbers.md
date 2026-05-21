---
tags:
  - complex
date-created: 2025-12-15
template-version: m.0
---
[[Physics]]
[[Complex Numbers L_MT1]]
[[Complex Functions L_TT1]]
### Complex numbers
Complex numbers $z=x+iy$ exist in the complex plane. We can consider this a specialization of $\mathbb{R}^{2}$ since $\mathbb{C}\cong\mathbb{R}^{2}$ so we can express 
$$
(x,y)=x\hat{e}_{1}+y\hat{e}_{2}=x+iy
$$
with the obvious multiplicative properties of the basis vectors such that
$$
(x_{1},y_{1})\times(x_{2},y_{2})=(x_{1}x_{2}-y_{1}y_{2},x_{1}y_{2}+x_{2}y_{1})
$$
We also have alternate forms of $z$ where we express in polar form:
$$
\begin{align}
z & =x+iy \\
 & =r(\cos\theta+i\sin\theta) \\
 & =re^{i\theta}
\end{align}
$$
Where we have
$$
r=\sqrt{ x^{2}+y^{2} },\ \tan \theta=\frac{y}{x}
$$
and
$$
x=r\cos\theta,\ y=r\sin\theta
$$
The form $z=re^{i\theta}$ is **Euler's formula**. #complex/eulers-formula Note that the argument of $z$, $\text{arg}\,z$ can be offset by a factor of $2\pi$ since angles are not unique. We can also derive a definition for a multi-valued logarithm using this like so:
$$
\ln z=\ln r+i(\theta+2\pi n)
$$
And we can also derive **De Moivre's formula** #complex/de-moivres-theorem 
$$
(\cos \theta+i\sin\theta)^{n}=\cos n\theta+i\sin n\theta
$$

We can take the **conjugate** of a complex number:
$$
z^{*}=x-iy\quad(\,=\bar{z}\,)
$$
which obeys certain properties like
$$
zz^{*}=|z|^{2}
$$
where $|z|=r$. This corresponds to a reflection across the $x$-axis in the argand plane. Notably, $z^{*}$ is independent of $z$, so if we have $z=x+iy$ we can re-express it in terms of the basis $\{ z,z^{*} \}$ by using:
$$
\begin{align}
x & =\frac{1}{2}(z+z^{*}) \\[1ex]
y & =\frac{1}{2}(z-z^{*})
\end{align}
$$

#### Argand plane and Riemann sphere
#complex/riemann-sphere 
Obviously this forms a 2d plane, and we can create a mapping which includes $\infty$ as a valid point on the complex plane by considering a unit sphere sitting on $(x,y)=0$ such that we represent $z$ by the point on the sphere whose tangent crosses the x-y plane at $z$ (and which intersects $(x,y)=0$). In this system, the point $(0,0,2)$ on the sphere maps to $\infty$ since it is tangent to every point at $\infty$. More specifically, if $z=X+iY$ and the cartesian coordinate on the sphere is $(x,y,z)$, we have
$$
(X,Y)=\left( \frac{2x}{2-z}, \frac{2y}{2-z} \right)
$$
and inverting this,
$$
(x,y,z)=\left( \frac{4X}{4+X^{2}+Y^{2}}, \frac{4Y}{4+X^{2}+Y^{2}}, 1+ \frac{-4+X^{2}+Y^{2}}{4+X^{2}+Y^{2}} \right)
$$
### Roots of polynomials
#complex/roots 
A polynomial of order $n$ has $n$ complex roots. Additionally in the special case $z^{n}-1=0$ we have that for roots $z_k$:
$$
\sum_{k=1}^{n} z_{k}=0,\ \ \prod_{k=1}^{n} z_{k}=(-1)^{n+1}
$$
### Curves
#complex/curves 
Complex curves are usually of the form
$$
f(z,z^{*})=c
$$
To solve them we usually write them in the form $x+iy$ and examine the cartesian form. Examples in notes.
### Complex functions
#complex/functions 
Are in general functions of the form
$$
\begin{align}
f & :(x,y)\mapsto(u,v) \\
\iff f & :\mathbb{C}\to \mathbb{C} \\
\iff f & =u(x,y)+iv(x,y)
\end{align}
$$
i.e. mapping from one complex space to another. However, when considering a general function in terms of the conjugate basis $f(z,\bar{z})$ we will mainly focus on functions of $z$ alone i.e. where
$$
\frac{ \partial f }{ \partial \bar{z} } =0
$$
which are **complex functions**.

#complex/holomorphic
We define that an $f(z)$ is **holomorphic** at $z_{0}$ if $\frac{df}{dz}]_{z_{0}}$ is well defined - no matter the direction we take the derivative, it will always give the same value. 
#complex/analytic
It happens that every holomorphic complex function is **analytic** as well, (and vice versa) which means that there exists a [[Taylor series]] power series representation around $z_{0}$ which converges to $f(z)$ for a given neighbourhood $N$ around $z_{0}$. Note that this means [[Laurent series]] only have non-zero principal parts when they are at a non-analytic point.
#complex/meromorphic
**Meromorphic** functions on some open subset $D\subset \mathbb{C}$ are holomorphic everywhere except at a set of *isolated* poles. Note this means that we can write any meromorphic function as the ratio of two holomorphic functions, where the poles are the zeros of the denominator.
#### Cauchy-Riemann conditions
#complex/cauchy-riemann-conditions 
To find a condition for a function to be holomorphic (and therefore analytic) we take the $x$ and $y$ directional derivatives and equate them. We write $f(x,y)=u(x,y)+iv(x,y)$ and expand like so:
$$
\begin{align}
\frac{df}{dz} & =\lim_{ \delta x \to 0 } \frac{f(x+\delta x,y)-f(x,y)}{\delta x} \\
 & =\lim_{ \delta x \to 0 } \frac{u(x+\delta x,y)+iv(x+\delta x,y)-u(x,y)-iv(x,y)}{\delta x} \\[1ex]
 & =\frac{ \partial u }{ \partial x } +i\frac{ \partial v }{ \partial x } 
\end{align}
$$
and similarly for in the y-dir, we divide by $i\delta y$ instead since it is an infinitesimal change in $i$-dir, to find
$$
\frac{df}{dz}=\frac{1}{i}\frac{ \partial u }{ \partial y } +\frac{ \partial v }{ \partial y } 
$$
equating these gives the **Cauchy-Riemann conditions**
$$
\begin{align}
\frac{ \partial u }{ \partial x }  & =\frac{ \partial v }{ \partial y }  \\
\frac{ \partial u }{ \partial y }  & =-\frac{ \partial v }{ \partial x } 
\end{align}
$$
which are necessary and sufficient conditions for $f$ to be complex differentiable (locally at least).

An important fact is that if $\frac{ \partial f }{ \partial \bar{z} }=0$ so is a function of $z$ only, then these conditions are satisfied (locally - so not at singularities) and so *complex functions are always differentiable*. Can be proven by expanding partial derivative using chain rule in terms of $x$, $y$ and using $(z,\bar{z})\to (x,y)$ conversion, recovers Cauchy-Riemann conditions. **this proof is really sus, find better one?**
#### [[Laplace's equation#Harmonic functions|Harmonic functions]]
It turns out that $u$, $v$ are always *harmonic* if they satisfy CR conditions. This means they satisfy Poisson's equation $\nabla^{2}f=0$.
#### Finding $f(z)$ from $u$ or $v$
If we have e.g. $v(x,y)=(x^{2}+y^{2})+y$, and the initial condition $f(0)=0$ then we can find $f(z)$ by one of two methods:
- Guessing, so we just note that $x^{2}-y^{2}=\mathrm{Re}(z^{2})$ and $y=\mathrm{Im}(z)$ so we guess $f=z+iz^{2}+C$ and with the initial condition we get $f=z+iz^{2}$ which is correct.
- More systematically by applying Cauchy-Riemann, so we have
$$
\frac{ \partial u }{ \partial x } =\frac{ \partial v }{ \partial y } =-2y+1
$$
so $u=-2xy+x+g(y)$ and then
$$
\frac{ \partial u }{ \partial y } =-\frac{ \partial v }{ \partial x } =-2x
$$
so $u=-2xy+h(x)$. Comparing these and applying the initial condition gives $f(z)=x-2xy+i(x^{2}-y^{2}+y)=z+iz^{2}$ again.
### [[Complex mappings]]
Includes *types of mappings*, *conformal mappings*, the *moebius transformation*.
### [[Singularities]]
Includes *removeable singularities*, *poles*, *essential singularities*. Specifically isolated singularities in this case.
### [[Laurent series]]
A basic generalisation of [[Taylor series]] to poles. If a function has an isolated singularity, then we can expand it at that point using a Laurent series.
### [[Branch points and cuts]]
Describes *branch points* and *branch cuts*… obviously, and their generalisation using *Riemann sheets*… sort of.
## Contour integrals
#complex/contour-integral
Complex integrals are called **contour integrals** and we have to define a path in the complex plane for them to follow. So for a closed (endpoints are equal) path $C_{1}$, and an open (endpoints are different) path $C_{2}$, we could integrate $f$ around them like so:
$$
\int_{C_{1}}f(z)\,dz\quad\text{or}\quad\oint_{C_{2}}f(z)\,dz
$$
Note that the path must not be self-intersecting. Hence we require a parametrisation similar to [[Vector Calculus#Curve integrals|curve integrals]]. Alternatively we can expand the function $f=u+iv$ into its real and imaginary part since
$$
\oint_{C}f(z)\,dz=\oint_{C}(u+iv)(dx+i\,dy)=\oint_{C}(u\,dx-v\,dy)+i\oint_{C}(v\,dx+u\,dy)
$$
which becomes identical to two curve integrals.

*The most applications of complex functions we have to do involve contour integrals - as a consequence many written notes have examples from the lecture.*
### Cauchy's theorem
#complex/cauchy-theorem
States that if $f(z)$ is analytic in a region $R$ enclosed by a contour $C$ then
$$
\oint_{C}f(z)\,dz=0
$$
We can prove this using [[Green's theorem]] which by direct application of the expanded form above gives
$$
\oint_{C}f(z)\,dz=\int_{R}\left( -\frac{ \partial u }{ \partial y } -\frac{ \partial v }{ \partial x } \right)\,dx\,dy+i \int_{R}\left( \frac{ \partial u }{ \partial x } -\frac{ \partial v }{ \partial y } \right)\,dx\,dy=0
$$
by Cauchy-Riemann conditions (since analytic on $R$).

One consequence of this is that we can deform a contour if $f(z)$ is analytic between the original and new contour without changing the value of the integral. [[Lecture 2026-05-07 12pm.excalidraw|shitty proof]].
### Cauchy's integral formula
#complex/cauchy-integral-formula
Supposing we have *analytic* $f(z)$ on a region $R$, with $C$ being a contour bounding $R$, then
$$
I=\oint_{C} \frac{f(z)}{z-a}\,dz=2\pi if(a)
$$
We can prove this by considering extending $C$ to include an infinitesimal circle around $a$, $z=a+\epsilon e^{i\theta}$ and then using Cauchy's theorem to find
$$
I=\int_{0}^{2\pi}d\theta\,f(a+\epsilon e^{i\theta}) \frac{\epsilon ie^{i\theta}}{\epsilon e^{i\theta}} \underset{\epsilon\to0}=i\int_{0}^{2\pi} f(a) \, d\theta =2\pi if(a)
$$
More generally,
$$
f^{(n)}(a)=\frac{d^{n}f}{dz^{n}}(a)=\frac{n!}{2\pi i}\oint_{C} \frac{f(z)}{(z-a)^{n+1}}\,dz
$$
for analytic $f(z)$ on $R$.
### Integration tricks
There are several important integration concepts in complex analysis:
#### [[Residue theorem]]
Describes *residues*, and the *Cauchy residue theorem*. A glorified integral trick.
#### [[Jordan's lemma]]
Gives an upper bound on the value of a common contour, which in the limit allows for computation of improper integrals on the real line.
#### [[Branch points and cuts]]
Specifically we can integrate around branch cuts in clever ways to evaluate more complex contour integrals.
