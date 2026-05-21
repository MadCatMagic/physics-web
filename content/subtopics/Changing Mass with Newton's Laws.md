---
tags:
  - mech/newtons-laws
  - mech/changing-mass
date-created: 2026-01-19
template-version: m.0
---
In general this situation is characterised by
1. having to write an expression for the change in momentum $\delta p$ in a particular instant
2. Setting $\delta p=\sum F_{external}$
3. Dividing through by $\delta t$ and taking the limit to find a differential equation (need to be careful whether derivatives should be positive or negative)
4. Solving the equation

#### Rocket equation
For example, if we consider a rocket in a vacuum where it is ejecting mass then we have the momentum conservation of
$$
\begin{align} \\
\delta p & =p_{\text{final}}-p_{\text{initial}} \\
 & =(m-\delta m)(v+\delta v)+\delta m(v-w)-mv \\
 & =m\delta v-w\delta m
\end{align}
$$
Dividing by $\delta t$, taking the limit and noting that since $\delta m$ is positive, but we are assuming mass is decreasing so $\frac{dm}{dt}$ is negative, we need to have $\frac{\delta m}{\delta t}=-\frac{dm}{dt}$ so
$$
\frac{dp}{dt}=m \frac{dv}{dt}+w \frac{dm}{dt}
$$
which can be analysed providing we have some additional other condition.
##### F=0 case
In this case we can solve the equation to find the rocket equation
$$
v_{f}-v_{i}=w\ln\left( \frac{m_{i}}{m_{f}} \right)
$$
##### F=mg case
Here, if $F=mg$ and we let $m=m_{0}-\alpha t$ for some rate of fuel usage $\alpha t$, we find that
$$
\frac{dp}{dt}=(m_{0}-\alpha t)g=(m_{0}-\alpha t) \frac{dv}{dt}-w\alpha
$$
which solves to
$$
v_{f}-v_{i}=-g(t_{f}-t_{i})-w\ln \frac{m_{0}-\alpha t_{f}}{m_{0}-\alpha t_{i}}
$$
which is equivalent to if we just considered it as an accelerating reference frame.


