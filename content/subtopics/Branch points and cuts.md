---
tags:
  - "#complex/branch-cut"
  - complex/branch-point
date-created: 2026-05-19
template-version: m.0
---
[[Complex Numbers]]

Supposing we have an image plane $w=f(z)$ and a domain plane $z$ where $f(z)=z^{1/2}$. Taking a loop on the $z$ plane around the origin, this does not correspond to a full loop in the $w$ plane. Specifically $f(e^{i(0)})\neq f(e^{i(2\pi)})$ even though these complex values are supposed to be equal normally. In this case we call the point we travelled around ($z=0$ here) a **branch point**. 

We can deal with this by introducing **branch cuts**, where we pick any direction for the cut (so long as it goes from the branch point to $\infty$). Any path not passing the cut will satisfy end points being equal under $f$. (**extremely lacking rigour here...**) This is somehow explained by *Riemann sheets*?

For example, taking $f(z)=\sqrt{ z^{2}-1 }$ has two branch points at $z=\pm1$, and we have two valid branch cut configurations - both points going to $\infty$ or the points connecting to one another. Both of these cases yield the same behaviour that only paths crossing the branch cut (an odd number of times?) have unequal endpoint values under $f$.
### Riemann sheets
#complex/riemann-sheets
Considering $f(z)=\ln z=\ln r+i\theta$, if we traverse a loop around the origin, then each time $\mathrm{Im}(f(z))$ increases by $2\pi$. We can think of $f(z)$ as mapping the plane to $\infty$ sheets separated by $2\pi$ (HOW??) or as a single curved surface topology which removes the need for an explicit branch cut. Similarly for $f(z)=z^{1/2}$ we need two sheets for the $4\pi$ periodicity.
### Integrals of functions involving branch cuts and points
Consider the integral
$$
I=\int_{0}^{\infty} \frac{1}{(x+a)^{2}\sqrt{ x }} \, dx 
$$
with $a>0$. This has a pole at $x=-a$ and a branch point at $x=0$, so we can let a branch cut go from $x=0$ along the positive real axis to $\infty$. Applying [[Residue theorem]], we get that
$$
2\pi i\,\text{Res}[f,a]=\left( \int_{l_{+}}+\int_{l_{-}}+\int_{C_{R}}+\int_{C_{\epsilon}} \right) \frac{dz}{(z+a)^{2}\sqrt{ z }}
$$
where we have taken the following contour
![[course/raw/Lecture 2026-05-15 9am.excalidraw.md#^clippedframe=zEkNzqn4fMwbC6hxUylXm]]
We can calculate the residue at $x=-a$ by finding the [[Laurent series]] expansion around that position so
$$
\frac{1}{(z+a)^{2}\sqrt{ z }}=\frac{(-a)^{-1/2}}{(z+a)^{2}}+\frac{1}{2ia^{3/2}} \frac{1}{(z+a)}+\dots
$$
hence the residue is $(2ia^{3/2})^{-1}$. Then the integrals for the curves both tend to 0 as $R\to \infty$ and $\epsilon\to0$, by simple analysis of the integrands under the relevant substitutions, so we just have to deal with
$$
I_{l_{+}}+I_{l_{-}}=\int_{0}^{\infty} \frac{1}{(x+a)^{2}\sqrt{ x }} \, dx +\int_{\infty}^{0} \frac{1}{(xe^{2\pi i}+a)^{2}\sqrt{ xe^{2\pi i} }} \, d(e^{2\pi i}x)  
$$
where in the second integral we substitute $x\to e^{2\pi i}x$ since it is on the other side of the branch cut so has $2\pi$ phase difference. Therefore
$$
I_{l_{+}}+I_{l_{-}}=2\int_{0}^{\infty} \frac{1}{(x+a)^{2}\sqrt{ x }} \, dx 
$$
so we directly get the final result
$$
\int_{0}^{\infty} \frac{1}{(x+a)^{2}\sqrt{ x }} \, dx =\frac{\pi}{2a^{3/2}}
$$
