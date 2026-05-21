---
tags:
  - elecmag
date-created: 2026-01-19
template-version: m.0
---
[[Physics]]
[[Electromagnetism L_HT1]]
[[Electromagnetism Textbooks]]
## Electric fields
#elecmag/coulombs-law 
Denotes the relationship of forces between point charges. In particular,
$$
\vec{F}_{12}=\frac{1}{4\pi\epsilon_{0}} \frac{q_{1}q_{2}}{r^{2}} \hat{r}_{12}
$$
is the force on $q_{2}$ due to $q_{1}$, where $\hat{r}_{12}$ points from $q_{1}$ to $q_{2}$.

#elecmag/superposition 
Since this is linear, we can superpose multiple charges very easily, and the net force is simply the sum over all these individual forces. This same principle holds for electric fields, potential, work done etc - anything linear in charge.
### Electric field & potential
#elecmag/electric-field 
Is defined as $\vec{E}_{j}=\frac{\vec{F}_{j}}{q_{j}}$ and is a [[Conservative forces|conservative field]]. The work done is then
$$
W_{AB}=-q\int_{\vec{v}_{A}}^{\vec{v}_{B}}\vec{E}\cdot   d\vec{l}=\frac{qQ}{4\pi\epsilon_{0}}\left[ \frac{1}{r_{B}}-\frac{1}{r_{A}} \right]
$$
for a single charge, but adds up linearly (obviously). Since the field is conservative, **for electrostatics** (not time dependent) $\oint \vec{E}\cdot d\vec{l}=0$.

#elecmag/electric-potential 
Then defining the potential as $V_{AB}=\frac{W_{AB}}{q}$, if we have some reference point $\vec{r}_{0}$, often set to $\infty$ then
$$
V(\vec{r})=\frac{q}{4\pi\epsilon_{0}} \frac{1}{r}
$$
This can also be written as $\vec{E}(\vec{r})=-\nabla V(\vec{r})$ using the [[Gradient]] function. Since potential is linear and scalar, it is often easier to sum potentials then take the gradient to find the field.

#elecmag/total-potential-of-system 
The total potential of a system of charges can be found as
$$
U=\frac{1}{8\pi \epsilon_{0}}\sum_{i}q_{i}\sum_{j\neq i} \frac{q_{j}}{r_{ij}}=\frac{1}{2}\sum_{i}q_{i}V_{i}
$$
where $V_{i}$ is the sum of potentials at $q_{i}$ from all the *other* charges.
#### Continuous charge distribution
#elecmag/continuous-charge-distribution 
In the case of continuous charge, we integrate over the infinitesimal charges $dq$:
$$
V(\vec{r})=\frac{1}{4\pi\epsilon_{0}}\int \frac{dq}{|\vec{r}-\vec{r}_{q}|}
$$
and
$$
\vec{E}(\vec{r})=\frac{1}{4\pi\epsilon_{0}}\int \frac{dq}{|\vec{r}-\vec{r}_{q}|^{2}}\cdot \frac{\vec{r}-\vec{r}_{q}}{|\vec{r}-\vec{r}_{q}|}
$$
Over a volume $V$, we have $dq=\rho\ dV$, for a surface $S$ this is $dq=\sigma\,dA$ and for a line $L$, this is $dq=\lambda\, dl$ where $\rho,\sigma,\lambda$ represent different dimensions of charge density.
### [[Electrostatics]]
Includes *electric multipoles*, *poisson* and *laplaces equations*, *uniqueness theorem* and *method of images*, *conductors*.
## Magnetic fields
#elecmag/magnetic-field #elecmag/magnetic-flux-density
Instead of electric field strength we have *magnetic flux density* $\vec{B}$ where $[B]=\text{T}$ the tesla, and *magnetic field strength* is then $\vec{H}=\frac{1}{\mu}\vec{B}$, $[H]=\text{Am}^{-1}$.
### [[Magnetostatics]]
Includes *boundary conditions*, *biot-savart law*, *magnetic dipoles*, *magnetic potential*.
### Charge conservation
#elecmag/continuity-equation 
Considering a volume $\mathcal{V}$ bounded by a surface $\mathcal{S}$, charge should be conserved so
$$
\oint_{\mathcal{S} }\vec{J}\cdot d\vec{a}=I=-\frac{dQ}{dt}
$$
Using the divergence equation and considering the charge density $\rho$, we can find the **continuity equation**
$$
\nabla\cdot \vec{J}=-\frac{ \partial \rho }{ \partial t } 
$$
which is the conservation of charge in differential form.
### [[Induction]]
Includes *emf*, *Faraday's law*, *Lenz's law*, *self-inductance*, *mutual inductance*.
## [[Maxwell's equations]]
The most general form of EM, contains *gauss's law*, *ampere's law*, *maxwell-faraday's law*, *energy density*.
### [[Motion in electromagnetic fields]]
Discusses the motion of a charged particle $q$ through electromagnetic fields.
### [[Electromagnetic wave]]
About electromagnetic waves in a vacuum devoid of charge or current. 