---
tags:
  - elecmag/waves
date-created: 2026-03-17
template-version: m.0
---
[[Electromagnetism#Maxwell's equations]]
[[Wave Motion]]

In a vacuum, in absence of charge or current, $\rho=0$ and $\vec{J}=0$. This allows us to derive from the symmetries in [[Maxwell's equations]] under this regime a pair of [[Wave Motion#Wave equation|standard wave equations]]
$$
\begin{align}
\nabla^{2}\vec{B} & =\epsilon_{0}\mu_{0} \frac{ \partial^{2} \vec{B} }{ \partial t^2 }  \\
\nabla^{2}\vec{E} & =\epsilon_{0}\mu_{0} \frac{ \partial^{2} \vec{E} }{ \partial t^2 } 
\end{align}
$$
which can be solved in the usual wave equation ways. We will consider plane waves which have the general form
$$
\vec{F}=\vec{F}_{0}\exp i(\omega t-\vec{k}\cdot \vec{r})
$$
in three dimensions (for some variable $\vec{F}$), and the real part denotes the actual physical behaviour of the wave. $\vec{k}$ is a direction normal to the wave-fronts and as with waves, $\lambda =\frac{2\pi}{k}$. The phase velocity of the wave-fronts is given by
$$
c=\frac{\omega}{k}=\frac{1}{\sqrt{ \epsilon_{0}\mu_{0} }}
$$
where in this case $c$ is the speed of light in a vacuum - universal constant.

If we substitute our solution into the Gauss's laws then since there is no charge or current, we find
$$
\begin{align}
\nabla\cdot \vec{E} & =-i\,\vec{k}\cdot \vec{E}=0 \\
\nabla\cdot \vec{B} & =-i\,\vec{k}\cdot \vec{B}=0
\end{align}
$$
so $\vec{E}\perp \vec{k}$ and $\vec{B}\perp \vec{k}$ and then considering other Maxwell equations we find
$$
\begin{align}
\nabla \times \vec{E}=-\frac{ \partial \vec{B} }{ \partial t } &  \implies \vec{B}=\frac{1}{\omega}\vec{k}\times \vec{E} \\[1ex]
\nabla \times \vec{B}=\mu_{0}\epsilon_{0}\frac{ \partial \vec{E} }{ \partial t }  & \implies \vec{E}=-\frac{c^{2}}{\omega}\vec{k}\times \vec{B}
\end{align}
$$
so $\vec{E}$, $\vec{B}$, $\vec{k}$ are mutually orthogonal and the ratio of magnitudes is
$$
\frac{|\vec{E}|}{|\vec{B}|}=\frac{|\vec{E}_{0}|}{|\vec{B}_{0}|}=\frac{c^{2}}{\omega}k=c=\frac{1}{\sqrt{ \mu_{0}\epsilon_{0} }}
$$
this gives us a total description of the behaviour of the waves in this situation - in phase, perpendicular transverse oscillations.

### Characteristic impedance of free space
#elecmag/characteristic-impedance-of-free-space 
Is defined as
$$
Z=\frac{|\vec{E}|}{|\vec{H}|}=\mu_{0}c=\sqrt{ \frac{\mu_{0}}{\epsilon_{0}} }=376.7\,\ohm
$$
### Polarisation
#elecmag/waves/polarisation 
There are several different types of polarisation
- for linearly/plane polarised waves, $\vec{E}$ has one specific orientation.
- for circularly polarised waves, there are two linear components of $\vec{E}$ superimposed at a right angle and phase shifted by $\frac{\pi}{2}$ so
$$
\begin{pmatrix}
E \\
0 \\
0
\end{pmatrix}\sin\omega t+\begin{pmatrix}
0 \\
E \\
0
\end{pmatrix}\sin\left( \omega t+\frac{\pi}{2} \right)=E\begin{pmatrix}
\sin\omega t \\
\cos\omega t \\
0
\end{pmatrix}
$$
- elliptically polarised waves are the same but unequal amplitudes are superimposed.
- unpolarised waves have $\vec{E}$ superimposed with all orientations, so there is no fixed phase relationships.