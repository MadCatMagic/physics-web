---
tags:
  - "#elecmag/electric-multipoles"
date-created: 2026-01-26
template-version: m.0
---
These consist of a set of charges $q$ such that the total charge is zero, and they are at a fixed small separation from each other. There are different possible configurations for higher order multipoles, but from a distance they are indistinguishable. 

In general, for an $n$-pole, (dipole is $n=2$) there will be a maximum of $2n$ particles, and $V\propto r^{-n}$, so $E\propto r^{-(n+1)}$.

For $n$ charges $q_{i}$, with distances $r_{i}$ from the origin and considering potential at a point $\vec{r}$, we find
$$
\begin{align}
V(\vec{r}) & =\frac{1}{4\pi\epsilon_{0}} \sum_{i=1}^{n} \frac{q_{i}}{|\vec{r}-\vec{r}_{i}|} \\
 & \approx \frac{1}{4\pi\epsilon_{0}}\left( \underbrace{ \sum_{i=1}^{n} \frac{q_{i}}{r} }_{ \text{monopole} }+\underbrace{ \sum_{i=1}^{n} \frac{q_{i}r_{i}\cos\theta_{i}}{r^{2}} }_{ \text{dipole} }+\underbrace{ \sum_{i=1}^{n} \frac{q_{i}r_{i}^{2}}{r^{3}} \frac{1}{2}(3\cos ^{2}\theta-1) }_{ \text{quadrupole} }+\dots  \right)
\end{align}
$$
which shows the different $r$ dependencies.
### Dipole
#elecmag/electric-dipole 
In this case there is only one configuration, a $q$ and $-q$ charge at a distance $d$. The potential of a dipole at $r\gg d$ is
$$
V=\frac{qd\cos\theta}{4\pi\epsilon_{0}r^{2}}=\frac{\vec{p}\cdot \hat{r}}{4\pi\epsilon_{0}r^{2}}
$$
where we have defined the **electric dipole moment** as $\vec{p}=q\vec{d}$ where $\vec{d}$ is the vector from one charge to the other.

Then using $\vec{E}=-\nabla V$ we can find that, in spherical coordinates,
$$
\begin{align}
E_{r} & =\frac{2qd\cos\theta}{4\pi\epsilon_{0}r^{3}}=\frac{\vec{p}\cdot \hat{r}}{2\pi\epsilon_{0}r^{3}} \\
E_{\theta} & =\frac{qd\sin\theta}{4\pi\epsilon_{0}r^{3}}=\frac{|\vec{p}\times \hat{r}|}{4\pi\epsilon_{0}r^{3}}
\end{align}
$$
#### External field acting on dipole
If we have an external field $\vec{E}_{\text{ext}}$ that is acting on the dipole, it will exert a torque on the dipole. This turns out to be (assuming that the dipole has no effect on $\vec{E}$)
$$
\vec{T}=\vec{p}\times \vec{E}_{\text{ext}}
$$
since the dipole is symmetric there is no translational force.

If we then find the potential energy as the work done to rotate the dipole to some angle $\theta$ from $\theta_{0}$ (taken to be $\frac{\pi}{2}$ here so there is no constant term) we get
$$
U=-\vec{p}\cdot \vec{E}_{\text{ext}}
$$
this can also be found by just finding the potential of both particles in the electric field (excluding their effect on one another).
### Quadrupole
#elecmag/electric-quadrupole 
In this case, there are two valid setups that are indistinguishable from a distance - two $+q$ and two $q-$ arranged in a square symmetrically with diameter $a$; or two $-q$ separated by $a$ with a $2q$ halfway between them. In either case, the potential for $r\gg d$ is
$$
V=\frac{qa^{2}}{4\pi\epsilon_{0}r^{3}}(1-3\cos ^{2}\theta)
$$
