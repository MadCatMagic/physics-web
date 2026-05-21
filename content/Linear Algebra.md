---
tags:
  - linalg
date-created: 2025-12-18
template-version: m.0
---

[[Vectors & Matrices L_MT1]]
[[Vectors & Matrices (Rn)]]
### Vector space
#linalg/vector-space 
A vector space is a set $V$ on a field $F$ with an addition and a scalar multiplication s.t. all elements constructible from members of $V$ are also in $V$ - a vector space is closed. Elements in $V$ are called vectors $\vec{v}$.

To prove something is a vector space it is sufficient to show that
- it is non-empty (contains 0 vector)
- it is closed under scalar multiplication
- it is closed under vector addition

#linalg/sub-vector-spaces 
A sub vector space $U$ is a vector space s.t. every element is contained in $V$, while holding all the usual vector space properties. E.g. $\mathbb{R}$ is a sub-vector space of $\mathbb{R}^{2}$.
#### Linear combinations
We can take a linear combination of $k$ vectors in a vector space $V$ like so:
$$
\alpha_{1}\vec{v}_{1}+\dots+\alpha _{k}\vec{v}_{k}=\sum_{i=1}^{k} \alpha_{i}\vec{v}_{i}
$$
The set of all possible combinations is called the #linalg/span of the vectors. The *span* is necessarily a sub vector space of $V$.

A 'minimal' span is one in which every vector is **linearly independent** #linalg/linear-independence. This is true iff
$$
\sum_{i=1}^{k} \alpha_{i}\vec{v}_{i}=0\iff\text{all }\alpha_{i}=0
$$
otherwise they are linearly dependent. If this is the case one vector can be written as a linear combination of the others.

#### Basis and dimension
Any set of linearly independent vectors that spans the whole vector space is a **basis** #linalg/basis.
Any vector in $V$ can then be represented by some linear combination of the basis:
$$
\vec{v}=\sum_{i=1}^{n} \alpha_{i}\vec{e}_{i}
$$
for a given basis $\{ \vec{e}_{1},\dots,\vec{e}_{n} \}$.

The number of vectors in a basis for a vector space $V$ is the dimension #linalg/dim of the space, denoted by
$$
\text{dim }V=n
$$
### Linear maps
#linalg/linear-map 
A map assigns to each $x \in X$ a $y\in Y$:
$$
f:X\to Y,\quad x \mapsto f(x)
$$
It assigns to each element of the *domain* an element of the *codomain*. The set of all reachable co-domain values is the **Image** of $f$, $\mathrm{Im}(f)$ #linalg/image.

We can compose maps like so:
$$
(f \circ g)(x)=f(g(x))
$$
and so on. 

A **linear map** is a map that operates on two vector spaces and so has linearity. The **kernal** $\text{Ker}(f)$ is the set of elements $\vec{v}$ s.t. $f(\vec{v})=0$. #linalg/kernal 

The dimension of the image of $f$ is the **rank** of $f$: #linalg/rank 
$$
\text{rank}(f)=\text{dim Im}(f)
$$
and the dimension of the kernal is the **nullity** of $f$: #linalg/nullity
$$
\text{nullity}(f)=\text{dim Ker}(f)
$$
The set of all linear maps $f:V\to W$ forms the vector space $\text{Hom}(V,W)$ as expected.
#### Rank-nullity
The #linalg/rank-nullity-theorem states that:
$$
\text{nullity}(f)+\text{rank}(f)=\text{dim}(V)
$$
### Matrices
#linalg/matrix-properties 
An $n\times m$ matrix given by
$$
A=\begin{pmatrix}
a_{11} & \dots & a_{1m} \\
\vdots &  & \vdots \\
a_{n1} & \dots & a_{nm}
\end{pmatrix}
$$
has $n$ rows and $m$ columns. If $n=m$ the matrix is square or *quadratic* #linalg/quadratic-matrix.
This also defines a linear map, and each linear map is expressible as a matrix - by matrix multiplication:
$$
A\vec{v}=\sum_{i=1}^{m} v_{i}A^i =\begin{pmatrix}
\vec{v}\cdot A_{1} \\
\vdots \\
\vec{v}\cdot A_{n}
\end{pmatrix}
$$
A *diagonal matrix* only has elements along the diagonal, and is 0 elsewhere.
The *conjugate matrix* has: $(A^{*})_{ij}=(A_{ij})^{*}$
The *transpose* of a matrix is obtained by exchanging rows and columns.
A matrix is *symmetric* if $A_{ij}=A_{ji}$ and *antisymmetric* if $A_{ij}=-A_{ji}$.
The **hermitian conjugate** of a matrix is the conjugate of the transpose matrix: $A^{\dagger}=(A^T)^{*}$. A matrix is *hermitian* if $A=A^{\dagger}$ and *anti-hermitian* if $A=-A^{\dagger}$. 
#### Relation to linear maps
Suppose we have a linear map $f:F^{m}\to F^{n}$ and we want to find the matrix representation of $f$ in bases $\mathbf{e}_{i}$ for $F^{m}$ and $\mathbf{\tilde{e}}_{i}$ for $F^{n}$. Then we can find the images of these standard unit vectors under the linear map in terms of some arbitrary constants $a_{ij}$ like so:
$$
f(\mathbf{e}_{j})=\sum_{i=1}^{n} a_{ij}\mathbf{\tilde{e}}_{i}
$$
then considering a general $\mathbf{v}\in F^{m}$ written in terms of the basis $\mathbf{e}_{i}$, its image under $f$ is then
$$
f(\mathbf{v})=\sum_{j=1}^{m} v_{j}f(\mathbf{e}_{j})=\sum_{j=1}^{m} v_{j}\sum_{i=1}^{n} a_{ij}\mathbf{\tilde{e}}_{i}=\sum_{i=1}^{n} \left( \sum_{j=1}^{m} a_{ij}v_{j} \right)\mathbf{\tilde{e}}_{i}
$$
which suggests that for the $i$th component of the image,
$$
[f(\mathbf{v})]_{i}=\sum_{j=1}^{m} a_{ij}v_{j}=(A\mathbf{v})_{i}
$$
where $A$ is the matrix with entries $a_{ij}$ which is the coefficients relating the basis vectors under the transformation. Hence every arbitrary linear map between column vectors can be expressed in terms of a matrix.
#### Rank
The rank of a matrix is the dimension of the span of its column vectors #linalg/rank:
$$
\text{rank}(A)=\text{dim Span}(A^1,\dots,A^{m})
$$
this is the column rank of the matrix = row rank of the matrix.
#### Multiplication
Matrices can be multiplied - same as composing linear maps. In summation notation,
$$
(AB)_{ij}=\sum_{k=1}^{n} A_{ik}B_{kj}
$$
#### Inverse
#linalg/inverse 
The inverse of a matrix exists if the matrix is square and its rank is maximal i.e. $\text{rank}(A)=n$.
#### [[Determinant]]

### Change of Basis
#linalg/change-of-basis 
There are four parts that come into consideration when describing how a linear map is represented under a basis, so if we consider two bases (an unprimed and primed one) and simplify by only considering a simple map $f:V\to V$ we have:
$$
\begin{align}
\text{basis of }V && \text{coordinate map} && \text{coordinate vector} && \text{representing matrix} \\
\{ \mathbf{v}_{1},\dots,\mathbf{v}_{n} \} && \psi(\boldsymbol{\alpha})=\sum_{i=1}^{n} \alpha_{i}\mathbf{v}_{i} && \boldsymbol{\alpha}=(\alpha_{1},\dots,\alpha_{n})^{T} && A=\psi ^{-1}\circ f\circ \psi \\
\{ \mathbf{v}'_{1},\dots,\mathbf{v}'_{n} \} && \psi'(\boldsymbol{\alpha}')=\sum_{i=1}^{n} \alpha'_{i}\mathbf{v}'_{i} && \boldsymbol{\alpha}'=(\alpha'_{1},\dots,\alpha'_{n})^{T} && A'=\psi' ^{-1}\circ f\circ \psi'
\end{align}
$$
If we want to relate $A$ and $A'$ we only need to consider that
$$
A'=\psi'^{-1}\circ f\circ \psi'=\underbrace{ \psi'^{-1}\circ \psi }_{ =P } \circ \underbrace{ \psi ^{-1}\circ f\circ \psi }_{ =A } \circ \underbrace{ \psi ^{-1}\circ \psi' }_{ =P^{-1} }
$$
so we directly get the **change of basis formula** $A'=PAP^{-1}$. Note that importantly, these change of basis matrices $P$ have the property that
$$
\boldsymbol{\alpha}'=P\boldsymbol{\alpha}
$$
so converts between coordinate vectors. This can be observed directly from the form of $P$ ($=\psi'^{-1}\circ\psi$). Another way of thinking about this is that $P$ relates the primed and unprimed basis vectors like so:
$$
\mathbf{v}_{j}=\sum_{i}P_{ij}\mathbf{v}_{i}'
$$
$$
\begin{align}
\psi(\mathbf{w}_{j}) & =\sum_{i}A'_{ij}\mathbf{w}_{i} \\
 & =\sum_{i}\sum_{k}A'_{ij}C_{ki}\mathbf{u}_{k} \\
 & =\sum_{k}\sum_{i}C_{ki}A'_{ij}\mathbf{u}_{k} \\
 & =\sum_{k}(CA')_{kj}\mathbf{u}_{k} \\
\psi\left( \sum_{i}C_{ij}\mathbf{u}_{i} \right) & =\sum_{i}C_{ij}\psi(\mathbf{u}_{i}) \\
 & =\sum_{i}C_{ij}\sum_{k}A_{ki}\mathbf{u}_{k} \\
 & =\sum_{k}\sum_{i}A_{ki}C_{ik}\mathbf{u}_{k} \\
 & =\sum_{k}(AC)_{kj}\mathbf{u}_{k}
\end{align}
$$
[[V&Mlecturenotes.pdf#page=72&selection=2,0,2,15&color=yellow|V&Mlecturenotes, p.71]]
### [[Scalar Product]]
Including *dual vector spaces*, *orthonormal basis*.
### [[Eigenvalues & Eigenvectors]]
Including *diagonalization*, *normal maps*.