---
tags:
  - optics
date-created: 2026-01-02
template-version: m.0
---
[[Optics Textbooks]]
[[Optics L_MT1]]
[[Optics L_HT1]]
## Geometric Optics
#optics/basics 
Revolves around the speed of light changing depending on refractive index $n$ of material it is travelling through - $v=\frac{c}{n}$.
We have law of reflection $\theta_{1}=\theta_{2}$, law of refraction $n_{1}\sin \theta_{1}=n_{2}\sin\theta_{2}$, and total internal reflection $\theta_{c}=\sin ^{-1}(n_{2} /n_{1})$ for $n_{2}<n_{1}$ (incident light $\theta_{1}$ on boundary).
#### Fermat Principle
#optics/fermat-principle 
Light follows the path of *stationary time* (least action) between two points - if we denote the **optical path** #optics/optical-path as
$$
L=\int _{\text{trajectory}}n \, ds 
$$
then the light will follow the path of stationary $L$ i.e. derivative of $L$ is 0.
#### Huygen's Principle
#optics/huygens-principle 
When a light wave is propagating, every point on a wavefront can be 
considered the source of spherical wavelets with the same wavelength 
and propagating in the same direction of the original wavefront. *The envelope of those wavelengths forms the new wavefront*.
### Prisms
#optics/prism #optics/prism-deviation-angle #optics/dispersing-prism
For a standard triangular *dispersing* prism with opening angle $\alpha$, the **deviation angle** of a ray of light passing through the prism is given by
$$
\delta  =\theta_{1}-\alpha+\sin ^{-1}\left( n\sin\left( \alpha-\sin ^{-1}\left( \frac{\sin\theta_{1}}{n} \right) \right) \right)
$$
for an entry angle to the normal of $\theta_{1}$ and index of refraction of the prism $n$.

For white light $n$ differs slightly for each wavelength so different colours deviate by different amounts.

#optics/prism-minimum-deviation 
The **minimum deviation angle** is given by 
$$
\delta_{\text{min}}=2\sin ^{-1}\left( n\sin \left( \frac{1}{2}\alpha \right) \right)-\alpha
$$
this corresponds to when the light is travelling parallel to the base of the prism while it is in the prism (or perpendicular to the axis of reflective symmetry of the prism).

#optics/crystals-and-light-halos 
Ice crystals are responsible for halos we see in the sky and tend to be hexagonal, so we find
$$
\delta=2\sin(1.31\sin(30^{\circ}))-60^{\circ}=21.84^{\circ}
$$
known as the $22^{\circ}$ halo. In reality deflection also depends on orientation so there is a secondary halo at $46^{\circ}$. Also, since $n$ depends on wavelength, halos have tinted fringes.

### Sign convention
#optics/sign-convention 
We use the sign convention *real is positive*, giving the standard
$\frac{1}{u}+\frac{1}{v}=\frac{1}{f}$ equation. $f>0$ for a **converging** lens, $f<0$ for a **diverging** lens. $v<0$ if the image is **virtual**. This means that lenses add their *powers*.

We can use ray tracing #optics/ray-tracing to deduce the effect of a particular optical system.
### [[Lenses]]
### [[Mirrors]]
### Optical Aberrations
There are three types of aberration #optics/aberrations:
- Spherical aberration is due to the divergence of a [[Mirrors#Spherical mirror|spherical mirror]] from the ideal parabolic shape - this divergence is approximately $\Delta x=y^{4} /3R^{3}$. This is most prevalent far from the focal axis. #optics/spherical-aberration
- Coma aberration is due to the paraxial approximation - rays non-parallel to axis converge at different distances forming a *coma* that points away from the focal axis. #optics/coma-aberration
- Chromatic aberration is due to different wavelengths of light having different refractive indices, so converge at different points (only happens with lenses, not mirrors). Hence have coloured fringes. #optics/chromatic-aberration
## Wave optics
#optics/waves 
Focuses more on the [[Electromagnetic wave]] physical side of things - namely we will be dealing principally with oscillating solutions of the wave equation. 

We will stick to
- plane wave - moving in one direction, useful in far-field approximation
- propagating - waves at velocity $\nu$ in $\vec{k}$-dir
- monochromatic - one wavelength only
- transverse - $\vec{E}$ and $\vec{B}$ are orthogonal to $\vec{k}$
- linearly polarised - $\vec{E}$ and $\vec{B}$ always in the same axes, do not rotate or anything wacky.

This allows for the scalar approximation of the wave function
$$
\psi(x,t)=A\cos(\omega t-kx+\phi_{0})
$$
which means the intensity is given by 
$$
I= \langle |\psi|^{2} \rangle_{t}=\frac{A^{2}}{2} 
$$
and with
$$
k=\frac{2\pi}{\lambda}=n \frac{2\pi}{\lambda_{0}}=nk_{0}
$$
which we could also rewrite using the **optical path** travelled by the wave $\delta$ #optics/optical-path so
$$
\psi(x,t)=A\cos(\omega t-k_{0}\delta+\phi_{0})
$$
with $\delta=\int_{C}n\,dl$.
Note that $\omega$ does NOT depend on $\delta$.
### Diffraction and interference
#optics/diffraction #optics/interference 
These are the central ideas in wave optics. **Diffraction** is when light is bend as it encounters obstacles, e.g. going from a plane wave to a point source as it encounters a slit. **Interference** is when waves interfere by interacting if they reach a screen at the same point.
### Rayleigh criterion
#optics/rayleigh-criterion 
Says that for two points to be visually distinguishable, the first minimum of one must lie at the maximum of the other. For a single slit this means that
$$
y=\frac{\lambda D}{\beta}=D\sin\theta\Rightarrow \sin\theta=\frac{\lambda}{\beta}
$$
is the criterion for a single slit. This is the minimum angular resolution for a given aperture.

In the case of a [[Slit diffraction#Circular aperture diffraction|circular aperture]] we find that
$$
\theta \approx 1.22 \frac{\lambda}{\alpha}
$$
where $\alpha$ is the diameter of the aperture. This is the form more commonly associated with astronomy/telescopes. Diffraction results in an *airy disk* and we require this separation for points to be distinguishable.
### Fraunhofer conditions & diffraction
#optics/fraunhofer-conditions 
The conditions allow for the case of far-field diffraction where the source, obstacle and screen are far from each other, so
- the lines from the source to an obstacle can be considered parallel
- the lines from the obstacle to a point in the pattern are parallel.
Specifically we require
$$
D\gg \frac{b^{2}}{\lambda}
$$
where $D$ is the distance from the source to the screen and $b$ is the slit width, or source size. [[Lecture 2026-03-03 11am.excalidraw|Derivation in notes]].

#optics/fraunhofer-diffraction
All the Fraunhofer diffraction phenomena can then be derived from adding up $\psi$ for different relevant paths at a point on the screen to find $\psi_{\text{tot}}$, and then taking the intensity using
$$
I=\langle |\psi_{\text{tot}}|^{2} \rangle _{t}
$$
as before and examining the behaviour as a function of some spatial coordinate to analyse the diffraction pattern.

#optics/complex-description
Another method of approach is the complex description which rewrites the wave function as $\psi=\mathrm{Re}(\tilde{\psi})$ where
$$
\tilde{\psi}=\tilde{A}e^{i(\omega t-k_{0}\delta+\phi)}
$$
Then summing wave functions is basically the same but we have two choices for calculating $I$, can either find it as before using $I=\langle \mathrm{Re}(\tilde{\psi})^{2} \rangle_{t}$ or using the more complex method $I=\frac{1}{2}\tilde{\psi}\tilde{\psi}^{*}$ which might sometimes be simpler.

Applications:
#### [[Young's slits]]
This is the simplest case of two point-like slits. Maxima separated by $\Delta y=\frac{\lambda D}{a}$.
#### [[Diffraction grating]]
This is the case of many parallel slits or reflective strips. Maximum when $\sin\theta=\frac{m\lambda}{a},\, m\in \mathbb{Z}$.
#### [[Slit diffraction]]
The case of a continuous slit which is not point like. Contains *single slit*, *rectangular slit* cases. For single slit case, maximum when $y=\frac{m\lambda D}{\beta}$ for $m\in \mathbb{Z} \setminus 0$.