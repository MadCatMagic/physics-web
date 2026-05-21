---
tags:
  - mech/normal-modes
date-created: 2026-01-26
template-version: m.0
---
[[Normal Modes & Wave Motion L_HT1]]
Normal modes are the natural modes of oscillation for an oscillating system. They are specifically components of the oscillatory solution with
- The same phase relation
- The same frequency
Modes are *independent* and the evolution of the system is completely determined by a linear sum of the modes.
## Finding modes
There are several ways of finding normal modes for an oscillating system.
We will use the example of three springs with spring constant $k$ connected to two masses $m$ s.t.
$$
\begin{align}
m\ddot{x}_{1} & =-kx_{1}+k(x_{2}-x_{1}) \\
m\ddot{x}_{2} & =-kx_{2}+k(x_{1}-x_{2})
\end{align}
$$
### Intuition method
#mech/normal-modes/intuition-method 
We first guess that the two modes are
1. when both masses move together so $x_{1}=x_{2}$
2. when masses move oppositely so $x_{1}=-x_{2}$
For guess 1, we indeed find that
$$
\begin{align}
m\ddot{x}_{1} & =-kx_{1} \\
m\ddot{x}_{2} & =-kx_{2}
\end{align}
$$
which satisfies being a node with $\omega_{1}=\sqrt{ k /m }$ which gives the solution
$$
\begin{pmatrix}
x_{1} \\
x_{2}
\end{pmatrix}=A\begin{pmatrix}
1 \\
1
\end{pmatrix}\cos(\omega_{1}t+\phi_{1})
$$
and equally for guess 2, we see
$$
\begin{align}
m\ddot{x}_{1} & =-3kx_{1} \\
m\ddot{x}_{2} & =-3kx_{2}
\end{align}
$$
which is another mode with $\omega_{2}=\sqrt{ 3k /m }$ hence
$$
\begin{pmatrix}
x_{1} \\
x_{2}
\end{pmatrix}=B\begin{pmatrix}
1 \\
-1
\end{pmatrix}\cos(\omega_{2}t+\phi_{2})
$$
So we find the general solution of the system as
$$
\begin{align}
x_{1} & =A\cos(\omega_{1}t+\phi_{1})+B\cos(\omega_{2}t+\phi_{2}) \\
x_{2} & =A\cos(\omega_{1}t+\phi_{1})-B\cos(\omega_{2}t+\phi_{2})
\end{align}
$$
this solution has 4 constants for two 2nd order coupled [[Ordinary Differential Equations|ODEs]] so is fully solved.
### Decoupling method
#mech/normal-modes/decoupling-method 
This method is by rearranging the equations to be in terms of some single other dummy variable $q$. For example using the above system, we can add the two equations and subtract the two equations to get the pair
$$
\begin{align}
m(\ddot{x}_{1}+\ddot{x}_{2}) & =-k(x_{1}+x_{2}) \\
m(\ddot{x}_{1}-\ddot{x}_{2}) & =-3k(x_{1}-x_{2})
\end{align}
$$
we can then define $q_{1}=x_{1}+x_{2}$ and $q_{2}=x_{1}+x_{2}$ to get two decoupled equations with two solutions as before:
$$
\begin{align}
q_{1} & =A\cos(\omega_{1}t+\phi_{1}) \\
q_{2} & =B\cos(\omega_{2}t+\phi_{2})
\end{align}
$$
these solutions correspond to the guesses 1 and 2 from before, and we can then convert these back into solutions in $x$ since $x_{1}=q_{1}+q_{2}$, $x_{2}=q_{1}-q_{2}$ by scaling constants. Usually the coordinate sets are normalised though so
$$
\begin{vmatrix}
x_{1} \\
x_{2}
\end{vmatrix}=\begin{vmatrix}
q_{1} \\
q_{2}
\end{vmatrix}
$$
hence $q_{1}=(x_{1}+x_{2}) /\sqrt{ 2 }$, $q_{2}=(x_{1}-x_{2}) /\sqrt{ 2 }$.
### Energy analysis
#mech/normal-modes/energy 
The total energy in this system is given by $U=T+V$ or
$$
U=\underbrace{ \left( \frac{1}{2}m\dot{x}_{1}^{2}+\frac{1}{2}m\dot{x}_{2} \right) }_{ \text{KE of }m_{1}\text{ and }m_{2} }+\underbrace{ \left( \frac{1}{2}kx^{2}_{1}+\frac{1}{2}k(x_{1}-x_{2})^{2} +\frac{1}{2}kx_{2}^{2}\right) }_{ \text{PE in springs} }
$$
In terms of normalised normal coordinates this becomes
$$
U=\underbrace{ \left( \frac{1}{2}m\dot{q}_{1}^{2}+\frac{1}{2}m\omega_{1}^{2}q_{1}^{2} \right) }_{ \text{Energy of mode 1} }+\underbrace{ \left( \frac{1}{2}m\dot{q}_{2}^{2}+\frac{1}{2}m\omega_{2}^{2}q_{2}^{2} \right) }_{ \text{Energy of mode 2} }
$$
So the energy separates out into linearly independent modes. This contrasts the original where energy is transferred between the springs due to cross-terms in the potential energy.
### Matrix method
#mech/normal-modes/matrix-method 
Better example in [[Lecture 2026-01-27 9am.excalidraw|notes]] but involves
1. Rewriting the equations of motion in matrix form $M \ddot{\vec{x}}=-K\vec{x}$
2. Substituting for a complex $\vec{z}=\vec{a}e^{i(\omega t+\phi)}$ and then rearranging so
3. $(K-M\omega^{2})\vec{a}=0$ which is a generalised [[Eigenvalues & Eigenvectors|eigenvalue equation]] and is solved for $\omega$ by $|K-M\omega^{2}|=0$.
4. Now substituting $\omega^{2}$ to find generalised eigenvectors. Each pair $(\omega^{2},\vec{v})$ represents a mode.
5. Solving each individual mode to get final solution - note that have to take into account value of $\omega^{2}$, if it is zero then additional constants have to be introduced by raising the degree.

For the previous example this would look like
$$
\begin{pmatrix}
m & 0 \\
0 & m
\end{pmatrix}\begin{pmatrix}
\ddot{x}_{1} \\
\ddot{x}_{2}
\end{pmatrix}=-\begin{pmatrix}
2k & -k \\
-k & 2k
\end{pmatrix}\begin{pmatrix}
x_{1} \\
x_{2}
\end{pmatrix}
$$
Note that $K$ is symmetric due to N3. Hence
$$
\begin{vmatrix}
2k-m\omega^{2} & -k \\
-k & 2k-m\omega^{2}
\end{vmatrix}=m^{2}\left( \omega^{2}-\frac{k}{m} \right)\left( \omega^{2}-\frac{3k}{m} \right)=0
$$
which gives the expected two $\omega$ values for the two known modes. This then generates the two mode vectors
$$
\vec{a}_{1}=A\begin{pmatrix}
1 \\
1
\end{pmatrix},\,\vec{a}_{2}=B\begin{pmatrix}
1 \\
-1
\end{pmatrix}
$$
so the general solution is
$$
\vec{x}=\vec{a}_{1}\cos(\omega_{1}t+\phi_{1})+\vec{a}_{2}\cos(\omega_{2}t+\phi_{2})
$$
as expected.
### Change of basis method
#mech/normal-modes/change-of-basis-method 
This method is basically identical to the previous one but characterised differently - namely we write the equation as
$$
\ddot{\vec{x}}=A\vec{x}
$$
If we diagonalize $A$, (which we always can since $A$ is symmetric) we can find $\Lambda=P^{T}AP$ as the diagonal matrix so
$$
\ddot{\vec{q}}=\Lambda \vec{q}
$$
which is easily solved for $\vec{q}$. Then this can be translated back using $\vec{x}=P\vec{q}$, which requires finding the (normalised) eigenvectors.

Hence, the normal modes represent the new basis in which we are expressing the system. It also explains why the matrix method works.
### Beats
#mech/normal-modes/beats 
If we have a solution as before of the form
$$
\begin{align}
x_{1} & =\frac{a}{2}(\cos(\omega_{1}t)+\cos(\omega_{2}t)) \\
x_{2} & =\frac{a}{2}(\cos(\omega_{1}t)+\cos(\omega_{2}t))
\end{align}
$$
then we can use sum-to-product identities to give
$$
\begin{align}
x_{1} & =a\cos\left( \frac{(\omega_{1}+\omega_{2} )t}{2} \right)\cos\left( \frac{(\omega_{1}-\omega_{2})t}{2} \right) \\
 x_{2} & =-a\sin\left( \frac{(\omega_{1}+\omega_{2})t}{2} \right)\sin\left( \frac{(\omega_{1}-\omega_{2})t}{2} \right)
\end{align}
$$
So we see a 'beat frequency' $\omega _k=(\omega_{1}-\omega_{2}) /2$ and an oscillation frequency $\omega _k=(\omega_{1}+\omega_{2}) /2$.
## Lumpy string
#mech/normal-modes/lumpy-string 
Considering a lumpy string which is
- flexible elastic string to which $N$ particles of mass $m$, each $l$ apart are attached.
- fixed at each end
- small transvers displacements applied.
For any arbitrary mass $n=p$ along the string
$$
\ddot{y}_{p}=-\frac{T}{ml}(-y_{p+1}+2y_{p}-y_{p-1})
$$
is the equation of motion. Considering the whole system and putting into matrix form $\ddot{\vec{y}}=-A\vec{y}$ we can find the relationships
$$
\begin{align}
\frac{a_{p-1}+a_{p+1}}{a_{p}} & =\frac{2\omega_{0}^{2}-\omega^{2}}{\omega_{0}^{2}} \\
a_{0} & =a_{N+1}=0
\end{align}
$$
where $\omega_{0}=\frac{T}{ml}$. The solution for this system is given by $a_{p}=C\sin p\theta$ which after solving gives the coefficients as
$$
a_{p}=C\sin\left( \frac{n\pi}{N+1}p \right),\quad n=1,2,\dots,N
$$
and
$$
\omega_{n}=2\omega_{0}\sin \frac{n\pi}{2(N+1)}
$$
which are analogous to the harmonics of a string. The complete solution for a particular mass $p$ is therefore given by
$$
y_{p}=\sum_{n=1}^{N} C_{n}\sin\left( \frac{n\pi}{N+1}p \right)\cos(\omega_{n}t+\phi_{n})
$$
so we have $2n$ constants as expected.
### Continuous case
#mech/normal-modes/continuous-case 
As we take the limit of $N\to \infty$, i.e. we take the length of the string as $L=(N+1)l$, the mass as $M=Nm$ and the density as $\rho=\frac{M}{L}\approx\frac{m}{l}$, and the chosen position of interest along the string as $x=pl$ then in the limit,
$$
y_{n}(x,t)=C_{n}\cdot\underbrace{ \sin\left( \frac{n\pi x}{L} \right) }_{ \text{spatial info} }\cdot\underbrace{ \cos(\omega _{n}t+\phi_{n}) }_{ \text{time info} }
$$
where 
$$
\omega_{n}=\frac{n\pi}{L}\sqrt{ \frac{T}{\rho} }
$$
so we find the **fundamental frequency** #waves/fundamental-frequency as
$$
\omega_{1}=\frac{\pi}{L}\sqrt{ \frac{T}{\rho} }
$$
