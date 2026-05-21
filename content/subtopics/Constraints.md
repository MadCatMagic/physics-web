---
tags:
  - "#mech/constraints"
date-created: 2026-03-02
template-version: m.0
---
[[Lagrangian Mechanics]]

Constraints and the constrained n-system are *holonomic* and *scleronomous* if
- constraints independent of time (scleronomous)
- can be written as a mix of:
	- $f_{k}(q_{1},\dots,q_{3n})=0,\quad k=1,2\dots,r\leq 3n$ which are hyperplanes in the space
	- $f_{k,1}(q_{1},\dots,q_{3n})=0$, $f_{k,2}(q_{1},\dots,q_{3n})=0$ for $k=1,2,\dots ,r\leq \frac{3}{2}n$ which are hyper curves.
- which are both geometrical shapes to which movements of particles are constrained to.
- Using only $q_{i}$ in constraints guarantees DoF reduces to $N=3n-r$ in constrained system, which is what makes constraints holonomic.

#mech/constraint-forces 
We could express these constraints via **constraint forces** $F'$ so for bodies in the system $m_{i} \ddot{r}_{i}=F_{i}+F_{i}'$.
### Finding constraints via constraining potentials
#mech/constraining-potentials 
One way of finding constraints is to un-constrain the constrained variable $q_{k}$ and introduce a potential term $V(q_{k})$ into the lagrangian, so we have $\mathcal{L}'=T-U-V(q_{k})=\mathcal{L}-V(q_{k})$. Then we have an additional [[Lagrangian Mechanics#Euler-Lagrange equation|Euler-Lagrange equation]] which allows us to define the constraint force $Q_{k}=-\frac{ \partial V }{ \partial q_{k}}$ so that
$$
\frac{d}{dt}\left( \frac{ \partial \mathcal{L}  }{ \partial \dot{q}_{k} }  \right)=\frac{ \partial \mathcal{L}  }{ \partial q_{k} } -Q_{k}
$$
### Finding constraints via Lagrange multipliers
#mech/lagrange-multiplier
If we assume scleronomous $F'$ only act $\perp$ to trajectories of particles then $F'$ never do any work on bodies. This perpendicularity allows determining $F'$ from $f$ via:
$$
F'_{i,k}=\lambda\frac{ d}{dq_{i}}(f_{k})\implies F'_{k}=\lambda \nabla f_{k}\quad(k=1,2,\dots,r\leq 3n)
$$
where $\lambda$ is an arbitrary **Lagrange multiplier**. 

More specifically, we implement the constraint by not constraining any variables instead writing a new lagrangian as
$$
\mathcal{L} '=T+U+\lambda f(q_{i},\dots,q_{n},t)
$$
which equals $\mathcal{L}$ since by definition of constraints, $f=0$. Treating $\lambda$ as a new coordinate allows us to find the constraint forces as above by
$$
Q_{i}=\lambda \frac{ \partial f }{ \partial q_{i} } 
$$
for that constraint.

**proof????**.