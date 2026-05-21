---
tags:
  - complex/jordans-lemma
date-created: 2026-05-19
template-version: m.0
---
[[Complex Numbers]]

Consider an $f$ meromorphic on the upper half plane, with a contour $C_{R}=\{ Re^{i\theta}\mid \theta \in[0,\pi] \}$ that does not pass through any singularities, then if the function is of the form $f(z)=e^{iaz}g(z)$, with a positive parameter $a$, then **Jordan's lemma** states that
$$
\left\lvert  \int_{C_{R}}f(z)\,dz  \right\rvert \leq \frac{\pi}{a}M_{R}\qquad\text{where}\qquad M_{R}:=\underset{ \theta \in[0,\pi] }{ \text{max} }\lvert g(Re^{i\theta}) \rvert 
$$
with equality when $g$ vanishes everywhere so both sides are $0$. An analogous statement holds in the lower half plane when $a<0$. 

If $f$ continuous on $C_{R}$ for all large $R$ and 
$$
\lim_{ R \to \infty } M_{R}=0\implies \lim_{ R \to \infty } \int_{C_{R}}f(z)\,dz=0
$$
this is the case which will be used most often as it allows us to eliminate annoying terms in contour integrals in the limit.
#### Jordan's lemma example
Take the integral
$$
I=\int_{-\infty}^{\infty} \frac{xe^{iax}}{1+x^{2}} \, dx 
$$
around the standard semi-circular and linear path in the upper half plane $C$, so we have the complex version
$$
\tilde{I}=\oint_{C} \frac{ze^{iaz}}{1+z^{2}}\,dz=\int_{-R}^{R} \frac{xe^{iax}}{1+x^{2}} \, dx +\int_{C_{R}} g(z) e^{iaz}\, dz =I_{1}+I_{2}
$$
then as $R\to \infty$, $I_{1}\to I$ and then by Jordan's lemma, since
$$
g(z)=\frac{z}{1+z^{2}}\sim \frac{1}{z}
$$
we have $\text{max}(g(z))\to0$ as $R\to \infty$ and therefore $I_{2}\to0$ as well. Now we just evaluate the residue of the pole in the contour, that is
$$
\int_{-\infty}^{\infty}  \frac{xe^{iax}}{1+x^{2}} \, dx =2\pi i\,\text{Res}[f,i]=\pi ie^{-a}
$$
