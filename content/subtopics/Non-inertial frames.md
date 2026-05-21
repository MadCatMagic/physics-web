---
tags:
  - mech/non-inertial-reference-frame
date-created: 2026-01-20
template-version: m.0
---
If we transform to a frame $S'$ which is moving with a variable velocity $\vec{w}$, we have
$$
\begin{align}
\vec{r}' & =\vec{r}-\int \vec{w} (t)\, dt \\
\vec{v}'  & =\vec{v}-\vec{w}(t) \\
\vec{a}' & =\vec{a}-\frac{d\vec{w}(t)}{dt} \\
\vec{F}' & =\vec{F}-m \frac{d\vec{w}(t)}{dt}
\end{align}
$$
so there is a #mech/fictitious-force given by
$$
F_{\text{fic}}=-m \frac{d\vec{w}(t)}{dt}
$$
in the non-inertial frame.
### [[Rotating coordinate systems]]
Gives the example of a rotating coordinate frame and the associated *centrifugal* and *Coriolis* fictitious forces within that frame.