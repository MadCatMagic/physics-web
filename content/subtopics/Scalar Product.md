---
tags:
  - linalg/scalar-product
  - linalg/scalar-product-properties
date-created: 2025-12-18
template-version: m.0
---
The scalar product is an operation with certain properties:
- $\langle \vec{v},\vec{w} \rangle=\langle \vec{w},\vec{v} \rangle^{*}$
- $\langle \gamma\vec{v},\alpha \vec{u}+\beta \vec{w} \rangle=\gamma ^{*}(\alpha\langle \vec{v},\vec{u} \rangle+\beta \langle \vec{v},\vec{w} \rangle)$ - conjugate linear in one of the arguments, linear in the other. (by convention)
- $\langle \vec{v},\vec{v} \rangle>0\text{ if }\vec{v}\neq {0}$.

It can be real (symmetric) or hermitian depending on whether the field is real or complex.

We then have a well defined length of a vector under this operation:
$$
|\vec{v}|^{2}=\langle \vec{v},\vec{v} \rangle 
$$
which follows the inequalities and properties given in [[Vectors & Matrices (Rn)]].

We can also state that two vectors are orthogonal if $\langle \vec{v},\vec{u} \rangle=0$ (although this says nothing about their magnitudes), provided $|\vec{v}|\neq0$ and $|\vec{u}|\neq0$.

### Orthonormal basis
#linalg/orthonormal-basis
A basis $\{ \epsilon_{1},\epsilon_{2},\dots,\epsilon_{n} \}$ is orthonormal iff
$$
\langle \epsilon_{i}, \epsilon_{j} \rangle =\delta_{ij}
$$
This can be derived using the [[Gram-Schmidt Algorithm]].

A use of this is that we can derive properties about the scalar product regardless of what it actually is. For example, we can start with:
$$
\vec{v}=\sum_{i}\alpha_{i}\hat{\epsilon}_{i},\quad \alpha_{i}=\langle \hat{\epsilon}_{i}, \vec{v} \rangle 
$$
$$
\vec{w}=\sum_{i}\beta_{i}\hat{\epsilon}_{i},\quad \beta_{i}=\langle \hat{\epsilon}_{i},\vec{w} \rangle 
$$
hence their scalar product is
$$
\langle \vec{v},\vec{w} \rangle=\sum_{i,j}\alpha_{i}^{*}\beta_{j}\langle \hat{\epsilon}_{i},\hat{\epsilon}_{j} \rangle=\sum_{i}\alpha_{i}^{*}\beta_{i}=\sum_{i}\langle \vec{v},\hat{\epsilon}_{i} \rangle\langle \hat{\epsilon}_{i},\vec{w} \rangle  
$$
This shows that relative to an ortho-normal basis, a scalar product can be expressed in terms of the standard scalar (dot) product on $\mathbb{F}^{n}$ - it always has this form in an ortho-normal basis. Additionally if we want to compute the representing matrix of a linear map $f:V\to V$ we get
$$
A_{ij}=\langle \hat{\epsilon}_{i},f(\hat{\epsilon}_{j}) \rangle 
$$
#### Perpendicular Space
#linalg/perpendicular-space
The perpendicular space $W^{\perp}\in V$ relative to some subspace $W\in V$ is defined such that
$$
W^{\perp}=\{ \vec{v}\in V\mid\langle \vec{w},\vec{v} \rangle =0\text{ for all } \vec{w}\in W \}
$$
i.e. it consists of all vectors orthogonal to all vectors in $W$.

#### Adjoint linear map
#linalg/adjoint 
An adjoint linear map is one satisfying
$$
\langle \vec{v},f\vec{w} \rangle=\langle f^{\dagger}\vec{v},\vec{w} \rangle  
$$
this is the effective 'hermitian conjugate' of a linear map, so follows same properties e.g. $(\alpha f)^{\dagger}=\alpha ^{*}f^{\dagger}$, $(f\circ g)^{\dagger}=g^{\dagger}\circ f^{\dagger}$, $(f^{-1})^{\dagger}=(f^{\dagger})^{-1}$, etc.

#linalg/self-adjoint 
A linear map is self-adjoint (or hermitian) iff $f=f^{\dagger}$. This means that
$$
\langle \vec{v},f(\vec{w}) \rangle=\langle f(\vec{v}),\vec{w} \rangle  
$$
#### Orthogonal/Unitary maps
#linalg/orthogonal-map #linalg/unitary-map
$V$ has a real (hermitian) scalar product. A linear map is orthogonal (unitary) iff
$$
\langle f(\vec{v}),f(\vec{w}) \rangle =\langle \vec{v},\vec{w} \rangle 
$$
in particular this means that $|f(\vec{v})|=|\vec{v}|$, so $f$ leaves the angle between vectors, and their lengths unchanged - it is a 'rotation' or 'reflection'. We have some properties:
- $f^{\dagger}\circ f=\text{id}_{V}$ 
- which implies that $f^{-1}=f^{\dagger}$
- composition of unitary maps is also unitary
The corresponding matrix $M$ representing $f$ has $|\det M|=1$ and the column vectors are orthogonal. If a matrix $M$ has $\det M=1$ then it is *special orthogonal* - represents a 'pure rotation'.

### Dual Vector Space
#linalg/dual-vector-space 
Taking the set of all linear maps $\phi:V\to F$ where we consider $F\equiv\mathbb{F}$ is a trivial one dimensional vector space - these maps are also called **linear functionals** #linalg/linear-functional and the set of all linear functionals is the *dual vector space* $V^{*}$ of $V$.

For example, for $V=\mathbb{R}^n$ and a fixed vector $\vec{w}\in V$, we can define $\phi_{\vec{w}}\in(\mathbb{R}^{n})^{*}$ by
$$
\phi_{\vec{w}}(\vec{v})=\vec{w}^T\vec{v}\in \mathbb{R}
$$
All linear functionals in $(\mathbb{R}^{n})^{*}$ are of this form. So all the functionals in $\mathbb{R}^{n}$ can be thought of as row vectors. Expanding on this idea we can write a corresponding *dual basis* $\hat{\epsilon}_{*}^{i}$ #linalg/dual-basis for any particular basis $\hat{\epsilon}_{j}$ such that
$$
\hat{\epsilon}^{i}_{*}(\hat{\epsilon}_{j})=\delta^{i}_{j}
$$
so $\text{dim}(V^{*})=\text{dim}(V)$. This has to do with the relation between coordinate spaces and the vector and basis defining that coordinate space. **dont understand this fully...**
[[V&Mlecturenotes.pdf#page=110&selection=85,0,85,11&color=yellow|V&Mlecturenotes, p.109]]
