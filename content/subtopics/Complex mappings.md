---
tags:
  - complex/mapping
date-created: 2026-05-19
template-version: m.0
---
[[Complex Numbers]]

For $f:(x,y)\to(u,v)$ these mappings are one-to-one iff the [[Jacobi matrix]] is non-singular where
$$
\begin{align}
|D_{f}| & =\left\lvert  \frac{ \partial u }{ \partial x } \frac{ \partial v }{ \partial y } -\frac{ \partial v }{ \partial x } \frac{ \partial u }{ \partial y }  \right\rvert \\
 & =\left\lvert  \left( \frac{ \partial u }{ \partial x }  \right)^{2}+\left( \frac{ \partial u }{ \partial y }  \right)^{2} \right\rvert \\
 & =\left\lvert  \left( \frac{ \partial v }{ \partial x }  \right)^{2}+\left( \frac{ \partial v }{ \partial y }  \right)^{2} \right\rvert
\end{align}
$$
from CR. Then considering the derivative of $f$, we have
$$
f'=\frac{df}{dz}=\frac{ \partial f }{ \partial x } \frac{ \partial x }{ \partial z } +\frac{ \partial f }{ \partial y } \frac{ \partial y }{ \partial z } 
$$
then converting using $z,\bar{z}$ basis and CR we get
$$
f'=\frac{ \partial u }{ \partial x } -i \frac{ \partial u }{ \partial y } 
$$
so
$$
|D_{f}|=|f'(z)|^{2}
$$
so the mapping is one to one if $f'(z)\neq0$.
### Types of mapping
Obviously we have the standard translation, scaling, etc. Rotations are done by applying $e^{i\theta}$ e.g. $f(z)=e^{i\theta}z$.
$f(z)=1/z$ is an inversion. All of these map the full plane to the full plane.

Several mappings map the full plane onto a part of the plane for example $f(z)=z^{1/n}$ maps onto the wedge with opening angle $2\pi/n$.
#### Moebius transformation
#complex/moebius-transformation
Is 
$$
f(z)=\frac{az+b}{cz+d}=e^{i\theta_{0}}\left( \frac{z-z_{0}}{z-\bar{z}_{0}} \right)
$$
which transforms the positive half-plane to a unit disc centred on $z_{0}$, where $\theta_{0}$ is the angle at which $-\infty$ and $\infty$ are mapped to. Hence it maps a non-compact object to a compact one.
#### Conformal transformations
#complex/conformal-transformation 
Are angle preserving. We could prove this by considering two points arbitrarily close to $z$ as
$$
\begin{align}
z_{1} & =z+\epsilon e^{i\theta_{1}} \\
z_{2} & =z+\epsilon e^{i\theta_{2}}
\end{align}
$$
so we can retrieve the angle between them as
$$
\frac{\delta z_{1}}{\delta z_{2}}=\frac{z_{1}-z}{z_{2}-z}=e^{i(\theta_{1}-\theta_{2})}=e^{i(\Delta\theta)}
$$
transforming these under $f$ and Taylor expanding (allowed since $f$ is assumed analytic) we get
$$
\frac{\delta z_{1}'}{\delta z_{2}'}=\frac{f'(z)\epsilon e^{i\theta_{1}}}{f'(z)\epsilon e^{i\theta_{2}}}\overset ?= e^{i\Delta\theta}
$$
so we see that the angle is preserved IF $f'(z)\neq 0$ and is defined. Therefore *f is conformal if $f'(z)\neq 0$ and f is analytic*.