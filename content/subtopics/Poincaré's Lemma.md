---
tags:
  - "#calc/poincares-lemma"
date-created: 2026-04-02
template-version: m.0
---
[[Vector Calculus]]

States that if $A:U\to \mathbb{R}^{n}$ vector field has a *vanishing cur*l and a *star shaped domain* $U$ (so that there is a $\mathbf{p} \in U$ s.t. the line from $\mathbf{p}$ to any $\mathbf{x}\in U$ are contained in $U$) *then $A$ is conservative*.

This statement can be generalised to [[Differential forms]] and so also holds true for e.g. vector potentials. We can also weaken the condition on $U$ - it is enough for $U$ to be simply-connected ($U$ contains no closed curves with cannot be continuously shrunk to a point in $U$).

Additionally since $\mathbb{R}^{n}$ is star-shaped, any curl-free vector fields with $U=\mathbb{R}^{n}$ are conservative, and we can find the potential $V$ as
$$
V(x)=\int_{C_{\mathbf{x}}}A\cdot d\mathbf{x}
$$
where $C_{\mathbf{x}}$ is any curve fully contained in $U$ connecting a reference point to $\mathbf{x}$.