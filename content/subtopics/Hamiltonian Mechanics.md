---
tags:
  - mech/hamiltonian-mechanics
date-created: 2026-03-03
template-version: m.0
---
[[Mechanics]]

#mech/hamiltonian 
Hamiltonian mechanics is an extension to [[Lagrangian Mechanics]] that instead uses $p_{k}$, the generalised or *conjugate momenta* and $q_{k}$ (generalised coordinates) as its natural set of coordinates. The definition of the **Hamiltonian** is: 
$$
\mathcal{H} =\sum_{i=1}^{N} p_{i}\dot{q}_{i}-\mathcal{L} 
$$
where $\mathcal{L}$ is the lagrangian. Implicit in this relation is the secondary fact that
$$
\frac{d\mathcal{H}}{dt}=-\frac{ \partial \mathcal{L}  }{ \partial t } 
$$
so if $\mathcal{L}$ does not depend explicitly on $t$ (i.e. $t$ is *cyclic*), $\mathcal{H}$ is a constant of motion. Also, if the system is non-driven (total energy constant) and under influence of a conservative potential $U$ that does not depend on any $\dot{q}_{k}$, $\mathcal{H}$ is the total energy of the system. [[Lecture 2026-03-03 12pm.excalidraw|Proofs and derivations.]]
### Hamilton's equations
#mech/hamiltons-equations 
These are the natural counterpart to the [[Lagrangian Mechanics#Euler-Lagrange equation|ELE equations]] of lagrangian mechanics, and are:
$$
\frac{ \partial \mathcal{H}  }{ \partial p_{k} } =\dot{q}_{k}
$$
which links momenta to velocities, and
$$
\frac{ \partial \mathcal{H}  }{ \partial q_{k} } =-\dot{p}_{k}
$$
which contains the dynamics of the system. The first equation will usually restore the definition of the conjugate momenta ($p_{i}=\frac{ \partial \mathcal{L}  }{ \partial \dot{q}_{i} }$).

In comparison to lagrangian mechanics, which gives a set of $n$ 2nd order PDEs in $q,\dot{q}$ from the ELE equations, the Hamiltonian formalism gives $2n$, 1st order PDEs in $p,q$ which could be easier to solve, and possibly $\mathcal{H}$ as a constant of motion.