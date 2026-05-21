---
tags:
  - optics/lens
date-created: 2026-01-03
template-version: m.0
---
For an imaging system to produce an image all rays of light leaving the focus must converge on the complementary focus. So, we find the optical path, then find the conditions for which every ray leaving $F$ converges on $F'$. 

Two approximations:
- The *paraxial approximation* #optics/paraxial-approximation that $\sin\theta \approx \tan\theta\approx\theta$ i.e. we assume rays are nearly parallel so angles are small.
- The *thin lens approximation* #optics/thin-lens-approximation that the thickness of the lens is much smaller than the radii of curvature or the distances between focii.

When we apply this and use [[Optics#Fermat Principle|Fermat principle]] we find the condition for forming an image is
$$
d(z)=d(0)-\frac{z^{2}}{2(n-1)}\left( \frac{1}{|OA'|}+\frac{1}{|AO|} \right)
$$
Where $d(z)$ is the thickness of the lens at a distance $z$ from the focal axis.

#optics/focal-length
We denote the quantity in the brackets as $\frac{1}{f}=P$, where $f$ is the **focal length** and $P$ is the *power* of the lens. Hence, the optimal shape for a lens is a **parabola**, however spherical lenses approximate this to second order.
#### Convex lens
#optics/convex-lens 
Is composed of two spherical slices of radius $R_{1}$ and $R_{2}$. We have the standard lens equation
$$
\frac{1}{u}+\frac{1}{v}=(n-1)\left( \frac{1}{R_{1}}+\frac{1}{R_{2}} \right)=\frac{1}{f}
$$
For second order there is a correction term ("thick" lens equation), which isn't needed usually:
$$
\frac{1}{u}+\frac{1}{v}=(n-1)\left( \frac{1}{R_{1}}+\frac{1}{R_{2}}-\frac{n-1}{n} \frac{d(0)}{R_{1}R_{2}} \right)
$$
Convex lenses are **converging lenses**.
#### Concave lens
#optics/concave-lens 
We find for a concave lens that
$$
\frac{1}{u}-\frac{1}{v}=-(n-1)\left( \frac{1}{R_{1}}+\frac{1}{R_{2}} \right)
$$
If we consider that the radii for a concave slice are negative, and same with the image being *virtual*, this reduces to the regular lens-makers formula.
#### Refracting telescope
#optics/refracting-telescope 
Aim is to form an image at infinity of an object at infinity, with some magnification.

The angular magnification is given by $M=\frac{f_{o}}{f_{e}}$ with the focal lengths of the objective lens and eyepiece, respectively. The diameter of the exit pupil can be found as the diameter of the objective lens divided by the magnification.
#### Compound microscope
#optics/compound-microscope 
Aim is to form an image much larger than its object size at the **Puntum Proximum** $P_{p}=25\text{cm}$. 

We have 
$$
M\approx \frac{LP_{p}}{f_{o}f_{e}}
$$