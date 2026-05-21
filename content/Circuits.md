---
tags:
  - circuits
date-created: 2026-01-03
template-version: m.0
---
[[Circuits L_MT1]]
## DC analysis and Components
#circuits/basic-dc 
We have **Ohm's law** $V=IR$ for any ohmic component, and **Kirchhoff's laws** (KCL, KVL). We can either assign every branch a current, apply the laws, and solve to find currents. *Passive sign convention* tells us that current flows from positive to negative.

#circuits/mesh-currents are slightly more elegant, using the linearly of ohm's law to layer currents for each branch on top of one another, but is effectively the same principle.

We can also apply *node analysis* by picking a spot for a ground node (0V) and then finding node voltages relative to ground.
##### Power matching
#circuits/power-matching is when we maximise the power delivered to the load. This occurs when $R_{L}=R_{in}$ so the internal resistance of the source matches the resistance of the load.
#### Thevenin's theorem
#circuits/thevenins-theorem 
Any two-terminal network of sources and resistors (or generalised [[Complex Impedance]] resistors) can be replaced with a series combination of a single resistor $R_{\text{th}}$ ($Z_{\text{th}}$) and voltage source $V_{\text{th}}$ (AC source $\tilde{V}_{\text{th}}$).

The voltage can be easily found as the potential drop across the terminals, but for the resistance, can either:
- short voltage sources, and disconnect current sources, then $R_{\text{th}}$ is resistance of remaining circuit across terminals.
- find current across terminals if they were shorted, then use $R_{\text{th}}={V_{\text{th}}} /{I_{\text{short}}}$.
#### Norton's theorem
#circuits/nortons-theorem 
Same but system is replaced with a parallel resistor $R_{\text{nor}}$ and current source $I_{\text{nor}}$ where
- $I_{\text{nor}}=I_{\text{short}}$
- $R_{\text{nor}}=V_{\text{th}} /I_{\text{nor}}=V_{\text{th}} /I_{\text{short}}=R_{\text{th}}$.
### Ohm's law
#circuits/ohms-law 
The statement of ohms law in terms of [[Electromagnetism]] is $V=IR=El$ where $E$ is the field strength in the ohmic resistor, $l$ is the length. Considering $I=JA$ from current density $J$, resistor area $A$, we get
$$
El=JAR
$$
which is ohm's law in terms of current density. Hence
$$
\vec{J}=\frac{l}{RA}\vec{E}=\sigma \vec{E}=\frac{1}{\rho}\vec{E}
$$
where $\sigma=\frac{1}{\rho}$ is the *conductivity*, $\rho$ is the *resistivity* of material.
### [[Capacitor]]
Includes *capacitor properties*, *shapes of capacitors*.
#### [[Inductor]]
Includes *inductor properties*, *transformers*.
### Op-amp
#circuits/op-amps 
The **ideal linear op-amp** obeys a couple *golden rules*:
- The output will do whatever is necessary to make the voltage difference between the inputs zero i.e. $V_{\text{in}}^{+}=V_{\text{in}}^{-}$
- No current flows into the inputs i.e. $I_{\text{in}}^{\pm}=0$
It achieves this by setting $V_{\text{out}}$ to whatever it needs - this means any amount of current can flow in or out of the output.

Additionally, the op-amp has infinite input impedance (so places no load on the input power supply) and zero output impedance (any amount of voltage/current can be drawn from it).

## AC analysis
#### [[Complex Impedance]]
Allows for easier calculation of oscillating circuits.
#### [[Telegraph equations]]
Application of circuit theory to wave equation.