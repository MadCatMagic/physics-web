---
tags:
  - mech/central-forces
  - "#mech/central-orbits"
date-created: 2026-02-02
template-version: m.0
---
A force is central if it
- acts along the radius vector $\vec{r}$,
- has magnitude dependent only on $r=|\vec{r}|$.
Hence
$$
\vec{F}_{\text{cent}}=f(r)\hat{r}
$$
Central forces are always [[Conservative forces|conservative]].
### Central orbits
For a central force we can find several useful properties:
- [[Rotational Dynamics|Angular momentum]] $\vec{J}=mr^{2}\dot{\theta}\hat{n}$ is conserved.
- Motion under a central force is *planar*.
- Keplar's laws hold.

We can also consider the energy to find
$$
E=\underbrace{ \frac{1}{2}m \dot{r}^{2} }_{ \text{radial motion} }+\underbrace{ \frac{1}{2}mr^{2}\dot{\theta}^{2} }_{ \text{azimuthal motion} }+\underbrace{ U(r) }_{ \text{potential} }
$$
also, the potential must be a function of $r$ only so
$$
U(r)=-\int_{r_{\text{ref}}}^{r} \vec{F}_{cent}\cdot  d\vec{r} =-\int_{r_{\text{ref}}}^{r} f(r') \, dr' 
$$
where we usually take $r_{ref}=\infty$ to lose the constant term in the potential.
#### Effective potential method
#mech/effective-potential
We can also rewrite the azimuthal energy in terms of the angular momentum to find
$$
E=\frac{1}{2}m \dot{r}^{2}+\frac{J^{2}}{2mr^{2}}+U(r)
$$
which becomes a decoupled one-variable equation. We can take this further by defining the *effective potential* $U_{\text{eff}}(r)=\frac{J^{2}}{2mr^{2}}+U(r)$, hence
$$
\frac{1}{2}m \dot{r}^{2}=E-U_{\text{eff}}(r)
$$
which means $E\geq U_{\text{eff}}(r)$ which limits the $r$ that can be reached in central orbits. Note that we have reduced a 2d problem potential to a 1d potential.
#### Hamiltonian of central motion
Using the [[Hamiltonian Mechanics]] formalism we can find the Hamiltonian as
$$
\mathcal{H} =\sum_{i=1}^{N} p_{i}\dot{q}_{i}-\mathcal{L} =p_{r} \dot{r}+p_{\theta}\dot{\theta}-\left( \frac{1}{2}m \dot{r}^{2}+\frac{1}{2}mr^{2}\dot{\theta}^{2}-V(r) \right)
$$
using the $r$, $\theta$ generalised coordinates. By considering the [[Lagrangian Mechanics#Conjugate momenta and cyclic coordinates|conjugate momenta]] we find the relations $p_{r}=m \dot{r}$ and $p_{\theta}=mr^{2}\dot{\theta}$ and then we can substitute to find $\mathcal{H}$ only in terms of its natural parameter set which gives
$$
\mathcal{H} =\frac{1}{2}\left( \frac{p_{r}^{2}}{m}+\frac{p_{\theta}^{2}}{mr^{2}} \right)+V(r) 
$$
Since $\mathcal{L}$ does not depend explicitly on $t$ and it is a free body, $\mathcal{H}$ gives the total energy and is a conserved quantity. The second Hamilton equation $-\dot{p}_{k}=\frac{ \partial \mathcal{H} }{ \partial q_{k} }$ then gives the equations:
$$
\dot{p}_{r}=\frac{p_{\theta}^{2}}{mr^{3}}-\frac{ \partial V }{ \partial r } 
$$
and $\dot{p}_{\theta}=0$ which tells us angular momentum $J=p_{\theta}$ is conserved and therefore we find the EOM as
$$
m \ddot{r}=\frac{J^{2}}{mr^{3}}-\frac{ \partial V }{ \partial r } 
$$
which matches energy or N2 derivation.
### Orbit equation
#mech/orbit-equation
Closely related to [[Rotational Dynamics]].
The orbit equation for gravitational attraction is the classic
$$
r(\theta)=\frac{r_{0}}{1+e\cos(\theta)}
$$
which is the general form of a conic section:
- $e=0$ is a circle ($E=-\frac{GMm}{2a}$),
- $0<e<1$ is an ellipse ($-\frac{GMm}{2a}<E<0$),
- $e=1$ is a parabola ($E=0$),
- $e>1$ is a hyperbola ($E>0$).
And $r_{0}=\frac{b^{2}}{a}=a(1-e^{2})$ relates the two constants of dimension for the conic section. Note $b=a\sqrt{ 1-e^{2} }$ for an ellipse.

If we initially note that the energy in a gravitational system (as a special case of the above equation) is
$$
E=\frac{1}{2}m \dot{r}^{2}+\frac{J^{2}}{2mr^{2}}-\frac{GMm}{r}
$$
then the total energy in an orbital system is given by
$$
E=-\frac{GMm}{2a}
$$
and we can find the orbital components in terms of $E$ and the angular momentum $J$ as:
$$
e=\sqrt{ 1+ \frac{2EJ^{2}}{m\alpha^{2}} }
$$
and
$$
a=-\frac{\alpha}{2E}
$$
where $\alpha=GMm$. We also then have that $J=\sqrt{ \alpha mr_{0} }$.
#### Vis-viva
The useful vis-viva equation is
$$
v^{2}=GM\left( \frac{2}{r}-\frac{1}{a} \right)
$$
where $a$ is the semi-major axis, $r$ is the distance from the focus at that point, $v$ is the velocity at that point of the orbiting object. This can be derived from energy - only use two of energy conservation, angular momentum, vis-viva because two can always derive the third. Also geometry is always useful.
#### Elliptical orbits
#mech/elliptical-orbit
As described above are mainly characterised by the eccentricity
$$
e=\sqrt{ 1-\frac{b^{2}}{a^{2}} }
$$
distances to apo/periapsis are $r_{a/p}=a(1\pm e)$.
#### Hyperbolic orbits
#mech/hyperbolic-orbit
In this case $e>1$ and instead, $b^{2}=a^{2}(e^{2}-1)$. $b$ is often described as the impact parameter because it has two separate meanings:
![[Pasted image 20260223180348.png|400]]
### Keplar's laws
#mech/keplars-laws 
#### 1st law
Orbits are conic sections under gravitational attraction. (or any $\frac{1}{r^{2}}$ attractive force).
#### 2nd law
Central orbits sweep out equal areas in equal times. In other words,
$$
\begin{align}
\frac{dA}{dt} & =\frac{1}{2}r \frac{dr}{dt}\sin\alpha \\
 & =\frac{|\vec{J}|}{2m}=\text{const}
\end{align}
$$
since $\vec{J}$ is constant in central orbital motion. Note that this is true *for all* central orbits in which $|\vec J|$ is conserved, not just gravitational ones. 
#### 3rd law
Is the formula
$$
T^{2}=a^{3} \frac{4\pi^{2}}{GM}
$$
is a classic. This is in the 1 body case, but 
### 2 body problem
#mech/two-body-problem 
Supposing we have two orbiting bodies with masses and positions $m_{1}$, $m_{2}$, $\vec{r}_{1}$, $\vec{r}_{2}$ with respect to some origin. If we choose [[Centre of Mass]] as origin then we get
$$
m_{1}\vec{v}_{1}+m_{2}\vec{v}_{2}=0
$$
And then by definition, $\vec{F}_{12}=m_{1} \ddot{\vec{r}}_{1}$ and $\vec{F}_{21}=m_{2} \ddot{\vec{r}}_{2}$ and then
$$
\vec{F}_{12}=-\vec{F}_{21}= \frac{Gm_{1}m_{2}}{|\vec{r}|^{2}}\hat{r}
$$
for the separation vector $\vec{r}=\vec{r}_{2}-\vec{r}_{1}$ hence
$$
\ddot{\vec{r}}=\ddot{\vec{r}}_{2}-\ddot{\vec{r}}_{1}= \vec{F}_{21}\left( \frac{1}{m_{1}}+\frac{1}{m_{2}} \right)
$$
where we have defined the **reduced mass** as $\mu=\left( \frac{1}{m_{1}}+\frac{1}{m_{2}} \right)^{-1}$. We therefore get the mutual equation of motion
$$
\mu \ddot{\vec{r}}=-\frac{G\mu(m_{1}+m_{2})}{|\vec{r}|^{2}}\hat{r}
$$
This shows that any two body problem is analogous to a single body with reduced mass $\mu$ orbiting a stationary body with effective mass $m_{1}+m_{2}=M$, and
$$
\vec{r_{1}}=-\frac{m_{2}}{m_{1}+m_{2}}\vec{r},\quad \vec{r}_{2}=\frac{m_{1}}{m_{1}+m_{2}}\vec{r}
$$
so both orbits have the same ellipticity but scaled $\vec{r}_{0}$. With regards to Keplar's third law, for a 2 body system we instead find
$$
T^{2}=\frac{4\pi^{2}}{G(m_{1}+m_{2})}(a_{1}+a_{2})^{3}
$$
where $a_{1}$, $a_{2}$ are the individual semi-major axes. Additionally the total energy of the orbit is the same and is therefore
$$
E=-\frac{G\mu M}{2a}
$$
but here $a=a_{1}+a_{2}$ is the 'total' equivalent semi-major axis.