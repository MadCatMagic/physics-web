---
tags:
  - optics/diffraction-grating
date-created: 2026-03-09
template-version: m.0
---
[[Optics#Fraunhofer conditions & diffraction]]

If we consider waves incident on a diffraction grating that are perpendicular to the grating so arrive in phase on the surface, then at some angle $\theta$ from the normal, parallel waves in that direction will interfere at $\infty$ to form some interference pattern. 

Considering the phase different for different points of diffraction from the grating, that are separated by a horizontal distance $a$, we have
$$
\delta_{p}=\delta_{0}+pna\sin\theta
$$
is the optical path length for the $p$th reflected wave. Then at $\infty$, the total wave function is
$$
\psi=\sum_{p=0}^{N-1} \psi_{p}=\sum_{p=0}^{N-1} Ae^{i(\omega t-k_{0}\delta_{p}+\phi_{0})}
$$
expanding and substituting in $\delta$, we find a geometric series which can be evaluated and then the intensity found as
$$
\begin{align}
I  =\frac{\psi \psi ^{*}}{2} & =\frac{A^{2}}{2}\left( \frac{\sin\left( \frac{N}{2}k_{0}na\sin\theta \right)}{\sin\left( \frac{1}{2}k_{0}na\sin\theta \right)} \right)^{2} \\[1ex]
 & =N^{2}I_{0}\left( \frac{\sin\left(\pi  \frac{Na}{\lambda}\sin\theta \right)}{N\sin\left(\pi  \frac{a}{\lambda}\sin\theta \right)} \right)^{2}
\end{align}
$$
using $k=\frac{2\pi}{\lambda}$ and setting $A^{2}=2I_{0}$. 

This function has quite complex behaviour, but we note that if we let $\pi a\sin\theta /\lambda=y\ll 1$ be small, the fraction reduces to $1$ and so *the function is maximised* when 
$$
\sin\theta=\frac{m\lambda}{a},\quad m\in \mathbb{Z}
$$
If $y$ is large instead, we have rapid oscillatory behaviour depending on $N$ - larger $N$ implies decreased peak width and decreased secondary amplitude:
![[Pasted image 20260309165651.png|400]]
##### Practical observations
Again we require two mirrors to focus the image from infinity to a screen, and to collimate the point source - the source should be in phase to work properly.