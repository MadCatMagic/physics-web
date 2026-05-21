---
tags:
  - linalg
date-created: 2025-12-18
template-version: m.0
---
This page covers properties and uses of vectors and matrices in standard $\mathbb{R}^{n}$ space such as will be used for most of physics.
More generally [[Linear Algebra]] covers the maths focused topic.

### Scalar & Vector Products
In $\mathbb{R}^{n}$ we have the **standard scalar** (or dot) product #linalg/dot-product 
$$
\vec{a}\cdot \vec{b}=\sum_{i=1}^{n} a_{i}b_{i}
$$
or using Einstein summation notation, $\vec{a}\cdot \vec{b}=a_{i}b_{i}$
This follows all the [[Scalar Product]] properties.

We also then have the **Cauchy-Schwarz inequality** #linalg/cauchy-schwarz-ineq
$$
|\vec{a}\cdot \vec{b}|\leq |\vec{a}||\vec{b}|
$$
proof given [[V&Mlecturenotes.pdf#page=23&selection=258,1,258,26&color=yellow|V&Mlecturenotes, p.22]].
And the related **Triangle inequality** #linalg/triangle-ineq
$$
|\vec{a}+\vec{b}|\leq |\vec{a}|+|\vec{b}|
$$

We can also write that
$$
\vec{a}\cdot \vec{b}=|\vec{a}||\vec{b}|\cos \theta
$$
for the angle $\theta$ between the vectors.

Then the **cross product** #linalg/cross-product is
$$
(\vec{a}\times \vec{b})_{i}=\epsilon_{ijk}a_{j}b_{k}
$$
using [[Summation notation#Levi-civita tensor|levi-civita notation]], and there are a couple of identities with it [[V&Mlecturenotes.pdf#page=23&selection=258,1,258,26&color=yellow|V&Mlecturenotes, p.22]].

There is also the **triple product**:
$$
\langle \vec{a},\vec{b},\vec{c} \rangle =\vec{a}\cdot(\vec{b}\times \vec{c})=\det(\vec{a}, \vec{b}, \vec{c})
$$
### Geometry
[[V&Mlecturenotes.pdf#page=32&selection=473,0,473,31&color=yellow|V&Mlecturenotes, p.31]]