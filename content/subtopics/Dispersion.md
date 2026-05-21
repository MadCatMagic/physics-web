---
tags:
  - "#waves/dispersion-relation"
  - waves/dispersion
date-created: 2026-03-12
template-version: m.0
---
[[Wave Motion]]

The wave number and angular frequency for some certain wave in a particular medium are related by the **dispersion relation** of a form $\omega=f(k)$. For the ideal linear wave equation, this relation is $\omega=ck$.
### Wave modulation
#waves/modulation
There are several different waves of transmitting information along a string or via waves:
- *pulse modulation* where the wave is modulated in pulses which could represent binary information, etc.
- *amplitude modulation* where the amplitude of the wave is modulated over time to transmit information.
- *frequency modulation* where the frequency of the wave itself changes over time.
### Wave packets
#waves/wave-packets #waves/phase-velocity #waves/group-velocity
If we consider two nearly-same waves
$$
\begin{align}
y_{1} & =A\sin((k+\delta k)x-(\omega+\delta\omega)t) \\
y_{2} & =A\sin((k-\delta k)x-(\omega-\delta\omega)t)
\end{align}
$$
then the combination $y=y_{1}+y_{2}$ appears to have **wave packet** behaviour where information is transmitted via *amplitude modulation* of the wave. Specifically
$$
y=2A\sin(kx-\omega t)\cos(\delta kx-\delta\omega t)
$$
which gives two velocities of the respective waves, we have
- **phase velocity** $v_{p}=\frac{\omega}{k}$ is the velocity of the carrier waves
- **group velocity** $v_{g}=\frac{\delta\omega}{\delta k}=\frac{d\omega}{dk}$ is the modulating envelope velocity - specifically the speed of the point where all constituent waves are peaking at the same time.
#### On a string
Or indeed any wave following the typical dispersion relation $\omega=ck$, we have
$$
\begin{align}
v_{p} & =\frac{\omega}{k}=c \\
v_{g} & =\frac{d\omega}{dk}=c
\end{align}
$$
so both waves and wave packets move at the same speed, $c$. This implies a transmitted signal doesn't change shape over time, it just translates in its direction of propagation.
### Dispersion
In the case where $\omega \cancel{ \propto }k$ we have a **non-linear** dispersion relation which means that $v_{g}\neq v_{p}$ and results in **dispersion** of different frequencies - the wave packet spreads out as different frequencies translate with different velocities. It is important to note that both energy and information is transmitted at $v_{g}$.

For more complex behaviour we must have a more complex wave equation since the simple [[Wave Motion#Wave equation|case]] is linear so always results in $\omega=ck$. We can be given a more complex dispersion relation and expected to find phase, group velocity.