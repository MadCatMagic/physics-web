---
tags:
  - circuits/inductor
date-created: 2026-03-17
template-version: m.0
---
[[Circuits]]
Closely related to [[Induction]]

An inductor with inductance $L$ has the following relations:
- solenoid inductor has $L=\mu N^{2}\pi R^{2} /l$ where it has $N$ turns, permeability of core $\mu$, radius $R$ and length $l$.
- has $V=L \frac{dI}{dt}$
- inductors combine inductance like resistors - **however** if we include mutual inductance the total inductance in series is actually $L=L_{1}+L_{2}+2M$.
- [[Complex Impedance]] is given by $Z=i\omega L$

### Transformer
#circuits/transformer 
Considering two coupled coils such that $\Phi_{s}=k\Phi_{p}$ where $k$ is the *coefficient of coupling* and $k=1$ for an ideal transformer, if we consider the ratio of induced emfs in the primary and secondary coil we see
$$
\frac{\epsilon_{s}}{\epsilon_{p}}=\frac{V_{s}}{V_{p}}=\underbrace{ \frac{d\Phi_{s}}{d\Phi_{p}} }_{ k }\underbrace{  \frac{N_{s}}{N_{p}} }_{ \text{winding ratio} }
$$
so the transformer is stepping up or down applied voltage. Ideally no power is dissipated if coils have zero resistance, so
$$
V_{s}I_{s}=V_{p}I_{p}\implies \frac{I_{s}}{I_{p}}=\frac{V_{p}}{V_{s}}=\frac{1}{k}\frac{N_{p}}{N_{s}}
$$

