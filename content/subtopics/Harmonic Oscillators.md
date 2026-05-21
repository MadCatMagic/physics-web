---
tags:
  - mech
date-created: 2025-12-17
template-version: m.0
---
### Simple
#mech/simple-harmonic-oscillator 
This is the simplest case where there is just a restoring force
$$
{F}=-k{x}
$$
which when solved gives:
$$
x=A\cos wt+B\sin wt
$$
where we have defined $\omega^{2}=\frac{k}{m}$.
### Damped
#mech/damped-harmonic-oscillator 
This introduces a damping force proportional to the velocity:
$$
\ddot{x}+\gamma \dot{x}+\omega^{2}x=0
$$
which can be solved again to give a general solution which depends on the value of $\frac{\gamma}{2\omega_{0}}$:
- $\frac{\gamma}{2\omega_{0}}<1$ weak damping:
$$
x(t)=e^{-\frac{\gamma}{2}t}(A\cos \omega_{\gamma} t+B\sin\omega_{\gamma} t)
$$
- $\frac{\gamma}{2\omega_{0}}=1$ critical damping:
$$
x(t)=(A+Bt)e^{-\frac{\gamma}{2}t}
$$
- $\frac{\gamma}{2\omega_{0}}>1$ heavy damping:
$$
x(t)=Ae^{-t/\tau_{1} }+Be^{-t/\tau_{2}}
$$
where we have defined the response frequency $\omega_{\gamma}$ as
$$
\omega_{\gamma}=\omega_{0}\sqrt{ 1-\left( \frac{\gamma}{2\omega_{0}} \right)^{2} }
$$
and for heavy damping there are two decaying exponentials with the time constants
$$
\tau_{1,2}=\frac{2}{\gamma}\left( 1\pm \sqrt{ 1-\left( \frac{2\omega_{0}}{\gamma} \right)^{2} } \right)^{-1}
$$
### Driven & Damped
#mech/driven-damped-harmonic-oscillator 
The case here is almost identical except with an extra periodic driving force:
$$
\ddot{x}+\gamma \dot{x}+\omega^{2}_{0}x=\frac{F}{m}\cos\omega t
$$
Solving this using some simple complex analysis yields
$$
x_{p}(t)=z_{0}\cos(\omega t+\delta)
$$
as the particular solution - we only care about the steady state in this case and the steady state is always the particular solution.
$$
z_{0}=\frac{F /m}{\sqrt{ (\omega_{0}^{2}-\omega^{2})^{2}+\gamma^{2}\omega^{2} }}
$$
$$
\tan\delta=\frac{\gamma\omega}{\omega^{2}-\omega_{0}^{2}}
$$
### Quality factor
#mech/quality-factor 
This is a property describing the damping properties of a weakly damped oscillator. It is defined like so:
$$
Q=2\pi \cdot \frac{E_{\text{stored}}}{\langle P_{d} \rangle /T }
$$
and represents how many oscillations the system makes before energy significantly decays (1/e). If we have $E(t)$ and some constant angular frequency $\omega_{0}$ we can approximate this as
$$
Q=\omega_{0}\cdot \frac{E(t)}{\dot{E}(t)}
$$
