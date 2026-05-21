---
tags:
  - calc/helmholtz-theorem
date-created: 2026-04-02
template-version: m.0
---
[[Vector Calculus]]

This theorem guarantees that a field is uniquely determined by its divergence and curl. If we have $\nabla\cdot \mathbf{F}=\phi$ and $\nabla \times \mathbf{F}=\mathbf{C}$ (so $\nabla\cdot \mathbf{C}=0$ as well) then if these functions are nicely behaved and go to zero at infinity (specifically faster than $1/r^{2}$, then by the theorem,
$$
\mathbf{F}=-\nabla U+\nabla \times \mathbf{W}
$$
where
$$
U(\mathbf{r})=\frac{1}{4\pi}\int \frac{\phi(\mathbf{r}')}{|\mathbf{r}-\mathbf{r}'|} \, dV'
$$
and
$$
\mathbf{W}(\mathbf{r})=\frac{1}{4\pi}\int \frac{\mathbf{C}(\mathbf{r}')}{|\mathbf{r}-\mathbf{r}'|} \, dV'
$$
where integrals are over $\mathbb{R}^{3}$. If we assume these integrals converge, it just so happens this is an exact single solution because there is no vector function with vanishing divergence and curl, and goes to zero at infinity that is not $0$, so this is the single unique solution.

More generally, any (diff) vector function $\mathbf{F}(\mathbf{r})$ that goes to zero faster than $1/r$ as $r\to \infty$ can be expressed as the gradient of a scalar plus the curl of a vector. (*even more generally this is true for any $\mathbf{F}$ with no conditions*, but that is a stronger statement then Helmholtz theorem can show).