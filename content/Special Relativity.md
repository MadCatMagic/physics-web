---
tags:
  - relativity
  - relativity/special-relativity
date-created: 2025-11-11
template-version: m.0
---
[[Special Relativity L_MT1]]
[[Galilean Relativity]] is the precursor to special relativity.
#### Postulates of relativity
#relativity/postulates-of 
1. Laws of physics the same in all IRF
2. c is the same in all IRF
Hence,
- massive particles have speed $v< c$ in all IRF
- massless particles travel at speed $c$ in all IRF

### Invariant Interval
 #relativity/invariant-interval
 Is defined
 $$
s^{2}=c^{2}\Delta t^{2}-\Delta x^{2}-\Delta y^{2}-\Delta z^{2}
$$
and is *invariant* under Lorentz transformations - is an interval between two 4-points $E_{1}=(t_{1},x_{1},y_{1},z_{1})$ and $E_{2}=(t_{2},x_{2},y_{2},z_{2})$.
This interval is the *metric* of the *Minkowsky space*, which is a specialisation of $\mathbb{R}^{4}$. #relativity/minkowsky-space
- if $s=0$ the events are 'light-like' and exist in each other's light-cone. #relativity/light-like
- if $s<0$ the events are 'space-like' and there exists a reference frame where they occur simultaneously in time. #relativity/space-like
- if $s>0$ the events are 'time-like' and there exists an IRF where they occur at same point in space. #relativity/time-like
If $s\geq {0}$ this is the only way there can be a causal connection as information travels $\leq c$. #relativity/causality

### Lorentz transformations
#relativity/lorentz-boost #relativity/lorentz-transformation #relativity/lorentz-group
We can define the **Lorentz boost**
$$
\begin{pmatrix}
ct' \\
x'
\end{pmatrix}=\begin{pmatrix}
\gamma & -\frac{v}{c}\gamma \\
-\frac{v}{c}\gamma & \gamma
\end{pmatrix}\begin{pmatrix}
ct \\
x
\end{pmatrix}
$$
The $S$ reference frame here is the one being boosted out of so $S'$ is the rest frame of the boosted object, $S$ is the observing frame *$S'$ is the moving frame*. This is a member of the **Lorentz group**, in that it preserves the invariant interval. A general **Lorentz transformation** may be any composition of boosts or reflections and will always satisfy
$$
\Lambda^{T}\eta\Lambda=\eta,\quad \eta=\text{diag}(1,-1,-1,-1)
$$
The simple Lorentz boost yields the *Lorentz transformation* set
$$
\begin{align}
x' & =\gamma(x-vt) \\
y' & =y \\
z' & =z \\
t' & =\gamma\left( t-\frac{xv}{c^{2}} \right)
\end{align}
$$
The final relation tells us that events in $S'$ will occur at different times depending on their x location that were simultaneous in $S$, specifically differing by the factor $\frac{xv}{c^{2}}$ in $S$.
#### Rapidity
#relativity/rapidity
We can instead parametrise the boost in terms of the **rapidity** $\phi$:
$$\begin{align}
\sinh \phi & =\frac{\beta}{\sqrt{ 1-\beta^{2} }} \\[1ex]
\cosh \phi & =\frac{1}{\sqrt{ 1-\beta^{2} }} \\[1ex]
\tanh \phi & =\beta \\[1ex]
\Lambda & =\begin{pmatrix}
\cosh \phi & \sinh \phi \\
\sinh \phi & \cosh \phi
\end{pmatrix}
\end{align}

$$
where we have defined $\beta=\frac{v}{c}$. 

If we have a constantly accelerating spaceship with acceleration $a(t)$, and we consider a small velocity change (using addition formula defined below):
$$
v(t+dt)=\frac{v(t)+a(t)\ dt}{1+v(t)a(t)\ dt /c^{2}}
$$
expanding this out in first order of $dt$ then gives
$$
\frac{dv}{dt}=a(t)\left( 1-\frac{v(t)^{2}}{c^{2}} \right)
$$
hence
$$
v(t)=c\tanh\left( \frac{1}{c} \int_{0}^{t} a(t) \, dt  \right)
$$
and therefore the rapidity can be defined as
$$
\phi(t)=\frac{1}{c}\int_{0}^{t} a(t) \, dt 
$$
#### Combining velocities
#relativity/combining-velocities
When composing Lorentz boosts, *rapidities add up* - e.g.
$$
\frac{u}{c}=\tanh(\phi_{w}+\phi_{v})=\frac{\tanh \phi_{w}+\tanh \phi_{v}}{1+\tanh \phi_{w}\tanh \phi_{v}}=\frac{w+v}{1+\frac{wv}{c^{2}}}
$$
gives the combining velocities formula directly. For transverse velocity combination there are the additional formulas
$$
\begin{align}
w_{y} & =\frac{w_{y}'}{\gamma_{v}\left( 1+\frac{vw_{x}'}{c^{2}} \right)} \\
w_{z} & =\frac{w_{z}'}{\gamma_{v}\left( 1+\frac{vw_{x}'}{c^{2}} \right)}
\end{align}
$$
for a velocity $\vec{w}'=(w_{x}',w_{y}',w_{z}')$ measured in $S'$, that is being observed in a frame $S$ with $S'$ moving with a velocity $v$ relative it, to find $\vec{w}$.
#### Space-time diagram
#relativity/space-time- #relativity/world-line #relativity/light-cone
We can draw events in the $x,t$ plane as a space time diagram. Examples in notes. The **world line** is the actual path that a particle travels through, constrained by the **light cone** of every event along the path for a *time-like* object.

When we draw a velocity boost in the diagram it will have $x'$ and $t'$ axes given by
$$
\begin{align}
x' & =\beta t \\
t' & =\frac{x}{\beta}
\end{align}
$$
in spacetime units.
### Time and Length
#relativity/time-dilation #relativity/proper-time
**Time dilation** is that 
$$
\Delta t'=\gamma \Delta \tau
$$
where $\tau$ is the **proper time** (time in the IRF where object is stationary), and $t'$ is the time observed by an observer moving relative to object. $\tau$ is the *quickest* that time can be measured - moving clocks tick slower.

> [!info]- Proof using only invariant interval
> Let a clock be stationary in frame $S'$ which moves at speed $v$ with respect to frame $S$, then invariant interval says that for the clock,
> $$(c\Delta t')^{2}=c^{2}\Delta t^{2}-(\Delta x^{2}+\Delta y^{2}+\Delta z^{2})$$
> so
> $$\left( \frac{\Delta t'}{\Delta t} \right)^{2}=1-\frac{\Delta x^{2}+\Delta y^{2}+\Delta z^{2}}{c^{2}\Delta t^{2}}=1-\frac{v^{2}}{c^{2}}=\frac{1}{\gamma^{2}}$$
> hence $\Delta t=\gamma\Delta t'$ is the standard time dilation result.

We can generalise proper time as
$$
\tau=\sum_{i} \frac{\Delta t_{i}}{\gamma_{i}}=\frac{1}{c}\sum_{i} \Delta s_{i}
$$
by taking segments of proper time along world line. This converts to
$$
\tau=\int \frac{1}{\gamma(v(t))} \, dt=\frac{1}{c}\int  \, ds  
$$
and hence $\tau$ depends on the world-line.

#relativity/length-contraction #relativity/proper-length
**Length contraction** is that
$$
l'=\frac{l_{0}}{\gamma}
$$
so the **proper length** $l_{0}$ is the longest length and moving objects 'contract'.

## [[4 Vectors]]
Including *4-velocity*, *4-acceleration*, *newtons-laws*
Leads directly to
## [[Momentum and Energy]]
Including *4-momentum*, *massless particles*, *longitudinal doppler shift*.
### Calculations
#relativity/decays *Decays* occur when a particle decays into multiple others. #relativity/collisions *Collisions* occur when multiple particles collide, resulting in some state afterwards. #relativity/inelastic-collisions *Inelastic collisions* are different to regular mechanics in that total energy is still conserved but particles may gain mass as some energy is converted to mass. 
#relativity/compton-scattering *Compton scattering* is the common interaction $e^{-}\gamma\to\gamma e^{-}$ resulting in the photon's frequency changing.

#### Threshold energy
#relativity/threshold-energy 
The minimum energy for an interaction to occur (usually for a particular incident particle) and can be found as in the minimum energy state, the resulting particles will be stationary in the zero-momentum frame.