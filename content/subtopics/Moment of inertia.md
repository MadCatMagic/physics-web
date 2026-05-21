---
tags:
  - "#mech/moment-of-inertia"
  - "#mech/inertia-tensor"
date-created: 2026-02-23
template-version: m.0
---
[[Rotational Dynamics]]
[[Mechanics]]

Considering the general equation $\vec{J}=I\vec{\omega}$, it is clear that if $\vec{J}$ and $\vec{\omega}$ are not parallel, $I$ cannot be a scalar and must in this instance be a matrix (or rank 2 tensor - its called the inertia tensor so yk). For increasing complexity:
- when all masses have same plane of rotation, $\vec{J}\parallel\vec{\omega}$, and $\vec{J}$ defined w.r.t origin on axis of rotation in plane of rotation we have the simplest case $I=\sum m_{i}r^{2}_{i}$.
- If $\vec{J} \nparallel\vec{\omega}$ then we retain that $\vec{J}_{z}=I_{z}\vec{\omega}$ where $\vec{\omega}\parallel \hat{z}$ so $I_{z}=\sum m_{i}r^{2}_{i}$ where $r_{i}$ measured perpendicular to axis.
- If $\vec{J}$ defined w.r.t point on axis of rotation then we still find same $I_{z}$.
- In the limit of continuous solid then the sum becomes
$$
I_{z}=\int _{V}d^{2}\rho(\vec{r}) \, dV 
$$
where $d$ is the distance perp to the $z$-axis.
### Inertia tensor
Considering the most general case where $\vec{J}$ is not parallel to $\vec{\omega}$ (but origin is still on rotational axis) we have the basic definition
$$
\vec{J}=\sum_{i=1}^{N} \vec{r}_{i}\times \vec{p}_{i}=\sum_{i=1}^{N} m_{i}\vec{r}_{i}\times  \dot{\vec{r}}_{i}
$$
then using implicit definition of angular velocity in circular motion $\dot{\vec{r}}=\vec{\omega}\times \vec{r}$ and expanding out with the triple product identity we get
$$
\vec{J}=\underbrace{ \sum_{i=1}^{N} m_{i}r_{i}^{2}\vec{\omega} }_{ \text{standard I component} }-\underbrace{ \sum_{i=1}^{N} m_{i}(\vec{r}_{i}\cdot\vec{\omega})\vec{r}_{i} }_{ \text{extra terms} }
$$
If we reformulate this in cartesian components and trudge through the algebra for a while you find the inertia tensor summation definition that is
$$
\begin{pmatrix}
J_{x} \\
J_{y} \\
J_{z}
\end{pmatrix}=\begin{pmatrix}
\sum(y_{i}^{2}+z_{i}^{2})m_{i} & -\sum(x_{i}y_{i})m_{i} & -\sum(x_{i}z_{i})m_{i} \\
-\sum(x_{i}y_{i})m_{i} & \sum (x_{i}^{2}+z_{i}^{2})m_{i} & -\sum(y_{i}z_{i})m_{i} \\
-\sum(x_{i}z_{i})m_{i} & -\sum(y_{i}z_{i})m_{i} & \sum(x_{i}^{2}+y_{i}^{2})m_{i}
\end{pmatrix}\begin{pmatrix}
\omega_{x} \\
\omega_{y} \\
\omega_{z}
\end{pmatrix}
$$
which shows a real, symmetric, rank-2 tensor with 6 independent components. If the mass is continuous in a rigid body we can take the continuum limit for the more common definition of the relation:
$$
\begin{pmatrix}
J_{x} \\
J_{y} \\
J_{z}
\end{pmatrix}=\begin{pmatrix}
\int (y^{2}+z^{2}) \, dm  & -\int xy \, dm & -\int xz \, dm  \\
-\int xy \, dm  & \int(x^{2}+z^{2})\,dm & -\int yz \, dm  \\
-\int xz \, dm  & -\int yz \, dm  & \int(x^{2}+y^{2})\,dm 
\end{pmatrix}\begin{pmatrix}
\omega_{x} \\
\omega_{y} \\
\omega_{z}
\end{pmatrix}
$$
so we can finally write $\vec{J}=\tilde{I}\omega$ where $\tilde{I}$ is the **moment of inertia tensor** of the system of rigidly connected point-masses or the continuous rigid body.

We label the components as 
$$
\begin{pmatrix}
J_{x} \\
J_{y} \\
J_{z}
\end{pmatrix}=\begin{pmatrix}
I_{xx} & I_{xy} & I_{xz} \\
I_{yx} & I_{yy} & I_{yz} \\
I_{zx} & I_{zy} & I_{zz}
\end{pmatrix}\begin{pmatrix}
\omega_{x} \\
\omega_{y} \\
\omega_{z}
\end{pmatrix}
$$
where the diagonal elements are the *moments of inertia* around the corresponding axes and the off-diagonal terms are called *moments of deviation* or *products of inertia*. 

Considering the *principal axes* which cross in the COM and are somehow balanced (???) in that all the moments of deviation become zero - there is always a way of finding these. This is true because the matrix is symmetric, so there exists a [[Eigenvalues & Eigenvectors|diagonal form]] for which all the off-axis components are zero. When the coordinate system is aligned with this principal axis $I$ becomes diagonal, and the diagonal terms are called *principal moments of inertia*.

To find the principal axis in general would require finding the eigenvalues of the inertia tensor, but if there are any plane (mirror) symmetries in the mass distribution, then the normal vector of that plane is a principal axis (origin = COM as always).
### Common moments of inertia
All have total mass $M$.
##### Thin homogeneous rectangular plate
Aligned with xy-plane, centred on origin, with x-length a and y-length b has:
$$
I_{xx}=\frac{Mb^{2}}{12},\quad I_{yy}=\frac{Ma^{2}}{12},\quad I_{zz}=M \frac{a^{2}+b^{2}}{12}
$$
##### Thin homogenous disk/cylinder
With axis of rotation in z-dir, radius R has
$$
I_{zz}=\frac{1}{2}MR^{2}
$$
for both of them. For the thin disk by perpendicular axis theorem we also have
$$
I_{x}=I_{y}=\frac{1}{4}MR^{2}
$$
##### Homogeneous solid sphere
With radius $R_{0}$ has
$$
I=\frac{2}{5}MR_{0}^{2}
$$
since is spherically symmetric.
### Axis theorems
#mech/parallel-axis-theorem
If $I_{\text{cm}}$ is the moment of inertia of a body of mass $M$ about an axis of direction $\hat{\omega}$ passing through its centre of mass (CM), and $I$ is the moment of inertia of the same body about a second axis parallel to $\hat{\omega}$ but a perpendicular distance $d$ away from the first axis. Then the moment of inertia about the CM axis is $I_{\text{cm}}=\int r^{2} \, dm$ and to calculate $I$ in primed coordinates aligned with second axis:
$$
\vec{r}'=\vec{d}+\vec{r}\implies r'^{2}=d^{2}+2\vec{d}\cdot \vec{r}+r^{2}
$$
So the moment of inertia about the second axis is
$$
	I=\int r'^{2} \, dm=\int d^{2}dm+2\vec{d}\cdot \int \vec{r} \, dm+\int r^{2}\,dm
$$
where the integral is over the volume being considered, hence by definition of centre of mass, the first term is $d^{2}M$, the second is zero and hence
$$
I=Md^{2}+I_{\text{cm}}
$$
which is the **parallel axis theorem**.

#mech/perpendicular-axis-theorem
This only applies for a thin rigid body entirely in one plane, but gives
$$
I_{z}=I_{y}+I_{x}
$$
so relates the moment of inertia about each axis. This is the **perpendicular axis theorem**.