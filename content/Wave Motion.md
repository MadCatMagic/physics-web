---
tags:
  - waves
date-created: 2026-01-27
template-version: m.0
---
[[Physics]]
[[Wave Motion Textbooks]]
[[Normal Modes & Wave Motion L_HT1]]
## Wave equation
#waves/wave-equation 
When we have
- Acceleration dependent on the spatial derivative of force
- Force varies because of passage of wave itself which implies
- Self sustaining oscillation
We often find the wave equation is satisfied
$$
\frac{ \partial^{2} y }{ \partial t^2 }=c^{2}\frac{ \partial^{2} y }{ \partial x^2 }  
$$
where $c$ is the **wave speed** #waves/wave-speed.
This is a second order linear partial differential equation so we must find
- Initial conditions $y(x,t=0)$ and $\dot{y}(x,t=0)$ for all points $y$ along the wave
- Boundary conditions if the system is bound

#todo characteristic diagrams for wave motions

If we approximate this using finite different method for the second derivatives, it reduces to the [[Normal Modes#Lumpy string|lumpy string]] derivation result.

For example, for transverse waves on an elastic string we find $c^{2}=T /\rho$ where $y$ is the transverse oscillation. For longitudinal waves in a solid bar, we instead find $c^{2}=Y /\rho$ where $Y$ is the young's modulus of the material and $y$ is the longitudinal displacement from the rest position. For longitudinal waves in a gas, the result is similar except $c^{2}=\frac{ \partial P }{ \partial \rho }$ which is a property of the gas.

#waves/wave-number 
There are other important properties that describe the motion of a wave. For sinusoidal motion, we have the *wave number* $k=\frac{2\pi}{\lambda}$ where $\lambda$ is the *wave length*. Additionally, $\omega$ is the angular frequency so the period is $\tau=\frac{2\pi}{\omega}$ and the frequency is $f=\frac{\omega}{2\pi}$. 
### [[Dispersion]]
Includes *dispersion relation* $\omega=ck$ for simple string, *dispersion*, *phase* and *group* *velocities*, *modulation*, and *wave packets*.
### D'Alembert Solution
#waves/d-alembert-solution 
Expressing the wave equation solution in terms of two functions $f$ and $g$ such that
$$
y(x,t)=y(f(x-ct),g(x+ct))
$$
we can expand out and substitute to find the form
$$
\frac{ \partial^{2} y }{ \partial (x-ct)\partial(x+ct) }=0 
$$
hence the most general solution of the wave equation is
$$
y(x,t)=f(x-ct)+g(x+ct)
$$
for arbitrary 'forward-travelling' and 'backward-travelling' functions $f(x)$, $g(x)$. This is the **d'Alembert solution**. Both waves travel at speed $c$, and their shape is unchanged in time. Hence if $f$ and $g$ can be found at some time, the general solution is just a propagation of them for all later and earlier times.
#### Solving for initial conditions
If we have that at $t=0$, $y(x,t=0)=y_{0}(x)$ and $\dot{y}(x,t=0)=\dot{y}_{0}(x)$ then considering the [[Partial Differentiation#Total Derivative|total derivative]] of $y$ allows us to integrate to directly find $f$, $g$ as:
$$
\begin{align}
f(x) & =\frac{y_{0}(x)}{2}-\frac{1}{2c}\int_{0}^{x} \dot{y}_{0}(x') \, dx'  \\[1ex]
g(x) & =\frac{y_{0}(x)}{2}+\frac{1}{2c}\int_{0}^{x} \dot{y}_{0}(x') \, dx' \\[1ex]
\Rightarrow y(x,t) & = \frac{y_{0}(x-ct)+y_{0}(x+ct)}{2}+\frac{1}{2c}\int_{x-ct}^{x+ct} \dot{y}_{0}(x') \, dx' 
\end{align}
$$
More details in [[Lecture 2026-02-09 9am.excalidraw]]. Note that this derivation includes setting some constant terms $\frac{1}{2}(f(0)-g(0))=0$ which is allowed since they would cancel in $y$.
### Separation of Variables Solution
#waves/separation-of-variables-solution 
If we assume that the solution has the format $y(x,t)=X(x)T(t)$, so is a product of functions of $x$ and $t$, we can substitute into the wave equation to find
$$
\frac{1}{c^{2}} \frac{1}{T}\frac{ \partial^{2} T }{ \partial t^2 } = \frac{1}{X}\frac{ \partial^{2} X }{ \partial x^2 } \overset! =-k^{2}
$$
since we are assuming this solution holds for all $x$, $t$ this can only be true if both sides of the expression equal a constant which we are setting as $-k^{2}$. Note that we assume the constant to be negative since only oscillatory solutions satisfy these intitial conditions. We can then solve the two equations separately to find
$$
\begin{align}
X(x) & =A\cos(kx+\phi) \\
T(t) & =B\cos(\omega t+\varphi)
\end{align}
$$
using $\omega=kc$ as the *dispersion relation* of this particular wave equation form. This then gives the solution as
$$
y(x,t)=C\cos(kx+\phi)\cos(\omega t+\varphi)
$$
which can be rewritten as a d'Alembert solution if is expanded out using trig identities. By the linearity of the wave equation, we can also express any wave signal in terms of a sum over many sine wave solutions like this.
#### Finite string example
If we consider a finite string of length $L$ with the boundary conditions of fixed end at $x=0$, free end at $x=L$ then by applying the boundary conditions to the separation of variables solution $y(x,t)$ we can derive the following relation for the wave number
$$
k_{n}=\frac{2n-1}{2L}\pi
$$
where $n$ is some positive integer. This tells us that the complete solution is a sum over all $k_{n}$, or for this case,
$$
y(x,t)=\sum_{n=1}^{\infty} A_{n}\sin(k_{n}x)\cos(\omega_{n}t+\varphi_{n})
$$
using $\omega_{n}=ck_{n}$ dispersion relation and with arbitrary constants $\varphi_{n},A_{n}\in \mathbb{R}$. This particular solution results in **stationary waves** #waves/stationary-wave on the string, with fixed ends corresponding to nodes and free ends corresponding to antinodes.

Solving for a specific set of initial conditions for $y(x,t)$ and $\dot{y}(x,t)$ along the string in general requires [[Fourier Series]] but some simple cases can be solved manually.
### Boundary conditions
#waves/boundary-conditions 
In the case of a non-infinite string, there can be several different boundary types, but typically all of them require finding some boundary conditions and substituting a general wave into them to find the resultant behaviour.
#### Fixed-end
If the end of the string is fixed (condition also known as *Dirichlet*, *no-slip*) then, assuming the boundary is at $x=0$ and the wave is in the region $x>0$ the boundary condition is $y(x=0,t)=0$. Substituting this into the d'Alembert solution directly results in the relevant relation
$$
y(0,t)=0=f(-ct)+g(ct)\implies f(-u)=-g(u)
$$
so the rightward-travelling or reflected wave $f$ is a $\pi$ rotation of the leftward-travelling incident wave $g$; waves are inverted in direction and polarity.
#### Open-end
If the end of the string is free to move along the y-axis (condition also known as *Neumann*, *free-slip*) then we could consider it as a zero-mass point, which results in the relevant constraint $\frac{ \partial y }{ \partial x }\bigr|_{x=0}=0$. Substituting this again into the d'Alembert solution and integrating allows us to find:
$$
\begin{align}
f'(-u) & =-g'(u) \\
\Rightarrow f(-u) & =g(u)
\end{align}
$$
where the constant terms are set to zero by the d'Alembert derivation from earlier. This corresponds to a reflection in y-axis as before but without a flip along the x-axis; waves are inverted only in direction. 
#### Dashpot end
Corresponds to applying a force to the end of the string given by
$$
F_{y}^{D}=-Z_{d}\frac{ \partial y }{ \partial t } =T\frac{ \partial y }{ \partial x } 
$$
with some damping constant $Z_{d}$. This replaces the second constraint as usual. In telegraph equations, analogous to a resistor for load impedance.
#### Mass on the end
Corresponds to having an additional inertia on the end of the string, or force, of the form
$$
F_{y}^{m}=m\frac{ \partial^{2} y }{ \partial t^2 } =T\frac{ \partial y }{ \partial x } 
$$
In telegraph equations, analogous to an inductor for load impedance.
#### Spring on the end
Corresponds to an additional force
$$
F_{y}^{s}=-ky=T\frac{ \partial y }{ \partial x } 
$$
with spring constant $k$. Analogous to a capacitor in telegraph equations for load impedance.
### Energy in the string
#waves/energy #waves/energy-density 
If we consider the energy components in an infinitesimal portion of wire then with some derivation [[Lecture 2026-02-10 9am.excalidraw|in notes]] we find
$$
dE=\Biggr[  \underbrace{ \frac{1}{2}\rho\left( \frac{ \partial y }{ \partial t } \right)^{2} }_{ \text{kinetic} }+\underbrace{ \frac{1}{2}T\left( \frac{ \partial y }{ \partial t }U   \right)^{2}}_{ \text{potential} } \Biggr ]dx
$$
which gives the **energy density** as 
$$
\epsilon=\frac{1}{2}\rho\left( \frac{ \partial y }{ \partial t }  \right)^{2}+\frac{1}{2}T\left( \frac{ \partial y }{ \partial x }  \right)^{2}
$$
If we substitute in d'Alembert solution and use the relation that for a string, $c^{2}=T /\rho$ we find
$$
\epsilon=T(f'(x-ct)^{2}+g'(x+ct)^{2})=\epsilon^{+}+\epsilon^{-}
$$
so energy can be split into forward-travelling and backward-travelling wave parts. 

Additionally this also allows us to see that *for a wave travelling in one direction only*, energy is equipartioned between KE, PE and therefore at every spatial location on the string at a given time, KE=PE and so energy is transferred along the wave even if the displacement of the wave is only transverse.
#### Energy flux
#waves/energy-flux
If we partially differentiate $\epsilon$ with respect to time, 
$$
\begin{align}
\frac{ \partial \epsilon }{ \partial t }  & =\frac{ \partial  }{ \partial t } \left( \frac{1}{2}\rho\left( \frac{ \partial y }{ \partial t }  \right)^{2}+\frac{1}{2}T\left( \frac{ \partial y }{ \partial x }  \right)^{2} \right) \\
 & =\rho \frac{ \partial y }{ \partial t } \frac{ \partial^{2} y }{ \partial t^2 } +T\frac{ \partial y }{ \partial x } \frac{ \partial^{2} y }{ \partial x\partial t } 
\end{align}
$$
noting that $\epsilon=\frac{ \partial E }{ \partial x }$ where $E$ is the energy in the string, and then substituting the wave equation for $\frac{ \partial^{2} y }{ \partial t^2 }$:
$$
\begin{align}
\frac{ \partial  }{ \partial t }\frac{ \partial E }{ \partial x } & =T\frac{ \partial y }{ \partial t } \frac{ \partial^{2} y }{ \partial x^2 } +T\frac{ \partial y }{ \partial x } \frac{ \partial^{2} y }{ \partial x\partial t }  \\[1ex]
 & =\frac{ \partial  }{ \partial x } \left( T\frac{ \partial y }{ \partial t } \frac{ \partial y }{ \partial x }  \right)
\end{align}
$$
so we can integrate along the length of the string to find
$$
\frac{ \partial  }{ \partial t } E_{L}=T\frac{ \partial y }{ \partial t } \frac{ \partial y }{ \partial x } \Biggr|_{L}-T\frac{ \partial y }{ \partial t } \frac{ \partial y }{ \partial x } \Biggr|_{0}=-\mathcal{F} _{\text{out of string}}(L)+\mathcal{F} _{\text{into string}}(0)
$$
where $E_{L}$ is the total energy in the string. Hence as expected, the total energy changing only depends on the flux through the endpoints, since within the string energy is conserved, just being carried along it. 

Additionally if we consider some particular segment of string we find the **energy flux** through that segment is given by
$$
\mathcal{F} =-T\frac{ \partial y }{ \partial t } \frac{ \partial y }{ \partial x } 
$$
substituting in d'Alembert solution once again then gives
$$
\mathcal{F} =Tcf'^{2}-Tcg'^{2}=c\epsilon^{+}-c\epsilon^{-}
$$
so the rate of flow of energy is the energy density times the speed of the wave, which implies *the wave transmits energy at the wave speed*.
### Waves at boundaries
#waves/boundaries 
Considering two strings joined together at $x=0$ with densities $\rho_{1}$ and $\rho_{2}$. For an incoming wave in the +x direction
$$
y_{1}(x,t)=\underbrace{ A_{I}\sin(\omega_{I}t-k_{I}x) }_{ \text{incident} }+\underbrace{ A_{R}\sin(\omega_{R}t+k_{R}x) }_{ \text{reflected} }\quad \text{for }x<0
$$
which encounters the boundary and results in a wave
$$
y_{2}(x,t)=\underbrace{ A_{T}\sin(\omega_{T}t-k_{T}x) }_{ \text{transmitted} }\quad\text{for }x>0
$$
we can apply some boundary conditions, notably that *the string is continuous* so $y_{1}(0,t)=y_{2}(0,t)$ and that since tension is constant on both sides and the vertical force at the boundary must be equal and opposite, *the gradient is continuous* so $\dot{y}_{1}(0,t)=\dot{y}_{2}(0,t)$. Since frequency of oscillations $\omega$ is constant throughout the oscillation as a result, we also take $\omega_{I}=\omega_{R}=\omega_{T}=\omega$. Substituting in $y_{1}$ and $y_{2}$ allows us to solve to find
$$
\begin{align}
r=\frac{A_{R}}{A_{I}} & =\frac{k_{1}-k_{2}}{k_{1}+k_{2}} \\[1ex]
\tau=\frac{A_{T}}{A_{I}} & =\frac{2k_{1}}{k_{1}+k_{2}}
\end{align}
$$
where $r$ is the **reflectance** #waves/reflection and $\tau$ is the **transmission** #waves/transmission of the boundary. Given that $k\propto \sqrt{ \rho }$ we can also write this purely in terms of the physical characteristics of the connected strings.
#### Energy transmission
Given the above energy flux formula, if we substitute the simple $y=A\sin(\omega t-kx)$ wave we find
$$
\langle \mathcal{F}  \rangle _{t}=\frac{1}{2}T\omega kA^{2}
$$
so considering the flux transmitted by the forward and backward travelling waves,
$$
\begin{align}
R_{r} & = \frac{\langle \mathcal{F} _{R} \rangle }{\langle \mathcal{F} _{I} \rangle }=r^{2}=\left( \frac{k_{1}-k_{2}}{k_{1}+k_{2}} \right)^{2} \\[1ex]
R_{\tau} & =\frac{\langle \mathcal{F} _{T} \rangle }{\langle \mathcal{F} _{I} \rangle }=\frac{k_{2}}{k_{1}}\tau^{2}=\frac{4k_{1}k_{2}}{(k_{1}+k_{2})^{2}}
\end{align}
$$
give the ratios for energy transmission to the reflected or transmitted wave. We note that $R_{r}+R_{\tau}=1$ so energy is conserved overall.
#### Wave impedance
#waves/impedance 
We can rewrite the above flux expression by letting $Z=\sqrt{ \rho T }$ be the **impedance** of the simple string, so
$$
\langle \mathcal{F}  \rangle =\frac{1}{2}Z\omega^{2}A^{2}
$$
The impedance basically just represents the physical properties of how good the string is at transmitting energy, whereas $\omega$ and $A$ determine the oscillation frequency and amplitude of the wave which is purely oscillation information.

#waves/impedance-matching 
If we wanted to minimise the reflection at a boundary, we could add a damping force to the boundary e.g. using a dashpot. This would result in some extra force on the boundary $F_{d}=-Z_{d}\frac{ \partial y }{ \partial t }|_{x=0}$ which, if we resolve the forces at the boundary and then assume mass is zero, gives
$$
T\left( \frac{ \partial y_{2} }{ \partial x } -\frac{ \partial y_{1} }{ \partial x }  \right)=Z_{d}\frac{ \partial y }{ \partial t } 
$$
as the boundary condition we can apply to the $y_{1}$, $y_{2}$ from before, replacing the continuous spatial derivative condition. Solving in this case gives:
$$
r= \frac{T(k_{1}-k_{2})-Z_{d}\omega}{T(k_{1}+k_{2})+Z_{d}\omega}=\frac{Z_{1}-Z_{2}-Z_{d}}{Z_{1}+Z_{2}+Z_{d}}
$$
so impedance matching yields no reflection when $Z_{2}+Z_{d}=Z_{1}$. Note that energy transmittance is imperfect as some is lost in the damping term - if we consider the energy transmittance ratio we see that
$$
R_{\tau}=\frac{\langle \mathcal{F} _{T} \rangle }{\langle \mathcal{F} _{I} \rangle }=\frac{k_{2}}{k_{1}}(1+r)^{2}
$$
using $\tau=1+r$ (which comes from the continuous string B.C.). So when $r=0$, the energy transmittance is $R_{T}=k_{2} /k_{1}=Z_{2} /Z_{1}$.
### [[Telegraph equations]]
Application of wave theory to circuits - specifically long parallel wires.
### [[Electromagnetic wave]]
Applications to electromagnetism.