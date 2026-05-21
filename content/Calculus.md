---
tags:
  - calc
date-created: 2025-12-21
template-version: m.0
---
[[Calculus L_MT1]]
[[Multivariate Calculus L_HT1]]
### Differentiation
#calc/leibnitzs-theorem 
Leibnitz's theorem is that you can expand product rule like binomial.
#### [[Ordinary Differential Equations]]
A total overview of the subject.
### [[Partial Differentiation]]
Most important part of what we do as allows generalisation of differentiation to multiple dimensions.
### [[Vector Calculus]]
About integration and differentiation in multidimensional spaces.
### Integration
#calc/integration 
fun little integration table

| Integrand                                   | Result                                               |
| ------------------------------------------- | ---------------------------------------------------- |
| $\int \tan ax \, dx$                        | $\frac{1}{a} \ln\lvert\text{sec } ax \rvert$         |
| $\int \text{sec}\, ax\, dx$                 | $\frac{1}{a} \ln\lvert\text{sec } ax+\tan ax \rvert$ |
| $\int \frac{1}{a^{2}+x^{2}} \, dx$          | $\frac{1}{a}\tan ^{-1}\left( \frac{x}{a} \right)$    |
| $\int \frac{1}{\sqrt{ a^{2}-x^{2} }} \, dx$ | $\sin ^{-1}\left( \frac{x}{a} \right)$               |
| $\int \ln x \, dx$                          | $x(\ln x-1)$                                         |
| $\int \csc ax \, dx$                        | $-\frac{1}{a} \ln \lvert\csc ax+\cot ax\rvert$       |
#### T-substitution
Uses $t=\tan\left( \frac{x}{2} \right)$, for $f(\sin x,\cos x)$ which gives
$$\frac{dt}{dx}=\frac{1+t^{2}}{2}$$
and then
$$
\sin x=\frac{2t}{1+t^{2}},\quad \cos x=\frac{1-t^{2}}{1+t^{2}}
$$
There is also the other sub for trig-squared functions, $t=\tan x$ to give
$$
\sin x=\frac{t}{\sqrt{ 1+t^{2} }}
$$
### Series
A series $\sum u_{n}$ *converges absolutely* if $\sum |u_{n}|$ converges - this means that the series converges no matter what order the terms are summed in. However, if the series converges but $\sum |u_{n}|$ does not converge, then it is *conditionally convergent*, and therefore rearranging the order of the terms in the series can affect the result of the sum.

A common series expansion is [[Taylor series]].
### Limits
#calc/limits 
A vector sequence $(\mathbf{x}^{(1)},\mathbf{x}^{(2)},\dots)$ converges to $\mathbf{a}\in \mathbb{R}^{n}$ if for every $\epsilon>0$, $\exists N$ s.t. for every $k\geq N$, $|\mathbf{x}^{(k)}-\mathbf{a}|<\epsilon$. This is the basic limit definition for sequences #calc/limits-of-sequences. If $(\mathbf{a}^{(k)})$ and $(\mathbf{b}^{(k)})$ converge to $\mathbf{a},\mathbf{b}$ then we have the algebra of limits:
- The sum of the series has the limiting value $\mathbf{a}+\mathbf{b}$.
- In the 1-dimensional case, the product has the limiting value $ab$, and the quotient has the limiting value $a /b$ (for $b\neq 0$).
- The components of the vectors also converge individually in the same way.

For a function instead the definition of a limit is that if for every sequence $(\mathbf{x}^{(k)})$ in $U$ with $\lim_{ k \to \infty }(\mathbf{x}^{(k)})=\mathbf{a}$ we have $\lim_{ k \to \infty }f(\mathbf{x}^{(k)})=\mathbf{A}$ where $\mathbf{A}$ is the limiting value at $\mathbf{a}$. The same properties therefore hold for functions as they naturally extend series. (reminder: $f:U\to \mathbb{R}^{m},\,U\subset \mathbb{R}^{n}$)

#calc/continuous-function 
A function is continuous at a point $\mathbf{a}\in U$ iff 
$$
\lim_{ \mathbf{x} \to \mathbf{a} } f(\mathbf{x})=f(\mathbf{a})
$$
and if a function is continuous everywhere in $U$ then it is continuous on $U$. An alternative definition is that if $f(\mathbf{x})$ is [[Partial Differentiation#Total Derivative|totally differentiable]] at $\mathbf{x}$, then it is continuous at $\mathbf{x}$.

#calc/lhopitals-rule 
If in 
$$
L=\lim_{ x \to a } \frac{f(x)}{g(x)}
$$
$f(x)$ and $g(x)$ are both either $0$ or $\infty$, then we can differentiate the function - if the limit exists, it is equal to $L$ (provided function is differentiable/continuous over considered range).
