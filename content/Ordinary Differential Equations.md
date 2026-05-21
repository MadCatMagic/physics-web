---
aliases:
  - ODE
tags:
  - calc/ODE
date-created: 2025-12-30
template-version: m.0
---
[[Ordinary Differential Equations L_MT1]]

This is the study of differential equations of one independent variable.

#calc/ODE/existence-theorem #calc/ODE/lipschitz-continuous 
If $f$ is continuous in $x$ and Lipschitz continuous (does not $=\infty$, doesn't explode to infinity - well behaved) in $y$ at $(x_{0},y_{0})$ then a single solution exists in $[x_{0}-\epsilon,x_{0}+\epsilon]$ for arbitrarily small $\epsilon>0$.

Most of the time when working with equations that are linear in $y'$ of the form $f(x,y,y')=0$ we write them in **symmetric form**:
$$
P(x,y)dx+Q(x,y)dy=0
$$
so $y'=\frac{P(x,y)}{Q(x,y)}=f(x,y)$ and since $y(x+\Delta x)\approx y(x)+y'(x)\Delta x=y(x)+f(x,y)\Delta x$ we can draw a direction field using $f(x,y)$ as the gradient of arrows.
## 1st Order ODEs
#### Separable
#calc/ODE/1st-order-separable 
The simplest is the separable equation where
$$\frac{dy}{dx}=\frac{f(x)}{g(y)}$$
so the solutions are given by
$$
\int g(y) \, dy =\int f(x) \, dx 
$$
#### Almost Separable
#calc/ODE/1st-order-almost-separable 
Have the form $y'=f(ax+by)$, solved with the substitution $z=ax+by$ which leads to the solution
$$
\int \frac{1}{a+b f(z)} \, dz=\int  \, dx +C  
$$
#### Homogeneous 
#calc/ODE/1st-order-homogeneous
Have the form $y'=f\left( \frac{y}{x} \right)$ and are solved with the substitution $z=\frac{y}{x}$ to give
$$
\int \frac{dz}{f(z)-z}=\int \frac{dx}{x}+C
$$
#### Almost Homogeneous
#calc/ODE/1st-order-almost-homogeneous 
Have form
$$
y'=f\left(  \frac{a_{1}x+b_{1}y+c_{1}}{a_{2}x+b_{2}y+c_{2}} \right)
$$
and the it reduces to a homogenous case if we can substitute $X=x+u$ and $Y=y+v$ such that
$$
\begin{align}
a_{1}u+b_{1}v & =c_{1} \\
a_{2}u+b_{2}v & =c_{2}
\end{align}
$$
so 
$$\frac{dy}{dx}=\frac{dY}{dX}=f\left( \frac{a_{1}X+b_{1}Y}{a_{2}X+b_{2}Y} \right)=f\left( \frac{a_{1}+b_{1} \frac{Y}{X}}{a_{2}+b_{2} \frac{Y}{X}} \right)$$
which is homogeneous.
#### Bernoulli's equation
#calc/ODE/bernoullis-equation
Has the form
$$
\frac{dy}{dx}+P(x)y=Q(x)y^{n}
$$
equation can be made linear by substituting $z=y^{1-n}$ so
$$
\frac{dy}{dx}=\left( \frac{y^{n}}{1-n} \right) \frac{dz}{dx}
$$
Substituting into equation and dividing through by $y^{n}$ yields
$$
\frac{dz}{dx}+(1-n)P(x)z=(1-n)Q(x)
$$
which is [[Exact Differentials#Special case (Linear 1st order)|linear]].
### [[Exact Differentials]]
Finding a perfect *potential* function whose derivative is exactly the ODE in question. Includes *integrating factor*.
### [[Particular & Complementary Solutions#First order ODEs]]
A different more general technique for solving. Works for 1st order.
### Singular solutions
#calc/ODE/singular-solution
Sometimes the standard methods of solving will leave out a valid solution, called a singular solution. We can find this by considering a couple of cases:
- Is the ODE *autonomous?* So $y'=f(y)$ only. In this case $y(x)=C$ is a solution as well.
- Have we divided by any function of $x,y$ at some point? In this case the divisor equals zero could correspond to a solution.
In both cases, we only have a singular solution if it is not included in the general solution already found. Usually the singular solutions are not that important though.
## Higher Order ODEs
#calc/ODE/higher-order 
The case of $F(t,y,y',y'',\dots,y^{(n)})=0$, which can always be written as a systems of equations:
$$
\begin{align}
y' & =p_{1} \\
p_{1}' & =p_{2} \\
 & \vdots \\
p'_{n-2} & =p_{n-1} \\
F(t,y,p_{1},p_{2},\dots,p_{n-1},p'_{n-1}) & =0
\end{align}
$$
If consider just ODEs where the highest derivative is expressed in terms of everything else explicitly: $y^{(n)}=f(t,y,y',y'',\dots,y^{(n-1)})$
We can write this in the general form
$$
\vec{y}'=\vec{f}(t,\vec{y})
$$
where $\vec{y}'$ is the *phase velocity*, $\vec{y}$ is the *phase* and $\vec{f}$ is an $n$-dimensional *velocity field*. For an $n$ order ODE we require $n$ integration constants in the general solution and therefore have $n$ parameters to set for an initial value problem.

In the specific case where $y^{(n)}$ is independent of $t$, we have $\vec{y}'=\vec{f}(\vec{y})$ which represents the *phase space*. A graphical representation of this is a **phase portrait** #calc/ODE/phase-portrait. Systems of this form are called **conservative systems** #calc/ODE/conservative-systems.
### Linear ODEs
#calc/ODE/higher-order-linear 
#### Homogeneous Case
#calc/ODE/higher-order-homogenous-linear 
I.e.
$$
a_{n}(x)y^{(n)}+\dots+a_{1}(x)y'+a_{0}(x)y=0
$$
we want to find $n$ linearly independent solutions $y_{i}$ to find the general solution as the [[Linear Algebra|span]] of the solutions:
$$
y=C_{1}y_{1}+C_{2}y_{2}+\dots+C_{n}y_{n}
$$
We define the **Wronskian** [[determinant]] as 
$$
W=\det Y=\begin{vmatrix}
y_{1}(x) & y_{2}(x) & \dots & y_{n}(x) \\
y_{1}'(x) & y_{2}'(x) & \dots & y_{n}'(x) \\
\vdots & \vdots & \ddots & \vdots \\
y_{1}^{(n-1)}(x) & y_{2}^{(n-1)}(x) & \dots & y_{n}^{(n-1)}(x)
\end{vmatrix}
$$
The solutions are linearly independent iff $W\neq 0$ on some interval. #calc/ODE/wronskian 

Actually solving the ODE is just the same as for higher order ODEs in general. However for the *initial value problem* we can write the conditions as
$$
\vec{y}_{0}=\vec{y}(t_{0})=Y(t_{0})\vec{c}
$$
where $Y$ is the matrix of solutions and solution derivatives, $\vec{c}$ is the vector of constants for the specific solution, $\vec{y}$ is the vector of general solutions and their derivatives and $\vec{y}_{0}$ is the vector of values of the function and its derivatives at the initial point. So:
$$
\vec{c}=Y^{-1}(t_{0})\vec{y}_{0}
$$
and the solution can be written as
$$
\vec{y}(t)=Y(t)Y^{-1}(t_{0})\vec{y}_{0}
$$
or
$$
y(t)=\vec{y}^{T}(t)Y^{-1}(t_{0})\vec{y}_{0}
$$
##### Euler-Cauchy equations
#calc/ODE/euler-cauchy-equation
Have the form 
$$
a_{n}x^ny^{(n)}(x)+\dots+a_{1}xy'(x)+a_{0}y(x)=0
$$
and can all be transformed to linear ODEs using substitution $t=\ln x \iff x=e^{t}$.
#### Inhomogeneous Case
#calc/ODE/higher-order-inhomogenous-linear 
When the RHS has the function $f(x)$ we just need to find a single particular solution $y_{p}$ and add it to the general solution $y_{h}$ of the same ODE, but without the inhomogeneity. The particular solution should be linearly independent of every part of the homogenous solution.
The technique of [[Particular & Complementary Solutions#Variation of constants|variation of constants]] can be used to deduce one solution from another.
#### Constant Coefficients
#calc/ODE/higher-order-constant-coefficients 
When the coefficients are constant we can use the ansatz $y(x)=\exp(\lambda x)$ to find a *characteristic equation* which is an nth order polynomial in $\lambda$. This in general yields n $\lambda_{i}$ solutions for $\lambda$, each of which yields a potential linearly independent solution. 

If some of the roots are identical (degenerate), we need to find other linearly independent roots. This can be done with [[Particular & Complementary Solutions#Variation of constants|variation of constants]], but in general if a solution with algebraic duplicity $k$ is $e^{\lambda x}$, the resulting set of linearly independent parts of the general solution is $e^{\lambda x}(C_{1}+C_{2}x+\dots+C_{k}x^{k})$.

We can also write complex conjugate pairs of roots in real form with complex coefficients by writing:
$$
Pe^{(\lambda+i\omega)x}+Qe^{(\lambda-i\omega)x}=e^{\lambda x}(C_{1}\cos(\omega x)+C_{2}\sin(\omega x))
$$
## Systems of ODEs
#calc/ODE/systems-of-odes 
### Hermitian Systems
In the case of a constant coefficient matrix $A$ for the system
$$
\vec{y}'(t)=A\vec{y}(t)\iff \begin{pmatrix}
y_{1}' \\
y_{2}' \\
\vdots \\
y_{n}'
\end{pmatrix}=A\begin{pmatrix}
y_{1} \\
y_{2} \\
\vdots \\
y_{n}
\end{pmatrix}
$$
if $A$ is #linalg/hermitian-map hermitian ($A^{\dagger}=A$) then there exists $n$ linearly independent eigenvectors $\vec{v}_{i}$ and eigenvalues $\lambda_{i}$ which satisfy
$$
\det(A-\lambda_{i} I)=0\iff A\vec{v}_{i}=\lambda_{i}\vec{v}_{i}
$$
so we can diagonalize: $A=RDR^{-1}$. If we define
$$
\vec{c}(t)=\begin{pmatrix}
C_{1}e^{\lambda_{1}t} \\
C_{2}e^{\lambda_{2}t} \\
\vdots \\
C_{n}e^{\lambda_{n}t}
\end{pmatrix}
$$
this solves $\frac{d}{dt}\vec{c}(t)=D\vec{c}(t)$ so, multiplying back into the original basis,
$$
\vec{y}(t)=R\vec{c}(t)=C_{1}e^{\lambda_{1}t}\vec{v}_{1}+C_{2}e^{\lambda_{2}t}\vec{v}_{2}+\dots+C_{n}e^{\lambda_{n}t}\vec{v}_{n }
$$
solves the system.
We can also separate $\vec{c}(t)$ into $E(t)\vec{c}$ where $E(t)$ is a matrix whose diagonal is the exponentials, and $\vec{c}$ is a vector of constants. For the initial value problem, this means that
$$
\vec{y}(t_{0})=RE(t_{0})\vec{c}
$$
so
$$
\vec{c}=(E(t_{0}))^{-1}R^{-1}\vec{y}(t_{0})
$$
which means the specific solution is
$$
\vec{y}(t)=RE(t-t_{0})R^{-1}\vec{y}(t_{0})
$$
