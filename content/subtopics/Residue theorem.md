---
tags:
  - complex/cauchy-residue-theorem
  - "#complex/residue"
  - complex/contour-integral
date-created: 2026-05-18
template-version: m.0
---
[[Complex Numbers]]

### Residue
The **residue** is only defined for the *first order* pole part of a pole and if we have
$$
f(z)=\frac{c}{z-a}g(z)
$$
where $g(z)$ has no multiplicative constants, then
$$
\text{Res}[f,a]=c
$$
gives the residue. Note we can also define this in terms of the [[Laurent series]] since if the coefficients are $a_{n}$, then $\text{Res}[f,z_{0}]=a_{-1}$. **Note more so** that by this more rigorous definition, an essential singularity can also have a residue and hence will also work with.

We can find the residue either by direct computation of the Laurent series, or by taking
$$
\lim_{ z \to z_{0} } (z-z_{0})f(z)
$$
if this limit is defined, then it is equal to the residue. If not, further computation is required.
### Residue theorem
Consider the integral
$$
\oint_{C}(z-a)^{n}\,dz,\qquad n\in \mathbb{Z}
$$
where $C$ contains $a$. If we let $C$ be a circle with radius $\epsilon$ around $a$ then
$$
\oint_{C}(z-a)^{n}\,dz=i\int_{0}^{2\pi} \epsilon^{n+1}e^{i(n+1)\theta} \, d\theta=
\begin{cases}
0 & \text{if} & n\neq-1 \\
2\pi i & \text{if} & n=-1
\end{cases} 
$$
so if we have a function $f(z)$ with a [[Laurent series]] expansion then
$$
\oint_{C}f(z)\,dz=\sum_{n=-p}^{\infty} a_{n}\oint_{C}(z-a)^{n}\,dz=2\pi ia_{-1}
$$
so *the contour integral around a loop containing a pole is given by the residue of the pole to a constant factor of $2\pi i$*. 

More generally, for a contour $C$ enclosing a region $R$ that is *meromorphic* under $f(z)$, we have
$$
\oint_{C}f(z)\,dz=2\pi i\sum_{k=1}^{N} \text{Res}(f,w_{k})
$$
where there are $N$ poles (or essential singularities since they also have a residue) at points $w_{k}$. This is **Cauchy's residue theorem**. We can use this to cleverly evaluate many integrals by finding some contour and applying residue theorem. Note that this assumes that the curve is *oriented simple curve* i.e. it is not self-intersecting, all points have a *winding number* of 1 if they are enclosed, 0 otherwise.

The standard integral examples all involve an integral on the real line (usually for $x \in(-\infty,\infty)$) so we extend the integral to a contour which is a half circle on the complex plane, and then the diameter of the half circle being on the real line. We then take the radius of this circle to $\infty$ and compute the values of the individual segments of the contour (which is usually simple) before equating this with the sum of the enclosed residues $\times2\pi i$. Often the circular part tends to zero as the radius grows so it is even more simple to deal with.

Examples:
#### Evaluating trig integrals
If we have some trig integral (note the limits)
$$
I=\int_{0}^{2\pi} F(\cos\theta,\sin\theta) \, d\theta 
$$
we can always solve this by letting $z=e^{i\theta}$ be the contour (so $C$ is a unit circle) and then solving the general complex integral form of this using residue theorem like so:
$$
I=\oint_{C}F\left( \frac{z+z^{-1}}{2}, \frac{z-z^{-1}}{2i} \right)\, \frac{dz}{iz}=2\pi i\sum_{k=1}^{N} \text{Res}(f,w_{k})
$$
where $f(z)$ is the new complex integrand. This is from substituting $dz=ie^{i\theta}\,d\theta\implies d\theta=\frac{dz}{iz}$. Hence this just becomes a root-finding exercise for the rational function $f(z)$.
#### Evaluating improper integrals
If we have the integral
$$
I=\int_{-\infty}^{\infty} \frac{1}{(1+x^{2})^{2}}  \, dx 
$$
then we can define some contour $C=C_{x}+C_{R}$ composed of two segments - $C_{R}$ is a semi-circle winding CCW radius $R$ around the origin, and $C_{x}$ is a line along the real axis from $-R$ to $R$, and then consider
$$
\tilde{I}=\oint_{C} \frac{dz}{(1+z^{2})^{2}}=\int_{-R}^{R} \frac{1}{(1+x^{2})^{2}}  \, dx +\int_{0}^{\pi} \frac{i\mathrm{Re}^{i\theta}}{(1+R^{2}e^{2i\theta})} \, d\theta =I_{1}+I_{2}
$$
as $R\to \infty$, we have $I_{1}\to I$ and $I_{2}\to0$ since the integrand tends to $1 /R$ in the limit. Then considering the residues of the integrand, we have one at $i$, one at $-i$, but only the one at $i$ is enclosed in $C$ so we evaluate the residue there by expanding the integrand's [[Laurent series]]:
$$
\begin{align}
\frac{1}{(1+z^{2})^{2}} & =-\frac{1}{4} \frac{1}{(z-i)^{2}}+\frac{1}{4i} \frac{1}{(z-i)}+\dots \\[1ex]
\implies \text{Res}(f,i) & =\frac{1}{4i}
\end{align}
$$
so we can evaluate that
$$
\tilde{I}=(2\pi i)\left( \frac{1}{4i} \right)=\frac{\pi}{2}=I_{1}+I_{2}\underset{R\to \infty}=I
$$
hence our integral is just $I=\frac{\pi}{2}$. By conventional methods this would be very difficult to solve but as a contour integral it is trivial.
#### Integrals through singularities
Supposing we have the integral
$$
I=\int_{-\infty}^{\infty} \frac{\cos ax }{x-1}\, dx =\mathrm{Re}(I_{z})=\mathrm{Re}\left(\int_{-\infty}^{\infty} \frac{e^{iax}}{x-1} \, dx \right)
$$
for $a>0$, this goes through a singularity at $x=1$. We therefore use a modified contour, similar to before, but with four parts - the outer semi-circular curve with radius $R\to \infty$ centred on the origin, two strips along the real axis, and an inner semi-circular curve centred on $x=1$ with radius $\epsilon\to0$, so
$$
\tilde{I}=\underbrace{ \int_{-R}^{-\epsilon} \frac{e^{iax}}{x-1} \, d+\int_{\epsilon}^{R} \frac{e^{iax}}{x-1} }_{ \to I_{z}\text{ as }R\to \infty\text{ and }\epsilon\to0 } \, dx +\int_{C_{\epsilon}} \frac{e^{iaz}}{z-1}\,dz+ \int _{C_{R}} \frac{e^{iaz}}{z-1} \, dz  
$$
and then the $C_{R}$ term goes to zero by [[Jordan's lemma]], and the $C_{\epsilon}$ term gives
$$
I_{\epsilon}=\int_{\pi}^{0} \frac{i\epsilon e^{i\theta}e^{ia(1+\epsilon e^{i\theta})}}{\epsilon e^{i\theta}} \, dx =i\epsilon^{ia}\int_{\pi}^{0}  \, d\theta=-\pi ie^{ia} 
$$
which is independent of $\epsilon$, so we can then find that since the contour contains no poles,
$$
\int_{-\infty}^{\infty} \frac{e^{iax}}{x-1}\, dx =i\pi e^{ia}
$$
so taking $\mathrm{Re}$ and $\mathrm{Im}$ parts we actually get an extra integral for free:
$$
\int_{-\infty}^{\infty} \frac{\cos ax}{x-1} \, dx=-\pi \sin a\qquad\text{and}\qquad \int_{-\infty}^{\infty} \frac{\sin ax}{x-1} \, dx=\pi \cos a 
$$
Alternatively we could've taken the contour to include the pole at $z=1$ instead, which would've given the same result after taking the residue into account, but it is more work that way.