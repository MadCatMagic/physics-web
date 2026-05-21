---
tags:
  - linalg/levi-civita-epsilon
  - linalg/kronecher-delta
date-created: 2026-03-12
template-version: m.0
---
[[Maths bits]]
### Kronecher delta
Is a tool that is defined
$$
\delta_{ij}=\begin{cases}
1 & \text{if} & i=j \\
0 & \text{if} & i\neq j
\end{cases}
$$
where $i,j$ are just integers that are usually being summed over. For example, if we have a vector $\mathbf{a}\in \mathbb{R}^{n}$, $\delta_{ij}a_{j}=a_{i}$ i.e. it replaces the index. Note that in this case we are summing over all $j=1,\dots,n$ since the $j$ index is repeated. Similarly we can write the dot product as
$$
\mathbf{a}\cdot \mathbf{b}=a_{i}b_{i}=\delta_{ij}a_{i}b_{j}
$$
and additionally $\delta_{ii}=n$ since we are just summing over 1s.
### Levi-civita tensor
This is a similar tool, where
$$
\epsilon_{i_{1}i_{2}\dots i_{n}}=\begin{cases}
+1 & \text{if} & (i_{1},i_{2},\dots ,i_{n})\text{ is cyclic} \\
-1 & \text{if} & (i_{1},i_{2},\dots,i_{n}) \text{ is anti-cyclic} \\
0 &  & \text{otherwise}
\end{cases}
$$
in this case $(1,2,3)$ would be cyclic, as would any cyclic permutation $(2,3,1)$ or $(3,1,2)$, whereas $(2,1,3),(3,2,1),(1,3,2)$ are all anti-cyclic, since they require swapping two of the numbers from a cyclic permutation. If any indices are equal, $\epsilon=0$.
#### In $\mathbb{R}^{3}$
It has a number of useful properties, namely
- Remains unchanged under cyclic permutations, e.g. $\epsilon_{ijk}=\epsilon_{jki}$
- Changes sign under anti-cyclic permutations or swaps, e.g. $\epsilon_{ijk}=-\epsilon_{ikj}$
- Vanishes if indices are identical, e.g. $\epsilon_{ijj}=0$
- $\epsilon_{ijk}\epsilon_{ilm}=\delta_{jl}\delta_{km}-\delta_{jm}\delta_{kl}$
- $\epsilon_{ijk}\epsilon_{ijm}=2\delta_{km}$
- $\epsilon_{ijk}\epsilon_{ijk}=6$
- $\epsilon_{ijk}a_{j}a_{k}=0$ since multiplication of $a_{j}a_{k}$ is commutative but indices of epsilon are anticommutative, so all pairs $j,k$ and $k,j$ cancel.
This allows for shortening of many complex expressions, for example the cross product can be written simply as
$$
(\mathbf{a}\times \mathbf{b})_{i}=\epsilon_{ijk}a_{j}b_{k}
$$