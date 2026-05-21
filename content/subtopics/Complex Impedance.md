---
tags:
  - circuits/complex-impedance
date-created: 2026-01-03
template-version: m.0
---
We can use complex numbers to simplify **steady state oscillating** circuits. We use **generalised ohm's law**: $\tilde{V}=\tilde{I}Z$ where $\tilde{V}$ and $\tilde{I}$ are complex and $Z$ is the impedance, which combines like resistance for resistors and is
- $Z=R$ for resistors
- $Z=i\omega L$ for inductors
- $Z=1 /i\omega C$ for capacitors
where $\omega$ is the oscillating frequency of the circuit.

Since we only care about steady state, every part of the circuit must oscillate at the same frequency but with different phases and magnitudes. This means we can write both complex current and voltage as
$$
\begin{align}
\tilde{V} & =V_{0}\exp{[i(\omega t+\theta_{V})]} \\
\Rightarrow V(t) & =\mathrm{Re}(\tilde{V}) \\
 & =V_{0}\cos(\omega t+\theta_{V}) \\[2ex]
\tilde{I} & =I_{0}\exp{[i(\omega t+\theta_{I})]} \\
\Rightarrow I(t) & =\mathrm{Re}(\tilde{I}) \\
 & =I_{0}\cos(\omega t+\theta_{I}) \\
\end{align}
$$
### Phasors
#circuits/phasors 
This is the concept of representing an instant of an alternating current circuit by an Argand diagram, where we pick a reference e.g. $\tilde{I}$ and find the voltages and their phases geometrically, or vice versa.
