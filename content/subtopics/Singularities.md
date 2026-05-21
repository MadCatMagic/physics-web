---
tags:
  - "#complex/singularity"
date-created: 2026-05-18
template-version: m.0
---
[[Complex Numbers]]

Supposing we have a function $f(z)$ that is analytic (so $\frac{df}{dz}$ is well defined) except for some *isolated* point $z_{0}$ where $\frac{df}{dz}\to \infty$ then we have a **singularity** at that point (it isn't analytic at that point). Note that functions that are analytic everywhere are *entire* (or *integral*) functions. 

We can classify singularities depending on their properties, and all **isolated singularities** will fall into one of three categories:
#### Removeable singularities
#complex/removeable-singularity 
A function which is analytic everywhere except at the singularity, and also has
$$
\lim_{ z \to z_{0} } f(z)\neq f(z)
$$
has a *removeable singularity* if we can define $g(z)$ to be analytic everywhere where
$$
g(z)=\begin{cases}
f(z) & \text{for} & z\neq a \\
\lim_{ z \to z_{0} }  & \text{for} & z=a
\end{cases}
$$
Alternatively, supposing we have a [[Laurent series]] expansion around the singularity, it will be of the form $f(z-z_{0})=a_{0}+a_{1}(z-z_{0})+\dots$ i.e. will have no pole terms, so we can define $g(z_{0})=a_{0}$ instead. 
#### Poles
#complex/pole 
A point $z_{0}$ is a **pole** of $f$ if it is a zero of $1/f$ and $1 /f$ is holomorphic on some neighbourhood of $z_{0}$. Note that this means poles are *isolated* by definition. If this is the case then there exists some integer $n>0$ such that
$$
g(z)=(z-z_{0})^{n}f(z)
$$
is holomorphic and nonzero in a neighbourhood of $z_{0}$. $n$ is the *order* (or degree) of the pole. A *simple pole* has $n=1$.

Considering the [[Laurent series]], we see that if it has finitely many terms in the *principal* part of its Laurent expansion, then it is a pole with order given by the greatest term in the expansion (if a point has multiple orders we assume the greatest). For example, the function
$$
f(z)=\frac{1}{(z-a)^{n}},\quad n\in \mathbb{N}
$$
is a pole of order $n$ at $a$. Functions can have infinitely many poles, and poles can have multiple orders, but a point with 'infinite' orders is not a pole but an essential singularity.

The [[Residue theorem|residue]] of a pole is the coefficient of the 1st order pole part. 
#### Essential singularities
#complex/essential-singularity 
A singularity which is neither removeable or a pole is called *essential*. For example
$$
f(z)=e^{1/z}=\sum_{n=0}^{\infty} \frac{1}{n!}\left( \frac{1}{z} \right)^{n}
$$
has infinite pole degrees so cannot itself be a pole. In other words, the [[Laurent series]] of $f$ has infinitely many negative degree terms. Alternatively, if there is a point $a$ for which $f(z)(z-a)^{n}$ is not differentiable at $a$ for all $n>0$ then $a$ is an essential singularity.