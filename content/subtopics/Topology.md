---
tags:
  - topology
date-created: 2026-04-01
template-version: m.0
---
[[Maths bits]]
[[Vector Calculus]] is where most uses are found.

This will all be working in $\mathbb{R}^{n}$ with the standard [[Metric]]
$$
|\mathbf{x}|=\left( \sum_{i=1}^{n} x_{i}^{2} \right)^{1/2}
$$
which defines a metric space $\{ \mathbb{R}^{n},\,|x| \}$. #topology/metric-space 

#topology/ball
We then can define the **ball** with radius $r$ as
$$
B_{r}(\mathbf{a})=\{ \mathbf{x} \in \mathbb{R}^{n}\mid |\mathbf{x}-\mathbf{a}|<r \}
$$
note that this doesn't include the surface of the ball. 

#topology/neighbourhood 
Additionally, $U$ is the *neighbourhood* of $\mathbf{x} \in \mathbb{R}^{n}$ if $\exists\epsilon>0$ where $B_{\epsilon}(\mathbf{x}) \subset U$.
### Open sets
#topology/open-sets 
A set $U\in \mathbb{R}^{n}$ is **open** if for every $\mathbf{x}\in U,\,\exists\,\epsilon>0: B_{\epsilon}(\mathbf{x})\subset U$. 
A set $C\in \mathbb{R}^{n}$ is **closed** if $\mathbb{R}^{n}\setminus C$ is open.
Effectively we can consider open sets to exclude their boundary and closed sets to include their boundary. A set can be neither open nor closed (or alternatively both but in different parts of the set if we consider being open or closed a local property).
1. Empty set and full set $\mathbb{R}^{n}$ are open sets (and also closed).
2. Intersection and union of open sets is also open.

If we have a subset $X\subset \mathbb{R}^{n}$ then
- A point $\mathbf{x}\in \mathbb{R}^{n}$ is called an *interior* point of $X$ if there exists $\epsilon>0$ s.t. $B_{\epsilon}(\mathbf{x})\subset X$. (so not on boundary)
- A point is *exterior* of $X$ if $B_{\epsilon}(\mathbf{x})\not\subset X\iff B_{\epsilon}(\mathbf{x})\subset \mathbb{R}^{n}\setminus X$.
- The set of all interior points is $\dot{X}$.
- A point is a *boundary point* if $B_{\epsilon}(\mathbf{x})$ intersects $X$ and its complement.
- The set of all boundary points is $\partial X$.
- The *closure* of $X$ is $\bar{X}=X \cup \partial X$.

For any such subset we then have the following properties:
- $\dot{X}$ is open and $\dot{X}=X\setminus \partial X$
- $\bar{X}$ is closed (by definition)
- $\partial X$ is also closed
- Iff $X$ open then $X=\dot{X}$
- Iff $X$ closed then $X=\bar{X}$

Additionally we have the fact that the closure $\bar{X}$ is given by $X$ and all of its limit points (since boundary points are the limit of any sequence ending at the boundary).

#topology/compact 
A subset is called **compact** if it is closed and bounded where bounded means
$$
\exists R>0\text{ so } X\subset B_{R}(0)
$$
#todo 
Alternatively, if every open cover has a finite subcover. An open cover $U$ is a collection of open sets that cover $X$, and a subcover $V$ is a subcollection $V\subset U$ that still covers $X$.

This definition holds for more general topological spaces - any space for which it is defined which subsets are open.

These two definitions are equivalent on Rn

Another topological definition is that a set is sequentially compact if every sequence of points in X has a subsequence which converges in X

tychonoff theorem, any product of compact sets is compact