---
tags:
  - waves/telegraph-equations
date-created: 2026-03-09
template-version: m.0
---
[[Wave Motion]]
[[Circuits]]

If we consider two long, parallel wires with zero resistance, capacitance per unit length $C$, and self-inductance per unit length $L$, with a load impedance of $Z_{T}$ at $x=0$. The self-inductance results in changes in the current of the form $\frac{ \partial V }{ \partial x }=-L\frac{ \partial I }{ \partial t }$ and the capacitance results in $\frac{ \partial I }{ \partial x }=-C\frac{ \partial V }{ \partial t }$ due to energy stored in each field exchanging. 

This comes from considering a $dx$ of wire, which has a voltage drop of $\frac{ \partial V }{ \partial x }dx$ across it, equalling the voltage drop due to the self inductance $-Ldx\frac{ \partial I }{ \partial t }$. Also, if the charge in a $dx$ is $q=(Cdx)V$, then $dI=\frac{dq}{dt}$ so $-\frac{ \partial I }{ \partial x }dx=\frac{ \partial  }{ \partial t }(Cdx)V$ which gives the second relation - using $dI=-\frac{ \partial I }{ \partial x }dx$ annoying sign change.

Partially differentiating both relations with respect to $x$ and $t$ allows us to find the **telegraph equations**
$$
\begin{align}
\frac{ \partial^{2} V }{ \partial t^2 }  & =\frac{1}{LC}\frac{ \partial^{2} V }{ \partial x^2 }  \\[1ex]
\frac{ \partial^{2} I }{ \partial t^2 }  & =\frac{1}{LC}\frac{ \partial^{2} I }{ \partial x^2 } 
\end{align}
$$
which are [[Wave Motion#Wave equation|wave equations]] so the wave speed $c$ is given by $c^{2}=\frac{1}{LC}$ for these particular wave equations. These have the standard [[Dispersion]] relation $\omega=ck$. We can then consider the standard solutions
$$
\begin{align}
V & =V_{0}\sin(\omega t\pm kx+\phi_{0}) \\
I & =I_{0}\sin(\omega t\pm kx+\phi_{0})
\end{align}
$$
and note that the phase must be equal from the previous relations. 

By considering the fields that are carrying the energy we can see that the transmission line is carrying electromagnetic waves.
### Characteristic impedance
The impedance is given as
$$
Z_{0}=\frac{V_{0}}{I_{0}}=\mp \sqrt{ \frac{L}{C} }=\mp Lc
$$
where it is positive for a forward wave, negative for a backward wave. $V$, $I$ are in phase so $Z_{0}$ is real (resistance-like). Note that even though each individual line has zero resistance, the transmission lines have resistance overall due to energy exchange in the fields. Additionally, considering the the energy flow
$$
\langle \mathcal{F}  \rangle =\frac{1}{2}LcI_{0}^{2}=\frac{1}{2}Z_{0}I_{0}^{2}
$$
is consistent with previous theory.
### Reflection at terminated line
If the line ends with impedance $Z_{T}$, we can write incident and reflected waves in exponential form as
$$
\begin{align}
V(x,t) & =A_{I}e^{i(\omega t-kx)}+A_{R}e^{i(\omega t+kx)} \\[1ex]
I(x,t) & =\frac{A_{I}}{Z_{0}}e^{i(\omega t-kx)}-\frac{A_{R}}{Z_{0}}e^{i(\omega t+kx)}
\end{align}
$$
noting $Z_{0}$ negative for backwards waves. Then at $x=0$, we must have
$$
\frac{V(0,t)}{I(0,t)}=Z_{T}=Z_{0} \frac{A_{I}+A_{R}}{A_{I}-A_{R}}
$$
hence we can find the reflectance as
$$
r=\frac{A_{R}}{A_{I}}=\frac{Z_{T}-Z_{0}}{Z_{T}+Z_{0}}
$$
which matches the result in [[Wave Motion#Waves at boundaries]]. Hence if $Z_{T}\neq Z_{0}$, power is reflected which is undesirable. If $Z_{T}$ is complex, $r$ becomes complex which corresponds to the reflected wave being phase shifted.