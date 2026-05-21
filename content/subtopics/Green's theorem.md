---
tags:
  - calc/greens-theorem
date-created: 2026-05-18
template-version: m.0
---
[[Vector Calculus]]

Also called *Green's theorem in a plane*. Is a 2D version of [[Stokes theorem]] (or a 2D version of [[Divergence theorem]], sources cannot agree?), and states that
$$
\oint_{\partial S}(A(x,y)\,dx+B(x,y)\,dy)=\int_{S}\left( \frac{ \partial B }{ \partial x } -\frac{ \partial A }{ \partial y }  \right)\,dx\,dy
$$
where $\partial S$ is a positively oriented, piecewise smooth, simple closed curve in a plane, and $S$ is the region bounded by $\partial S$ - $S$ is therefore simply connected. The path of integration along $C$ is counter clockwise.
### Simple proof
We can prove this by considering the following region $R$:
![[course/raw/illustrations.excalidraw.md#^clippedframe=5JqE3Qg7ARLimDRmuZfYA]]
We let $y=y_{1}(x)$ and $y=y_{2}(x)$ be parametrisations for $STU$ and $SVU$ respectively, so then
$$
\begin{align}
\int_{R}\frac{ \partial A }{ \partial y }\, dx\,dy &  =\int_{a}^{b} dx \int_{y_{1}(x)}^{y_{2}(x)}  dy \frac{ \partial A }{ \partial y }  \\
 & =\int_{a}^{b} dx\,[A(x,y_{2}(x))-A(x,y_{1}(x))]  \\
 & =-\int_{a}^{b} A(x,y_{1}(x)) \, dx -\int_{b}^{a} A(x,y_{2}(x)) \, dx =-\oint_{C} A\,dx
\end{align}
$$
we can do the exact same process on $TSV$ and $TUV$ to find
$$
\int_{R}\frac{ \partial B }{ \partial x } \,dx\,dy=\oint_{C}B\,dy
$$
then subtracting the two integrals gives us Green's theorem.
### Generalised case
We can generalised to multiply connected regions if we just take the line integral over all the distinct boundaries of the region, traversing all of them in the same positive direction (i.e. $S$ should always be on the left when looking top down at a boundary)
