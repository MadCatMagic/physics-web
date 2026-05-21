---
tags:
  - calc/manifold
date-created: 2026-05-19
template-version: m.0
---
[[Vector Calculus]]

AKA surfaces and stuff. Note that these are a special class of differentiable manifolds. We define such a manifold in one of two main ways:
#### Zero locus
As a **zero locus**, so a subset $M\subset \mathbb{R}^{n}$ is a $k$-dimensional (differentiable) sub-manifold of $\mathbb{R}^{n}$ if, for every $\mathbf{p} \in M$ and an [[Topology#Open sets|open]] neighbourhood $V\subset \mathbb{R}^{n}$ of $\mathbf{p}$, we have 
$$V\cap M=\{ \mathbf{x}\in V \mid f_{1}(x)=\dots=f_{n-k}(x)=0\}$$
for continuously differentiable functions $f_{i}:\mathbb{R}^{n}\to \mathbb{R}$ for which the [[Jacobi matrix]] has
$$
\text{rank}\left(\frac{ \partial (f_{1},\dots,f_{n-k}) }{ \partial (x_{1},\dots,x_{n}) }(\mathbf{p}) \right)=n-k.
$$
The first condition gives the definition of what the manifold actually contains, and the second requires that the manifold is smooth. We always require $n-k$ equations to define a $k$ dimensional manifold.
#### Parametrisation
As a **parametrisation**, so $M\subset \mathbb{R}^{n}$ is a $k$-dimensional sub-manifold of $\mathbb{R}^{n}$ iff, for every $\mathbf{p}\in M$, we have an open neighbourhood $V\subset \mathbb{R}^{n}$ of $\mathbf{p}$, an open set $U\subset \mathbb{R}^{k}$ and a *diffeomorphism* map $X=(X_{1},\dots,X_{n})^{T}:U\to V\cap M$ such that
$$
\text{rank}\left( \frac{ \partial (X_{1},\dots,X_{n}) }{ \partial (t_{1},\dots,t_{k}) }  \right)=k\quad \forall \mathbf{t}\in U
$$
the map $X$ is called a **chart** of $M$.

Note that we call $n-k$ the *co-dimension* of the manifold, and a manifold with co-dimension one in $\mathbb{R}^{n}$ is called a **hyper-surface**.
### Tangent space
#calc/manifold/tangent-space
Describes the vector space tangent to some point $\mathbf{p}\in M$. Specifically we have that the **tangent space** $T_{\mathbf{p}}M$ of a $k$-dim manifold $M\subset \mathbb{R}^{n}$ with a chart $X:U\to V\cap M \ni\mathbf{p}$ is given by
$$
T_{\mathbf{p}}M=\text{Span}(\mathbf{v}_{1}(\mathbf{p}),\dots,\mathbf{v}_{k}(\mathbf{p}))\quad\text{where}\quad \mathbf{v}_{a}(\mathbf{p})=\frac{ \partial X }{ \partial t_{a} } \Biggr|_{\mathbf{p}}
$$
note that this tangent space is $k$-dimensional at every point, and we can write a general vector at this point in terms of the basis $\{ \mathbf{v}_{1},\dots,\mathbf{v}_{n} \}$. We can also write these basis vectors as
$$
\mathbf{v}_{a}(\mathbf{p})=\sum_{i=1}^{n} \frac{ \partial X_{i} }{ \partial t_{a} }\Biggr|_{\mathbf{p}}\mathbf{e}_{i} 
$$
where $\mathbf{e}_{i}$ are the standard basis vectors in $\mathbb{R}^{n}$. So we can transform from the standard basis vectors to the manifold basis vectors by using the [[Jacobi matrix]] of the chart map.
#### Hyper-surfaces and normal vectors
#calc/manifold/normal
For a general $k$-manifold then we can define a **normal vector field** $N$ to be normal to $M$ at $\mathbf{p}\in M$ iff $N_{\mathbf{p}}$ is orthogonal to the entire tangent space $T_{\mathbf{p}}M$, so $\mathbf{v}\cdot N_{\mathbf{p}}=0$ for all $\mathbf{v}\in T_{\mathbf{p}}M$.

#calc/manifold/hyper-surface
Specifically for a *hyper-surface* so $k=n-1$, we require an $N_{\mathbf{p}}\in \mathbb{R}^{n}$ for which $\frac{ \partial X }{ \partial t_{a} }\big|_{\mathbf{p}}\cdot N_{\mathbf{p}}=0$ for $a=1,\dots,n-1$. We can define this explicitly using the formula
$$
\begin{align}
N_{\mathbf{p},i} & =\pm\epsilon_{ii_{1}\dots i_{n-1}} \frac{ \partial X_{i_{1}} }{ \partial t_{1} } \Biggr|_{\mathbf{p}}\dots\frac{ \partial X_{i_{n-1}} }{ \partial t_{n-1} } \Biggr|_{\mathbf{p}} \\[1ex]
  \implies \frac{ \partial X }{ \partial t_{a} }\Biggr|_{\mathbf{p}}\cdot N_{\mathbf{p}} & =\pm \det\left( \frac{ \partial X }{ \partial t_{a} } \Biggr|_{\mathbf{p}}, \frac{ \partial X }{ \partial t_{1} } \Biggr|_{\mathbf{p}},\dots,\frac{ \partial X }{ \partial t_{n-1} } \Biggr|_{\mathbf{p}}\right) =0
\end{align}
$$
where the final equality follows from there being a repeated column in the determinant matrix - so it goes to zero. *In three dimensions*, we just have that
$$
N_{\mathbf{p}}=\pm \frac{ \partial X }{ \partial t_{1} } \Biggr|_{\mathbf{p}}\times\frac{ \partial X }{ \partial t_{2} } \Biggr|_{\mathbf{p}}
$$
which matches our intuition for being normal to both tangent vector directions.

A hyper-surface is often defined in terms of the zero locus of a function $f:V\to \mathbb{R}$ such that $M\cap V=\{ \mathbf{x} \in V\mid f(\mathbf{x})=0 \}\ni \mathbf{p}$. As it turns out, we can easily find the normal vector by just setting
$$
N_{\mathbf{p}}=\pm \nabla f(\mathbf{p})
$$
since intuitively, the [[Gradient]] gives the direction of greatest ascent. This can be proved by writing a parametrisation $X(\mathbf{t})=(t_{1},\dots,t_{n-1},g(\mathbf{t}))^{T}$ in terms of the zero locus such that $f(\mathbf{t},g(\mathbf{t}))=0$ for $\mathbf{t}\in \mathbb{R}^{n-1}$.

Finally we can define the **unit normal vector field** as
$$
\hat{n}=\frac{N}{|N|}
$$
whichever way it was obtained. Note that only some surfaces are *orientable* i.e. there exists a continuous unit normal $\hat{n}:M\to \mathbb{R}^{n}$ on the entire hyper-surface. An example of a *non-orientable* surfaces is a Möbius strip.
### Metrics
#calc/manifold/metric 
Skipping a lot of mumbo jumbo, since the embedding space is $\mathbb{R}^{n}$, we already have a standard metric (scalar product), the dot product, which induces a **metric** $g$ on $M$ of the form
$$
g_{ab}=\frac{ \partial X }{ \partial t_{a} } \cdot \frac{ \partial X }{ \partial t_{b} } \iff g=\begin{pmatrix}
\left\lvert  \frac{ \partial X }{ \partial t_{1} }   \right\rvert ^{2} & \frac{ \partial X }{ \partial t_{1} } \cdot \frac{ \partial X }{ \partial t_{2} }  & \dots & \frac{ \partial X }{ \partial t_{1} } \cdot \frac{ \partial X }{ \partial t_{k} }  \\
\frac{ \partial X }{ \partial t_{1} } \cdot \frac{ \partial X }{ \partial t_{2} }  & \left\lvert  \frac{ \partial X }{ \partial t_{2} }   \right\rvert ^{2} & \dots & \frac{ \partial X }{ \partial t_{2} } \cdot \frac{ \partial X }{ \partial t_{k} }  \\
\vdots & \vdots & \ddots & \vdots \\
\frac{ \partial X }{ \partial t_{1} } \cdot \frac{ \partial X }{ \partial t_{k} } & \frac{ \partial X }{ \partial t_{2} } \cdot \frac{ \partial X }{ \partial t_{k} } & \dots & \left\lvert  \frac{ \partial X }{ \partial t_{k} }   \right\rvert ^{2}
\end{pmatrix}=\left( \frac{ \partial X }{ \partial \mathbf{t} }  \right)^{T}\left( \frac{ \partial X }{ \partial \mathbf{t} }  \right)
$$
we can interpret this metric by considering that for two tangent vectors $\boldsymbol{\alpha}=\alpha_{i}\mathbf{v}_{i}(\mathbf{p})$ and $\boldsymbol{\beta}=\beta_{j}\mathbf{v}_{j}(\mathbf{p})$, both in $T_{\mathbf{p}}M$, their scalar product is given by $g_{\mathbf{p},ij}\alpha_{i}\beta_{j}$.

The determinant of the induced metric is called **Gram's determinant** and is:
$$
\det(g)=\det\left(\left( \frac{ \partial X }{ \partial \mathbf{t} }  \right)^{T}\left( \frac{ \partial X }{ \partial \mathbf{t} }  \right)\right)
$$
Note that **importantly**
$$
\sqrt{ \det(g) }=\det\left( \frac{ \partial X }{ \partial \mathbf{t} }  \right)
$$
which will be important later 
*skipping some stuff about rewriting diff operators in new coordinate systems...*