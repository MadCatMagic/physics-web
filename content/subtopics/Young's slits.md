---
tags:
  - optics/youngs-slits
date-created: 2026-03-09
template-version: m.0
---
[[Optics#Fraunhofer conditions & diffraction]]

In this specific case we have two source slits separated by a distance $a$, and a flat screen a distance $D$ away. For a position from the central axis (directly between the slits) $y$ along the screen, we can consider the total wave combination at that point as
$$
\begin{align}
\psi_{\text{tot}}(y) & =\psi_{1}(y)+\psi_{2}(y) \\[1ex]
 & =A\cos(\omega t-k_{0}\delta_{1}+\phi_{1})+A\cos(\omega t-k_{0}\delta_{2}+\phi_{2}) \\[1ex]
 &=2A\cos\left( \omega t-\frac{k_{0}(\delta_{1}+\delta_{2})+(\phi_{1}+\phi_{2})}{2} \right)\cos\left( \frac{k_{0}(\delta_{2}-\delta_{1})+(\phi_{1}-\phi_{2})}{2} \right)
\end{align}
$$
which then yields an intensity of 
$$
I(y)=2A^{2}\cos ^{2} \frac{1}{2}(k_{0}(\delta_{2}-\delta_{1})+(\phi_{1}-\phi_{2}))
$$
and since at the origin (the slits) the intensities of each wave must be equal so 
$$
I_{0}=\langle A^{2}\cos ^{2}(\dots) \rangle=\frac{A^{2}}{2} 
$$
we can then rewrite this as
$$
I(y)=2I_{0}[1+\cos(k_{0}(\delta_{2}-\delta_{1})+\phi_{1}-\phi_{2})]
$$
where $\delta_{1}$ and $\delta_{2}$ are functions of $y$, since that determines the path length. 
#### $\phi_{1}=\phi_{2}$ and double slit geometry
Examining then the geometry of the situation we can expand the path lengths $l_{1,2}$ to first order since we are assuming $y$ small and $D\gg y,a$ to find
$$
\delta_{2}-\delta_{1}=\frac{na}{D}y
$$
and then using $nk_{0}=k=\frac{2\pi}{\lambda}$ we get
$$
I(y)=2I_{0}\left( 1+\cos\left( \frac{2\pi}{\lambda} \frac{a}{D}y \right) \right)
$$
which shows an oscillating pattern of minima and maxima between $4I_{0}$ and $0$, with distance between adjacent maxima given by
$$
\Delta y=\frac{\lambda D}{a}
$$
#### Multiple wavelengths
Considering that $\Delta y\propto\lambda$ it is clear that if we have multiple wavelengths or even a continuous spectrum as in sunlight we will have different diffraction patterns overlaying on one another, which creates coloured fringes.
#### Angled incident radiation
If the incident radiation is angled $\gamma$ from perpendicularly into the slits, we can find that the phase change due to the wavefront reaching each slit at different times is $\phi_{1}-\phi_{2}=k_{0}na\sin\gamma$ which when substituted into the intensity equation above (keeping the same $\delta_{2}-\delta_{1}$ from the first case) gives:
$$
I(y)=2I_{0}\left( 1+\cos\left( \frac{2\pi}{\lambda} \frac{a}{D}y +\frac{2\pi}{\lambda}a\sin\gamma\right) \right)
$$
so the pattern will be shifted in the negative $y$-direction by $D\sin\gamma$ on the screen (for positive $\gamma$ measured CCW from the positive y-axis).
#### Practical observations
To actually observe this pattern, we require a lens both to focus light from a point source to be collimated and to focus the diffraction pattern from infinity to form an image on a screen. An alternative method than using two slits is to use a single slit and a mirror (*Lloyd's mirrors* - [[Labs MT1#Optics|did in labs]]) to create a virtual source for the second slit.
### Combining with slit diffraction
[[Slit diffraction]]
If we also consider the variation in intensity due to non-zero slit widths $\alpha$ we can multiply the intensities to find
$$
I(x)=I_{\text{max}}\,\text{sinc}^{2}\left( \frac{\pi\alpha x}{\lambda D} \right)\left( 1=\cos\left( 2\pi  \frac{ax}{\lambda D} \right) \right)
$$
which results in the plot:
![[Pasted image 20260310122529.png|500]]
so there are two different effects going on simultaneously with two different maximum separations.