---
tags:
  - linalg/eigenvalue
  - linalg/eigenvector
  - linalg/eigen-properties
date-created: 2025-12-21
template-version: m.0
---
[[Linear Algebra]]

For a linear map, the **eigenvalue** $\lambda \in F$ satisfies, for a non-zero **eigenvector** $\vec{v}\in V$$$
f(\vec{v})=\lambda \vec{v}
$$
We can then define an **eigenspace** #linalg/eigenspace for a particular $\lambda$
$$
\text{Eig}_{f}(\lambda)=\text{Ker}(f-\lambda\text{ id}_{V})
$$
which is a sub vector space of $V$ and collects the eigenvalues. If the dimension of the eigenspace is 1 then the $\lambda$ is *non-degenerate*, whereas for higher dimensions it is *degenerate*. This leads to the summary:
$$
\lambda\text{ is an e-v of }f \iff \text{Ker}(f-\lambda\text{ id}_{V})\neq \{ 0 \}\iff\text{det}(f-\lambda\text{ id}_{V})=0
$$
### Characteristic polynomial
#linalg/characteristic-polynomial 
is defined by
$$
\chi_{f}(\lambda)=\text{det}(f-\lambda\text{ id}_{V})
$$
and the eigenvalues are then the zeroes of this polynomial, so can be determined like this. The characteristic polynomial is *basis-independent*, and therefore the eigenvalues are also basis-independent.

Then, we compute the eigenspace by finding all vectors $\vec{v}$ which solve the equation
$$
(f-\lambda\text{ id}_{V})\vec{v}=0
$$
which gives the eigenvalues.
#### Trace of a matrix
#linalg/trace
One valid [[Scalar Product]] for a matrix and also a useful tool is the trace defined as the sum of the diagonal terms. It is also basis independent, as it directly relates to the characteristic equation.

In particular, for $\chi_{f}(\lambda)=c_{n}\lambda^n+c_{n-1}\lambda^{n-1}+\dots+c_{1}\lambda+c_{0}$, we have that
- $c_{n}=(-1)^n$
- $c_{n-1}=(-1)^{n-1}\text{ tr}(A)$
- $c_{0}=\det (A)$
Since the eigenvalues are solutions of the equations we then have that
$$
\det(A)=\prod_{i=1}^{n} \lambda_{i},\quad\text{tr}(A)=\sum_{i=1}^{n} \lambda_{i}
$$
### Diagonalization
#linalg/diagonalization #linalg/diagonalizable 
A linear map $f$ can be diagonalized if there exists a basis of $V$ in which the matrix describing $f$ is diagonal. Hence, a matrix $A$ can be diagonalized iff there is an invertible $n\times n$ matrix $P$ such that $\hat{A}=P^{-1}AP$ is diagonal.

The matrix $P$ is defined as $P=(\vec{v}_{1},\vec{v}_{2},\dots,\vec{v}_{n})$ - matrix whose columns are the eigenvectors, and $\hat{A}=\text{diag}(\lambda_{1},\lambda_{2},\dots,\lambda_{n})$.

Since it must be a basis of eigenvectors, this gives more stringent requirements. For $A$ to be diagonalized, each eigenvalue must have its algebraic duplicity equal to its geometric duplicity - the corresponding eigenspace (the space of vectors $\vec{v}$ satisfying $A\vec{v}=\lambda \vec{v}$) must have a dimension equal to the duplicity of the root in the characteristic equation.

So if we have $n$ unique eigenvalues for an $n\times n$ matrix, we are guaranteed diagonalizability. 
#### Self-adjoint maps
If a map is self-adjoint #linalg/self-adjoint (so has corresponding *symmetric/hermitian matrix*), and for the map $f:V\to V$ over $\mathbb{R}$ ($\mathbb{C}$) with real (hermitian) scalar product, then
- All eigenvalues are real
- Eigenvectors are all orthogonal
- this guarantees diagonalizability
And therefore the resulting basis of eigenvectors $\{ \epsilon_{1},\epsilon_{2},\dots,\epsilon_{n} \}$ is ortho-normal. #linalg/orthonormal-basis This means that $P$ is orthogonal (unitary).

If we have a higher-dimension eigenspace then we can use the [[Gram-Schmidt Algorithm]] to find orthogonal eigenvectors in the space.

#### Normal linear maps
#linalg/normal-map #linalg/commutator
A linear map $f:V\to V$ is **normal** iff $f\circ f^{\dagger}=f^{\dagger}\circ f$, or equivalently iff the **commutator** vanishes: $[f,f^{\dagger}]=f\circ f^{\dagger}-f^{\dagger}\circ f=0$. This category encompasses *hermitian* and *unitary* maps, as well as *anti-hermitian* maps ($f=-f^{\dagger}$).

This class of maps has the property that: if $\lambda$ is an eigenvalue of $f$ with eigenvector $\vec{v}$ then $\lambda ^{*}$ is an eigenvalue of $f^{\dagger}$ for the same eigenvector.

More importantly, iff $f$ is normal, it has an **ortho-normal basis** of eigenvectors. 

#linalg/unitary-map 
For a *unitary* map, there is the additional constraint that $|\lambda|=1$ for complex $\lambda$.
#### Simultaneous diagonalization
Two matrices $A$, $B$ can be diagonalized simultaneously iff $[A,B]=0$. [[V&Mlecturenotes.pdf#page=126&selection=202,0,203,1&color=yellow|Proof.]] This means that one basis transformation $P$ transforms both to diagonal matrices.

We can prove this for the case when the eigenvalues of $A$ are non-degenerate by considering that each eigenvalue of $A$ must satisfy $A\vec{v}_{A}=\lambda_{A}\vec{v}_{A}$ for the eigenvector $\vec{v}_{A}$, so multiplying by $B$:
$$
BA\vec{v}_{A}=A(B\vec{v}_{A})=\lambda_{A}(B\vec{v}_{A})
$$
so $B\vec{v}_{A}$ is also an eigenvector of $A$ with eigenvalue $\lambda_{A}$ - however, since eigenvalues of $A$ are non-degenerate, this means that $B\vec{v}_{A}\in\text{eigenspace}(\lambda_{A})$ which for non-degenerate eigenvalues is just all scaled vectors $\alpha \vec{v}_{A}$ so we must have
$$
B\vec{v}_{A}=\lambda_{B}\vec{v}_{A}
$$
for some $\lambda_{B}\in \mathbb{R}$. Hence eigenvectors of $A$ are eigenvectors of $B$, so we can simultaneously diagonalize them as they have the same eigenvector basis. *Note that the linked proof has much more details and rigour*.