---
tags:
  - optics/single-slit-diffraction
  - "#optics/rectangular-slit-diffraction"
  - optics/circular-aperture-diffraction
date-created: 2026-03-09
template-version: m.0
---
[[Optics#Fraunhofer conditions & diffraction]]
### Single slit diffraction
Considering the contributions from a continuous slit of width $\beta$, we can integrate over the many infinitesimal $d\psi$ to find the total contributions from points $-\beta /2<x<\beta /2$ to a point $y$ on the screen. Similarly to the double slit, we find the path by binomially expanding while assuming $D\gg\beta$ and $D\gg y$ so
$$
\delta(x,y)=\delta_{0}+\frac{ny^{2}}{2D}-\frac{nyx}{D}
$$
and considering that we can normalise the intensity along the slit by taking $dA=\frac{dx}{\beta}A$, we get the wavefunction integral as
$$
\psi=\frac{A}{\beta}\int_{-\frac{\beta}{2}}^{\frac{\beta}{2}} \exp {i\left( \omega t-k_{0}\delta_{0}-\frac{k_{0}ny^{2}}{2D}+k_{0}nyx+\phi_{0} \right)}  \, dx 
$$
Evaluating this integral and the finding the intensity,
$$
\begin{align}
I=\frac{\psi \psi ^{*}}{2} & =\frac{1}{2}\left( \frac{AD}{\beta k_{0}ny} \right)^{2}\left( 2\sin\left( \frac{k_{0}ny\beta}{2D} \right) \right)^{2} \\[1ex]
 & =I_{0}\,\text{sinc}^{2}\left( \frac{\pi\beta}{\lambda D}y \right)
\end{align}
$$
using $k_{0}n=\frac{2\pi}{\lambda}$ and letting $I_{0}=\frac{1}{2}A^{2}$. Since we have normalized, we could also write $I_{0}=\beta I'$ where $I'$ is the intensity per unit length along the slit. For this function, the central maximum occurs at $y=0$ and minima occur at $y=\frac{m\lambda D}{\beta}$ for $m\in \mathbb{Z} \setminus 0$:
![[Pasted image 20260309205056.png|500]]
### Rectangular slit diffraction
If we have an $\beta \times\alpha$ dimension slit we can perform much of the same analysis as before but with extra dimensions to integrate over, which is tedious but eventually leads to
$$
I(x,y)=I_{0}\,\text{sinc}^{2}\left( \frac{\pi x\alpha}{\lambda D} \right)\,\text{sinc}^{2}\left( \frac{\pi y\beta}{\lambda D} \right)
$$
which is analogous to the single slit case in the cardinal directions. Note that intensity is also normalized in this case, so it might be better to rewrite as $I_{0}=\alpha^{2}\beta^{2}I'$ where $I'$ is intensity per unit area along the rectangular slit.

### Circular aperture diffraction
Considering an aperture of diameter $\alpha$, the intensity at a distance from the centre of the aperture $\rho$ is given
$$
I(\rho)=I_{\text{max}}\left( \frac{\text{J}_{1}\left( \frac{\pi \rho}{\lambda D} \right)}{\frac{\pi \rho}{\lambda D}} \right)^{2}
$$
where $\text{J}_{1}(x)$ is the first order [[Bessel function]]. When we solve this for the first minima we find
$$
x=1.22 \frac{\lambda D}{\alpha}
$$
where $1.22$ is a result of the Bessel function - is just an arbitrary constant.