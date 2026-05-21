---
tags:
  - relativity/4-vector
date-created: 2025-12-23
template-version: m.0
---
[[Special Relativity]]

A **4-vector** is anything that transforms under an L.T. the same way as $X$:
$$
X=\begin{pmatrix}
ct \\
x \\
y \\
z
\end{pmatrix},\quad X'=\Lambda X
$$
Where $X$ is a 4-position vector for an event. 

#relativity/minkowsky-inner-product #relativity/invariant-scalar-product 
We can then defined the **Minkowsky inner product** (aka *invariant scalar product*) as
$$
X\cdot Y=X^{T}\eta Y=X_{0}Y_{0}-X_{1}Y_{1}-X_{2}Y_{2}-X_{3}Y_{3}
$$
which is naturally invariant under L.T. Hence, 'Squaring' a 4-position vector gives:
$$
X\cdot X=c^{2}t^{2}-x^{2}-y^{2}-z^{2}
$$
which is the invariant interval.
### 4-velocity & 4-acceleration
#relativity/4-velocity #relativity/4-acceleration
The time derivative of $X$ is not a 4-vector, but the derivative with respect to *proper time* is, and is the **4-velocity** vector:
$$
U=\begin{pmatrix}
c \frac{dt}{d\tau} \\
\frac{dx}{d\tau} \\
\frac{dy}{d\tau} \\
\frac{dz}{d\tau}
\end{pmatrix}=\begin{pmatrix}
\gamma_{u}c  \\
\uparrow\\
\gamma_{u}\vec{u} \\
\downarrow
\end{pmatrix}
$$
and $U\cdot U=c^{2}$. (using $d\tau=\frac{1}{\gamma}dt$)
Another derivative w.r.t $\tau$ gives **4 acceleration**:
$$
A=\frac{dU}{d\tau}=\gamma^{2}\left( \frac{\vec{u}\cdot \vec{a}}{c}\gamma^{2}, \frac{\vec{u}\cdot \vec{a}}{c^{2}}\gamma^{2}\vec{u}+\vec{a} \right)^{T}
$$
which is not pretty. Then, $A\cdot A=-|\vec{a}_{\text{inst}}|^{2}$.
In the rest frame, $\vec{U}\cdot \vec{A}=0$ so are orthogonal in rest frame.
This directly leads to
### [[Momentum and Energy]]
### Relativistic Newton's Laws
#relativity/newtons-laws #relativity/4-force
The normal equation is replaced with
$$
\frac{dP}{d\tau}=F
$$
where $P$ is the 4-momentum and $F$ is the **4-Force** such that
$$
F=\begin{pmatrix}
\frac{\gamma}{c} \frac{dE}{dt} \\
\gamma \vec{f}
\end{pmatrix}
$$
where $\vec{f}$ is the 3-force and is analogous to the Newtonian force vector, so
$$
\frac{d\vec{p}}{dt}=\vec{f}
$$
We can also find that
$$
\frac{dE}{dt}=\vec{u}\cdot \vec{f}
$$
which is the equivalent of $Fv=P$ from Newtonian mechanics. 