---
tags:
  - elecmag/magnetic-dipole
date-created: 2026-03-16
template-version: m.0
---
[[Electromagnetism]]
Analogous to [[Electric Multipoles]].

A small current loop defines a magnetic dipole - we define the *magnetic dipole moment* as $\vec{m}=m\hat{A}=I\vec{A}$ where $\hat{A}$ points perpendicularly out of coil according to RHR, and $|A|$ is the area of the loop. Similarly to the electric dipole, we can find the radial and rotational components of the field a long distance from the coil as
$$
\begin{align}
B_{r} & =\frac{2\mu_{0}m\cos\theta}{4\pi r^{3}} \\
B_{\theta} & =\frac{\mu_{0}m\sin\theta}{4\pi r^{3}} \\
B_{\phi} & =0
\end{align}
$$
The most effective derivation of this uses [[Magnetic potential]].
### Torque on dipole in external B-field
Similarly to electric dipole, we find
$$
\vec{\tau}=\vec{m}\times \vec{B}_{\text{ext}}
$$
this derivation comes from considering the forces on some rectangular loop, and can be generalised to any dipole area by composing it of individual little current loops, of which all contributions except the edge loop cancel out so it only depends on area.
### Energy in external B-field
Again in similar method to electric dipole, we find
$$
\vec{U}=-\int_{\frac{\pi}{2}}^{\Theta} \vec{\tau}\cdot d\vec{\theta}'=-\vec{m}\cdot \vec{B}_{\text{ext}}
$$
where we have used $\vec{\tau}=-mB_{\text{ext}}\sin\theta$ (from before) and negative sign comes from the fact torque is restoring force.