---
tags:
  - calc/partial-diff
date-created: 2025-12-22
template-version: m.0
---
[[Calculus]]
### Vector definition
is that a function is partially differentiable w.r.t. $x_{i}$ if
$$
\frac{ \partial f }{ \partial x_{i} } = \lim_{ \epsilon \to 0 } \frac{f(\mathbf{x}+\epsilon \mathbf{e}_{i})-f(\mathbf{x})}{\epsilon}
$$
exists. In vector analysis we sometimes write this as $\partial_{i}f(\mathbf{x})$ for short. An alternative definition of this is that
$$
f(\mathbf{x}+\epsilon \mathbf{e}_{i})=f(\mathbf{x})+\frac{ \partial f }{ \partial x_{i} } (\mathbf{x})\epsilon \mathbf{e}_{i}+O(\epsilon^{2})
$$
which effectively states the partial derivative as a linear approximation. Partial differentiation is therefore linear, and also follows the familiar product rule.

#### Directional derivative
#calc/partial-diff/directional-derivative 
Generalising in some direction $\mathbf{v}$, $f$ is differentiable in a direction $\mathbf{v}$ if there exists $\partial_{\mathbf{v}}f(\mathbf{x})$ s.t.
$$
f(\mathbf{x}+\mathbf{v}\epsilon)=f(\mathbf{x})+\partial_{\mathbf{v}}f(\mathbf{x})\epsilon+O(\epsilon^{2})
$$
Applying linearity of the operation and treating $\mathbf{v}$ in terms of an orthonormal basis, we get that
$$
\partial_{\mathbf{v}} f(\mathbf{x})=\sum_{i=1}^{n} v_{i} \frac{ \partial f }{ \partial x_{i} } (\mathbf{x})
$$
We can also write this in terms of the [[Gradient]] like so:
$$
\partial_{\mathbf{v}}f(\mathbf{x})=\mathbf{v}\cdot \nabla f(\mathbf{x})
$$
### Clairaut's theorem
#calc/partial-diff/clairauts-theorem 
Is that for a function where the second derivatives both exist at a point, we have at that point,
$$
\frac{ \partial^{2} f }{ \partial x \partial y } =\frac{ \partial^{2} f }{ \partial y \partial x } \iff f_{xy}=f_{yx}
$$
This extends to higher dimensions.
### Total Derivative
#### In one dimension
#calc/partial-diff/total-derivative 
#calc/partial-diff/total-differential 
The **total differential** is
$$
df=\frac{ \partial f }{ \partial x } dx+\frac{ \partial f }{ \partial y } dy
$$
and the **total derivative** is then logically
$$
\frac{df}{dx}=\frac{ \partial f }{ \partial x } +\frac{ \partial f }{ \partial y } \frac{dy}{dx}
$$
provided $y$ is a function of only $x$.
#### [[Exact Differentials]]
Whether there exists a function whose total differential is the differential being considered.
#### [[Jacobi matrix]]
Is the generalisation of this to vector-valued functions.
### Relations
The following relations can all be derived from the form of the total derivative.
$$
\left( \frac{ \partial x }{ \partial y }  \right)_{z}=\left( \frac{ \partial y }{ \partial x }  \right)^{-1}_{z}
$$
is #calc/partial-diff/reciprocity-relation provided derivatives do not vanish. Similarly, #calc/partial-diff/cyclic-relation is
$$
\left( \frac{ \partial y }{ \partial z }  \right)_{x}\left( \frac{ \partial z }{ \partial x }  \right)_{y}\left( \frac{ \partial x }{ \partial y }  \right)_{z}=-1
$$
#### Chain rule
#calc/partial-diff/chain-rule 
$$
\frac{df}{du}=\frac{ \partial f }{ \partial x } \frac{dx}{du}+\frac{ \partial f }{ \partial y } \frac{dy}{du}
$$
from dividing through the total differential. Logically we can extend this to vector form as
$$
D_{f\circ g}(\mathbf{x})=D_{f}(\mathbf{y})D_{g}(\mathbf{x})
$$
where $\mathbf{y}=g(\mathbf{x})$. (assuming totally differentiable at points, sets work, etc.) This allows us to rewrite this product in terms of indices to get the most common version of the chain rule:
$$
\frac{ \partial (f\circ g)_{i} }{ \partial x_{j} } (\mathbf{x})=\sum_{k=1}^{m} \frac{ \partial f_{i} }{ \partial g_{k} } (\mathbf{y})\frac{ \partial g_{k} }{ \partial x_{j} } (\mathbf{x})
$$
#calc/partial-diff/inverse
If we have an invertible differentiable function $g$ with $\mathbf{y}=g(\mathbf{x})$ then $D_{g}(\mathbf{x})$ is invertible and
$$
D_{g^{-1}}(\mathbf{y})=(D_{g}(\mathbf{x}))^{-1}
$$
#### Change of variables
#calc/partial-diff/change-of-variables 
$$
\frac{ \partial f }{ \partial u_{j} } =\sum_{i=1}^{n} \frac{ \partial f }{ \partial x_{i} } \frac{ \partial x_{i} }{ \partial u_{j} } ,\quad j=1,2,\dots,m
$$
To change from $f=(x_{1},x_{2},\dots,x_{n})$ to $x_{i}=x_{i}(u_{1},u_{2},\dots,u_{m})$.
#### [[Taylor series]]
Mostly the multidimensional/vector definitions.
### Stationary points
#calc/partial-diff/stationary-values
All stationary points have $f_{x}=f_{y}=0$ and:
- minima if $f_{xx}$ and $f_{yy}$ positive *and* $f^{2}_{xy}<f_{xx}f_{yy}$
- maxima if $f_{xx}$ and $f_{yy}$ negative *and* $f^{2}_{xy}<f_{xx}f_{yy}$
- saddle point if $f_{xx}$ and $f_{yy}$ have opposite signs *or* $f^{2}_{xy}>f_{xx}f_{yy}$
- ELSE, need to analyse further derivatives.
This is the case for $f(x,y)$ i.e. two dimensions.
#### Higher dimensional case
#calc/extremal-points
In this case, the local extrema of a function $f:U\to \mathbb{R}$, $U\in \mathbb{R}^{n}$ are found at its stationary points as before, specifically those points where $\nabla f(x)=0$ (using [[Gradient]]). To determine the nature of these points we can consider the [[Taylor series]] which gives
$$
f(\mathbf{x}+\boldsymbol{\xi})-f(\mathbf{x})=\frac{1}{2}\boldsymbol{\xi}^{T}H_{f}(\mathbf{x})\boldsymbol{\xi}+\mathcal{O} (|\boldsymbol{\xi}|^{3})
$$
so the behaviour is determined by the properties of the [[Hesse matrix]]. We specifically have that
1. If $H_{f}(\mathbf{x})$ is positive definite then $\mathbf{x}$ is an isolated local minimum
2. If $H_{f}(\mathbf{x})$ is negative definite then $\mathbf{x}$ is an isolated local maximum
3. If $H_{f}(\mathbf{x})$ is indefinite then $\mathbf{x}$ is not a local extremum
4. Otherwise, e-values are not strictly negative or positive (contain zeroes) so we cannot determine nature just from $H_{f}$.

Hence we can determine the stationary points and nature of them by solving $\nabla f(\mathbf{x})=0$, computing $H_{f}(\mathbf{x})$ for each of those stationary points and then classifying according to the eigenvalues of the matrix (all positive, then positive definite, etc.)

In the two dimensional case this reduces to the conditions stated above.