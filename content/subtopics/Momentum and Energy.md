---
tags:
  - relativity/4-momentum
  - relativity/momentum
  - relativity/energy
date-created: 2025-12-23
template-version: m.0
---
[[Special Relativity]]
[[4 Vectors]]

The **4-momentum** is
$$P=mU=m\gamma(c,\vec{u})^{T}$$
from which we derive the usual momentum and energy relations:
$$
\begin{align}
E & =\gamma mc^{2} &  \\
\vec{p} & =\gamma m \vec{u} \\
P\cdot P & =m^{2}c^{2} \\
E^{2} & =m^{2}c^{4}+|\vec{p}|^{2}c^{2}
\end{align}
$$
so
$$
P=\begin{pmatrix}
\frac{E}{c} \\
\vec{p}
\end{pmatrix}
$$
and since we have 4-momentum conservation, both linear momentum and energy are conserved in relativistic interactions, *always*. #relativity/momentum-conservation 
#### Massless particles
#relativity/massless-particles
Massless particles have $P\cdot P=0$, so
$$
E=|\vec{p}|c
$$
and quantum gives the energy of a photon as
$$
E=\hbar\omega=\frac{hc}{\lambda}
$$
so for massless particles,
$$
P_{\gamma}=\frac{\hbar\omega}{c}\begin{pmatrix}
1 \\
\hat{n}
\end{pmatrix}=\frac{E_{\gamma}}{c}\begin{pmatrix}
1 \\
\hat{n}
\end{pmatrix}
$$
so the particle must be travelling at $c$ in any reference frame.
#### Longitudinal doppler shift
#relativity/longitudinal-doppler-shift 
$$
\omega'=\omega \sqrt{ \frac{ 1-\frac{v}{c} }{1+\frac{v}{c}} }
$$
for photons observed being redshifted in a moving reference frame $S'$ relative to $S$ with frequency in $S$, $\omega$.
#### Centre of mass/momentum frame
#relativity/centre-of-momentum-frame 
For any system (mostly - not for e.g. a single photon) there exists an IRF for which the total 4-P is
$$
P_{\text{tot}}=\left( \frac{E_{\text{com}}}{c},0,0,0 \right)^{T}
$$
and $E_{\text{com}}^{2}=c^{2}P_{\text{tot}}^{2}$. It is useful to know that
$$
\vec{v}_{\text{com}}=\frac{\vec{p}_{\text{tot}}}{E_{\text{tot}}}c^{2}
$$
Additionally it is very useful to recall that we can apply the Lorentz transformation to all the individual 4-momenta in the CM frame to derive the result:
$$
\gamma_{\text{CM}}=\frac{\sum_{i=1}^{N}E_{i}}{E_{\text{CM}}}
$$
where $E_{i}$ are the energies in the lab frame and $\gamma_{\text{CM}}$ is the Lorentz factor relating the lab frame and CM frame.