---
tags:
  - mech/lagrangian-mechanics
date-created: 2026-02-24
template-version: m.0
---
[[Mechanics]]

Is an alternative treatment compared to Newtonian mechanics that avoids the concept of force. It can be developed into the [[Hamiltonian Mechanics]] formalism.

Relies on *generalised coordinates* that are any set of parameters $q_{i}(t)$ that completely specify the system's momentary configuration. They are typically geometrical. There are also *generalised velocities* that are just $\dot{q}_{i}(t)=\frac{d}{dt}q_{i}(t)$. 

The number of degrees of freedom #mech/degrees-of-freedom is the number of independently variable generalised coordinates which is sufficient to completely describe the moment to moment system.
#### Configuration space
#mech/configuration-space 
For a system with $n$ DoF, it is the $n$-dimensional space whose points determine spatial positions of the system in time. Coordinates are $\vec{q}=(q_{1},\dots,q_{n})$. The path of an entire system is one single continuous trajectory in configuration space.
### [[Constraints]]
Serve to define the geometry of the problem by either reducing the degrees of freedom (*holonomic*) and defining *constraint forces* that can be found in several different ways.

### Euler-Lagrange equation
#mech/euler-lagrange-equation 
Basically describes the whole essence of the system. We first write the lagrangian #mech/lagrangian as
$$
\mathcal{L}(q_{1},\dots,q_{n},\dot{q}_{1},\dots,\dot{q}_{n}) =T-U
$$
where $T$ is the kinetic energy as a function of $\dot{q}_{i}$ and $U$ is the potential as a function of $q_{i}$, and then we substitute into the **Euler-Lagrange equations**
$$
\frac{d}{dt}\left( \frac{ \partial \mathcal{L}  }{ \partial \dot{q}_{i} }  \right)=\frac{ \partial \mathcal{L}  }{ \partial q_{i} } 
$$
to obtain $N_{\text{DoF}}$ equations from which conservation laws and equations of motion can then be derived.
#### Calculus of variations proof
#calc/calculus-of-variations
Considering a vector-valued path $f(t)$ such that $f(t_{0})=\mathbf{a}$, $f(t_{1})=\mathbf{b}$ are fixed endpoints. We want to find the path that results in stationary values of
$$
I=\int_{t_{0}}^{t_{1}} \mathcal{L(f(t),\dot{f}(t))}  \, dt 
$$
for some scalar function $\mathcal{L}$. $I$ is called a *functional* in this case. We can then introduce a small perturbation to $f$, $\delta f$ so $f(t)\to f(t)+\delta f(t)$ in just ONE element $f_{i}$ that holds the start and end points fixed. Then to first order, $\mathcal{L}\to \mathcal{L}+\delta \mathcal{L}(f, \dot{f})$ where
$$
\delta \mathcal{L} (f,\dot{f})= \frac{ \partial \mathcal{L}  }{ \partial f_{i} }\delta f_{i} + \frac{ \partial \mathcal{L}  }{ \partial \dot{f}_{i} } \frac{d}{dt}( \delta f_{i})+\mathcal{O} (\delta f_{i}^{2})
$$
is the first order Taylor expansion, using $\delta \dot{f}_{i}=\frac{d}{dt}\delta f_{i}$. Hence we can find a variation in the functional
$$
\delta I=\int_{t_{0}}^{t_{1}} \left[\frac{ \partial \mathcal{L}  }{ \partial f_{i} }\delta f_{i} + \frac{ \partial \mathcal{L}  }{ \partial \dot{f}_{i} } \frac{d}{dt}( \delta f_{i})\right] \, dt\overset{ ! }{ = }0
$$
Integrating second section by parts and using the fact that $\delta f_{i}(t_{0})=\delta f_{i}(t_{1})=0$ yields
$$
\delta I=\int_{t_{0}}^{t_{1}} \left[\frac{ \partial \mathcal{L}  }{ \partial f_{i} } + \frac{d}{dt}\left( \frac{ \partial \mathcal{L}  }{ \partial \dot{f}_{i} }  \right)\right] \delta f_{i}\, dt\overset{ ! }{ = }0
$$
which for $I$ to be stationary requires that $\delta I=0$ for any $\delta f_{i}$, and in general this should be true whatever $i$ we choose to vary, so we find the $N$ equations:
$$
\frac{ \partial \mathcal{L}  }{ \partial f } -\frac{d}{dt}\left( \frac{ \partial \mathcal{L}  }{ \partial \dot{f} }  \right)=0
$$
where obviously in the case of the lagrangian we take $f=q(t)$.
#### Hamilton's principle of stationary action
#mech/hamiltons-principle
States that a mechanical system evolves between points A and B in configuration space along the path which makes the **action** functional $I$ *stationary*, where the action is defined by the lagrangian $\mathcal{L}=T-U$.

Hence we can use this to define the equations of motion for any mechanical system under conservative forces, even those derived from time dependent potentials.
### Conjugate momenta and cyclic coordinates
Considering the above Euler-Lagrange equations, we define the *generalised* or **conjugate momenta** #mech/conjugate-momenta by
$$
p_{i}=\frac{ \partial \mathcal{L}  }{ \partial \dot{q}_{i} } 
$$
which can represent either linear or angular momenta. Notice this is the term being time-derived in the EL equations. In fact we can therefore rewrite them as
$$
\dot{p}_{i}=\frac{ \partial \mathcal{L}  }{ \partial q_{i} } \quad\text{where}\quad p_{i}=\frac{ \partial \mathcal{L}  }{ \partial \dot{q}_{i} } 
$$
this form shows us that if $\mathcal{L}$ does not depend on a specific $q_{i}$ explicitly this co-ordinate is called **cyclic** or *ignorable* #mech/cyclic-coordinates and we get:
$$
\frac{ \partial \mathcal{L}  }{ \partial q_{i} } =\dot{p}_{i}=0\implies p_{i}=\frac{ \partial \mathcal{L}  }{ \partial \dot{q}_{i} } =\text{const}
$$
so that this $p_{i}$ becomes a constant of motion - i.e. this particular momentum is conserved. *The momentum conjugate to a cyclic co-ordinate is a constant of motion*. This can be generalised to Noether's theorem:
### Noether's theorem
#mech/noethers-theorem 
This theorem states that whenever there is a continuous symmetry of the lagrangian, there is an associated conservation law. In particular, continuous symmetry means that a transformation of $q_{i}$ exists which leaves $\mathcal{L}$ unchanged and can be continuously applied. If $q_{i}$ is cyclic then as above, the corresponding momentum conjugate as conserved. This corresponds to a continuous transformation of $q_{i}\to q_{i}+\delta q_{i}$.

Considering a general transformation of $M\leq N$ different parameters,
$$
q_{k}(t)\to Q_{k}(s_{1},\dots,s_{M},t)=q_{k}+\sum_{i=1}^{M} \frac{ \partial Q_{k} }{ \partial s_{i} } s_{i}
$$
which is effectively a first order expansion on $q_{k}$, we find $M$ different **Noether charges** #mech/noether-charge 
$$
I_{k}=\sum_{i=1}^{M} p_{i} {\frac{ \partial Q_{i} }{ \partial s_{k} } }\biggr\rvert_{s=0}
$$
we can do this since we are expanding the $s_{k}$-derivative of $\mathcal{L}$ as:
$$
\frac{ \partial \mathcal{L}  }{ \partial s_{k} } =\sum_{i=1}^{N} \frac{ \partial \mathcal{L}  }{ \partial Q_{i} } \frac{ \partial Q_{i} }{ \partial s_{k} } +\frac{ \partial \mathcal{L}  }{ \partial \dot{Q}_{i} } \frac{ \partial \dot{Q}_{i} }{ \partial s_{k} } \overset{!}=0
$$
and are then substituting in Euler-Lagrange to get a total derivative, which simplifies to
$$
\sum_{i=1}^{N} \frac{ \partial \mathcal{L}  }{ \partial \dot{Q}_{i} } \frac{ \partial Q_{i} }{ \partial s_{k} } =\text{const}
$$
and then setting $s=0$ lets the first term go to $p_{i}$, so the whole expression becomes constant as above. Hence,
 *we get as many invariants as independent parameters in coordinate transforms which leave $\mathcal{L}$ invariant*.