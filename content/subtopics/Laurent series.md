---
tags:
  - complex/laurent-series
date-created: 2026-05-18
template-version: m.0
---
[[Complex Numbers]]
[[Taylor series]] (is a complex generalisation of this)

The Laurent series allows us to write a converging power series for a point $a$ like so:
$$
f(z)=\sum_{n=-p}^{\infty }a_{n}(z-a)^{n} 
$$
for constants $a_{n}\in \mathbb{C}$. Note that if $p=0$ this is exactly equal to the taylor series around the point, and we denote the **principal part** of the Laurent series as
$$
\mathcal{P} [f,a]=\sum_{n=-p}^{-1} a_{n}(z-a)^{n}
$$
so it is the 'pole' parts of the series.

If $f(z)$ is analytic at $a$, then $p=0$. Otherwise, we expect $p$ to vary depending on the type of singularity (isolated). If it is an essential singularity, $p=\infty$, if it is a removeable singularity $p=0$ but $f(a)\neq a_{0}$, and if it is a pole then $p$ is the order of the pole (highest reciprocal power). 

We can think of this that for a pole order $p$, then $(z-a)^{p}f(z)$ is analytic at $a$ so we can locally taylor expand around $a$:
$$
f(z)=\frac{1}{(z-a)^{p}}\sum_{n=0}^{\infty} b_{n}(z-a)^{n}=\sum_{n=-p}^{\infty} a_{n}(z-a)^{n}
$$
Note that the [[Residue theorem|residue]] of the point is given just as
$$
\text{Res}(f,a)=a_{-1}
$$
and this means that residues can also be found for essential singularities, not just poles.