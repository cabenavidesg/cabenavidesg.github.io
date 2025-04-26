---
title:  "Image of spherical black hole with thin accretion disk"
mathjax: true
layout: post
categories: media
---

![First black hole image](/assets/Image1979.png)by [Jean-Pierre Luminet 1979](https://ui.adsabs.harvard.edu/abs/1979A%26A....75..228L/abstract)
## Abstract

Black hole accretion distks are crretnly a topic of widespread interest in astrophysics and are suppose to play and important role in a number of high-energy situations. The present paper contains an investigation of the optical appearance of a spherical black hole sourrounde by a thin accretion disk. Isoradial curves corresponding to photons emitted at constant radius from the hole as seen by a distant observer in arbitrary direction have been plotted, as well as spectral shifts arising from gravitational and doppler shifts. By the results of Page and Thorne (1974) the relative intrisinc intensiy of radiation emitted by the disk at a given radius is a known function of the radius only, so that it is possible to calculate the exact distribution of observerd  bolometric flux. Direct and secondary images are plotted and the strong asymmetry in the flux distribution due to the rotation of the disk  is exhibited. Finally, a simulated photograph is constructed, valid for black holes of any mass accreting matter at any moferate rate. 

## Introduction

In order to be visible a black hole has of course to by illuminated, like any ordinary body. One of the simplest possibilities would be for the black hole to be illuminated by a distant localized source which in practice might be a companion star in a loosely bound binary system. A more interesting and observationally important possibility is that in which the light source is provided by an emitting accretion disk around the black hole, such as may occurt in a tight binary system with overflow from the primary, and perhaps also on a much larger scale in a dense galactic nucleus. The general problem of a the oprical appearance of a black hole is relared to the analysis of trajectories in the gravitational field of black holes. For spherical, static, electric-free black holes (whose external space-time geometry is described by Schwarzschild metric) this problem is already well know (Hagihara, 1931; Darwin, 1959; for a summary, see Miner etal. 1973 MTW). In Sec. 2 we give only a brief outline of it with basic equations, trying to point out the major features which appear latter. All our calculations are don in the geometrical optics approximation (for a study of wave-aspects, see Sanchez, 1977). In Sec. 3 we calculate the apparent shape of the circular rings orbiting a non-rotating black hole and the results are depicted in Figs. 5-6. In Sec. 4 we recall the standard analysis by Novikov and Thorne (1973) of the problem of energy release by a thin accretion disk in a general astrophysical context, focusing attention more particularly on the analytic solution for the surface distribution of energy release that was derived by Page and Thorne (1974) in the limiting case of a sufficiently low accretion rate. In terms of this idealized (but appropriate circumstances, realistic) model, we calculate the distribution of bolometric flux as seen by distant observers at various angles above the plane of the disk (Figs. 9-11).

## Images of Bare Black holes

Before analyzing the general problems of a spherical black hole surrounded by an emitting accretion disk, it is instructive to investigate a more simple case in which all the dynamics are already contained, namely the problem of the return of ligth from a bare black hole illuminated by a light beam projected by a distant source. It is conceptually interesting to calculate the precise apparent pattern of the reflected light, since some of the main characteristics features of the general geometrical optics problem are illustrated thereby.

The Schawarzschild metric for a static pure vacuum black hole may be written as

$$ds^2 = -\left(1-\frac{2M}{r}\right)dt^2+\left(1-\frac{2M}{r}\right)^{-1}dr^2+r^2\left(d\theta^2+\sin^2\theta d\varphi^2\right)\quad(1)$$

where $$r$$, $$\theta$$ and $$\varphi$$ are spherical coordinates and the unit system is chosen such that $$G=c=1$$. $$M$$ is the relativistic mass of the black hole (which has dimenssions of lenght). In this standard coordinate system the horizon forming the surface of the hole is located a the Schwarzschild radius $$r_s=2M$$, see Eq.(1).

One can take advanange of the spherical symmetry to choose the equatorial plane $$\theta=\pi/2$$ so as to contain any particular photon trajectory under consideration. The trajectories will then satisfy the differential equation (See derivation equation 2):

$$\left(\frac{1}{r^2}\left(\frac{dr}{d\varphi}\right)^2\right)^2+\frac{1}{r^2}\left(1-\frac{2M}{r}\right)=\frac{1}{b^2}\quad(2)$$

The second term in the left member can be interpreted as the effective potential $$V(r)$$, in analogy with the non-relativistic mechanics. The motion does not depend on the photon energy $$E$$ and on its angular momentum $$L$$, but only on the ration $$L/E=b$$, which is the impact parameter at infinty.

Let the observer be in a direction fixed by the polar angle $$\varphi_0$$ in the Schwarschild metric, at a radius $$r_0>> M$$ (the observer is at infinity). The rays emitted by a distance source of light deflected by the black hole intersect the observert's detector (for example a photographic plate) at a distance $$b$$ from the the central point of the plaque. From (2), one sees that a ray with impac parameter $$b$$ can reach a point at a distance $$r$$ ony if $$b\leq [V(r)]^{-1/2}$$. This can be seen directly from (2), from which

$$\frac{1}{r^2}\left(\frac{dr}{d\varphi}\right)=\sqrt{\frac{1}{b^2}-V(r)}$$

It is clear that the rim of te ''optical'' black hole corresponds to rays which arre marginally trapped by the balck hole: the spiral around many times before reaching the observer, and in our case the rim (borde) is located at $$b_c= 3\sqrt{3M}\approx 5.19695M$$. Thus, the apparent diameter of the hole is about $$10.38$$.

{% highlight python %}
"""
In this part of the code, we define the black hole mass M, the Schwarzschild radius r_s (horizon), 
the photon radius r_c (critical radius), the critical impact parameter b_c, and the function effective potential. 
We use geometrized units and create an arrange of values for r.
"""
M = 1
r_s = 2*M
r_c = 3*M
b_c = 3*np.sqrt(3)*M
radial_coordinate = np.arange(r_s,100, 0.01)
"""
Definition of the effective potential
"""
def V(r):
    Veff = (1/r**2)*(1-r_s/r)
    return Veff
{% endhighlight %}

![Effective potential](/assets/EffectivePotential.png)

Let usreturn to Eq. (2). Letting $$u=1/r$$, we get (See derivation equation 3):

$$\left(\frac{du}{d\varphi}\right)^2=2Mu^3-u^2+\frac{1}{b^2}\equiv 2MG(u)\quad(3)$$

Let us call $$u_1$$, $$u_2$$ and $$u_3$$, the roots of $$G(u)$$, with $$u_1< u_2< u_3$$, if they are all real. Comploete information about the rays is contained in (3), so it is useful to investigate its mathematical structure. It is easy to see that $$G(u)$$ possesses only one real root (because $$u_1u_2+u_1u_3+u_2u_3=0$$; see [Chandrasekhar](https://inspirehep.net/literature/224457), and that we have the following possible cases:

   1. $$b > b_c$$: $$u_1 \le 0< u_2 < u_3$$.
   2. $$b = b_c$$: $$u_1=-\frac{1}{6M}$$, $$u_2 = u_3 = \frac{1}{3M}$$.
   3. $$b < b_c$$: $$u_1\le 0$$, $$u_2$$, and $$u_3$$ complex conjugate.

We are interested in orbits reaching the observer's plane, i. e., for which $$b > b_c$$. These orbits posses a periastron, and itis convenient to express all the quantities in terms of the periastron distance $$P$$. so that if we let: $$Q^2\equiv (P-2M)(P-6M)$$, we get (See the derivation of equations 4, 5 and 6.):

$$u_1= -\frac{Q-P+2M}{4MP}, u_2=\frac{1}{P}, u_3 = \frac{Q+P-2M}{4MP} \quad(4)$$ 

$$b^2  = \frac{P^3}{(P-2M)} \quad(5)$$

So, given a value of the periastron, we obtain a value for the impact parameeter at infintiy. 


![First black hole image](/assets/figure1.jpeg) by [Jean-Pierre Luminet 1979](https://ui.adsabs.harvard.edu/abs/1979A%26A....75..228L/abstract)


Equation (3) must be integrated over the range of values where $$u$$ and $$G(u)$$ are positive; i. e. between $$u_2$$ and $$0$$. Figure 1 shows the corresponding trajectory of the ray. We assume that $$r_0>> M$$ is really at infinity (i. e. that the impact parameter on the plate is really $$b$$, which is a good assumption), so that the final value, $$\varphi_\infty$$, of $$\varphi$$ is given by:

$$\varphi_\infty = \frac{1}{\sqrt{2M}}\int^{u_2}_0\frac{dx}{\sqrt{G(x)}}\quad(5a)$$
    
This integral can be transformed into a classical Jacobian elliptic integral (See derivation of equations 4,5 and 6)

$$
\begin{aligned}
\varphi_\infty &= 2\left(\frac{P}{Q}\right)^{1/2}\int^{\pi/2}_{\zeta\infty}(1-\kappa^2\sin^2x)^{-1/2}dx = 2\left(\frac{P}{Q}\right)^{1/2} \left(K(\kappa)-F(\zeta\infty,\kappa)\right)
\end{aligned}
$$









## Enjoy reading this post while listen the Interstellar music!

{% include embed.html url="https://www.youtube.com/embed/5gO0xpY_Y3E?si=3obwjvQjHsYChMGA"%}
