---
tags:
  - linalg/gram-schmidt-algorithm
  - linalg/orthonormal-basis
date-created: 2025-12-21
template-version: m.0
---
This algorithm is used to find an orthonormal basis from a non-orthonormal basis, provided the space is equipped with a [[Scalar Product]]. If we begin with a basis $\{ \vec{v}_{1},\vec{v}_{2},\dots,\vec{v}_{n} \}$, then we proceed to find the orthonormal basis $\{ \hat{\epsilon}_{1},\hat{\epsilon}_{2},\dots,\hat{\epsilon}_{n} \}$ like so:
$$
\hat{\epsilon}_{1}=\frac{\vec{v}_{1}}{|\vec{v}_{1}|}
$$
and then for the remaining set,
$$
\vec{v}_{k}'=\vec{v}_{k}-\sum_{i=1}^{k-1} \langle \hat{\epsilon}_{i},\vec{v}_{k} \rangle \hat{\epsilon}_{i},\quad\hat{\epsilon}_{k}=\frac{\vec{v}_{k}'}{|\vec{v}_{k}'|}
$$
for $k=2,3,\dots,n$. This is guaranteed to be an orthonormal basis, and therefore every finite dimensional vector space has an orthonormal basis - provided it is equipped with a scalar product.