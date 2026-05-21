---
tags:
  - calc/ODE/particular-integral-and-complementary-function
date-created: 2025-12-30
template-version: m.0
---
The method of solving a linear equation in a vector space by using the linearity of the operators. 
### First order ODEs
#calc/ODE/1st-order-linear 
In the simpler
$$
y'+a(t)y=f(t)
$$
case, we want to find a particular solution and homogenous solution where
$$
\begin{align}
y_{h}'+a(t)y_{h} & =0 \\
y_{p}'+a(t)y_{p} & =f(t) \\
\implies \frac{d}{dt} (y_{p}+y_{h})+a(t)(y_{p}+y_{h}) & =f(t)
\end{align}
$$
so the general solution would be given by $y=y_{p}+y_{h}$.
We first solve the homogenous case, which is separable. Then, we can either guess at a likely solution for the particular case, or use 
#### Variation of constants
#calc/ODE/variation-of-constants 
This is simply the method of replacing the constant in the homogenous solution with a general $\psi(t)$ and substituting, then solving for $\psi$ by integrating.