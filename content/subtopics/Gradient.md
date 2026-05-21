---
tags:
  - "#calc/gradient"
date-created: 2026-01-25
template-version: m.0
---
[[Vector Calculus]]

The **gradient** is an operator on a scalar function $f:U\to \mathbb{R}$ where $U\in \mathbb{R}^{n}$, that returns a vector field. It is given by:
$$
\text{grad}\,f(\mathbf{x})=\nabla f(\mathbf{x})=\left( \frac{ \partial  }{ \partial x_{1} } ,\dots,\frac{ \partial  }{ \partial x_{n} }  \right)f(\mathbf{x})
$$
in *cartesian coordinates*. This is equivalent to the [[Jacobi matrix]] for a scalar function $f$. Note the use of the nabla operator $\nabla=\frac{ \partial  }{ \partial x_{i} }e_{i}$.

The gradient has several properties:
- $(\nabla f)_{i}=\partial_{i}f$
- linearity
- product/quotient rules $\nabla(fg)=f\nabla g+g\nabla f$, etc.
We can also write the [[Partial Differentiation#Directional derivative|directional derivative]] in terms of the gradient.

We can derive a vector field $F$ from a scalar function $f$ by applying the gradient to $f$, fields generated this way are [[Conservative forces]].

The gradient represents the *slope* of the scalar function in the space - it is a vector field and the vectors point in the direction of greatest change of the scalar function. (direction of steepest ascent)

There are several alternative forms in different coordinate spaces. In *spherical coordinates* $(r,\theta,\phi)$, this transforms to
$$
\nabla =\left( \frac{ \partial  }{ \partial r } , \frac{1}{r}\frac{ \partial  }{ \partial \theta } , \frac{1}{r\sin\theta}\frac{ \partial  }{ \partial \phi }  \right)
$$