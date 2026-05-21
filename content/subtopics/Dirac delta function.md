---
tags:
  - maths/dirac-delta-function
date-created: 2026-04-02
template-version: m.0
---
[[Maths bits]]

There is a need in lots of physics for a representation of a point particle. (for modelling stuff) and so we use the Dirac delta function for that. Note that it is not technically a function but a *generalised function* or *distribution* - the limit of a series of functions. 

It is best to think of the delta function as something always intended to be in an integrand. In particular two delta functions are equal if
$$
\int_{-\infty}^{\infty} f(x)D_{1}(x) \, dx=\int_{-\infty}^{\infty} f(x)D_{2}(x) \, dx  
$$
### One dimensional case
We define $\delta(x)$ such that
$$
\delta(x)=\begin{cases}
0 & \text{if }x\neq 0, \\
\infty & \text{if }x=0,
\end{cases}
$$
and
$$
\int_{-\infty}^{\infty} \delta(x) \, dx =1
$$
Note that the dimensions of $\delta(x)$ are 1 over dimensions of $x$, so if $[x]=\text{m}$, $[\delta(x)]=\text{m}^{-1}$.

If $f(x)$ is some ordinary continuous function then
$$
f(x)\delta(x)=f(0)\delta(x)
$$
hence
$$
\int_{-\infty}^{\infty} f(x)\delta(x) \, dx =f(0)\int_{-\infty}^{\infty} \delta(x) \, dx=f(0)
$$
so the delta function 'picks out' the value of $f(x)$ at $x=0$ under an integral. We can of course shift this to any other value by just generalising as
$$
\delta(x-a)=\begin{cases}
0 & \text{if }x\neq a, \\
\infty & \text{if }x=a,
\end{cases} \quad\text{with}\quad\int_{-\infty}^{\infty} \delta(x-a) \, dx =1
$$
so
$$
\int_{-\infty}^{\infty} f(x)\delta(x-a) \, dx =f(a)
$$
We can derive identities from this, for example
$$
\delta(kx)=\frac{1}{|k|}\delta(x)
$$
using equality criterion from above.
### Three dimensional case
It is easy to generalise
$$
\delta^{3}(\mathbf{r})=\delta(x)\delta(y)\delta(z)
$$
so the integral over $\mathbb{R}^{3}$ is 1. Similar properties hold:
$$
\int_{\text{all space}}f(\mathbf{r})\delta^{3}(\mathbf{r}-\mathbf{a})\,dV=f(\mathbf{a})
$$
We can relate this to other functions like [[Divergence]] by noting that
$$
\nabla\cdot\left( \frac{\hat{r}}{r^{2}} \right)=4\pi\delta^{3}(\mathbf{r})
$$

