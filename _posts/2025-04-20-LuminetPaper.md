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
'''
We began by defining the black hole mass M, the Schwarzschild radius r_s (horizon), 
the photon radius r_c (critical radius), the critical impact parameter b_c, and the function effective potential. 
We use geometrized units and create an arrange of values for r.
'''
M   = 1
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
\varphi_\infty &= 2\left(\frac{P}{Q}\right)^{1/2}\int^{\pi/2}_{\zeta\infty}(1-\kappa^2\sin^2x)^{-1/2}dx = 2\left(\frac{P}{Q}\right)^{1/2} \left(K(\kappa)-F(\zeta\infty,\kappa)\right)\quad(6).
\end{aligned}
$$

Here, $$K(\kappa)$$ is the complete elliptic integral of modulus

$$\kappa \equiv \left(Q-P\frac{6M}{2Q}\right)^{1/2}$$

and $$F(\zeta\infty.\kappa)$$ is the elliptic integral of modulus $$\kappa$$ and argument $$\zeta_\infty$$ such that

$$
\sin^2\zeta_\infty = \frac{Q-P+2M}{Q-P+6M}.
$$

The total deviation of the light ray, $$\mu$$, is given by $$\varphi_\infty=\frac{\pi}{2}+\frac{\mu}{2}$$. It is interesting to give the formulas at the limit $$P>>M$$ and $$P\rightarrow 3M$$. For very large $$P$$ (weak field approximation) we verify immediately that $$\mu\sim 4M/P$$, $$P\rightarrow b$$ (See the derivation here). This famous formula for the deflection of light ray in the gravitational field of a spherical star leads to the Rutherford limit for the differential cross-section $$\frac{d\sigma}{d\Omega}=\frac{b}{\sin{\mu}}\lvert\frac{db}{d\mu}\rvert$$ (which is precisely the number of particles per unit solid angle $$d\Omega=2\pi\sin\mu d\mu$$ collected by the observer); which is independent of the energy of the incident photons. 

For $$P$$ near the critical value $$3M$$, i.e. for $$b$$ near $$b_c$$, the asymptotic expansion of the elliptic funtions for modulus $$\kappa\sim 1$$ (Gradshteyn and Ryzhik, 1965) leads to the important relation:

$$b = 5.19695M+3.4823M e^{-\mu} \quad(7)$$

In fact, the particles that come off at a given angle $$\mu$$ in clude not only those that have really been deflected by $$\mu$$, also those that have been deflected by $$\mu+2\pi$$, $$\mu+4\pi$$, ..., $$\mu+2n\pi$$, etc. (an infinite series of contributions), and which correspond to the following impact parameters (See the derivation here):

$$
\begin{aligned}
b_0&=b_c+3.4823M e^{-\mu} & \text{(zero circuit)}\\
b_1&=b_c+3.4823M e^{-(\mu+2\pi)} & \text{(one circuit)}\\
...&...\\
b_n&=b_c+3.4823M e^{-(\mu+2n\pi)} &\text{(two circuit)}\\\\
...&...\\
b_\infty&=b_c & \text{(infinity circuits)}\\
\end{aligned}
$$

We see that the nth order contribution to the differential cross section is proprotional to

$$
\frac{db_n}{d\mu} = -  3.4823 M e^{-(\mu+2n\pi)}\quad(8)
$$

Thus the total contribution of successive numbers of circuits is proportional to $$\sum^{\infty}_0e^{-2n\pi}=\frac{1}{1-e^{-2\pi}}$$. Thus in practice the contribution for $$n\geq 2$$ is really negligeble. We shall see bellow the observational consequences of this fact.

Once the properties of the deflectionangle $$\mu(b)$$ are known, one is ready to work out what is the image of the black hole illuminatted by a parallel bean light, as seen by an observer placed on $$\Theta-$$direction. It follows from the above discussion that rays that reach the observer will give a picture consisting of a black disk of radius $$b_c= 5.19695M$$ surrounded by 'ghost' rings of different radius and brightness. The exterior ring corresponds to the rays that have not described any circuit; as $$b$$ approaches its critical value $$b_c$$, the rays described more and more circuits, until in the limit $$b_\infty = b_c$$ (infinite circuits) the rays are captured.

To conclue this section, the only ring practically distinguishable would be the external one. This is not a matter of brightness, but also a matter of resolution. 

{% highlight python %}
import warnings
warnings.filterwarnings('ignore')
'''
We began by defining the black hole mass M, the Schwarzschild radius r_s (horizon), 
the photon radius r_c (critical radius), the critical impact parameter b_c, and the function effective potential. 
We use geometrized units and create an arrange of values for r.
'''

def intensity_integrand(u):
    #Integral terms
    t1 = (1-2*M*u)**2
    t2 = 1/(1-b**2*u**2+2*M*b**2*u**3)
    return np.sqrt(t1*t2)

Denominator_intensity = lambda x: 1-b**2*x**2+2*M*b**2*x**3
Denominator = lambda x: (1/b**2)-x**2+2*M*x**3
b_intensity = np.arange(1e-3,20,1e-3)

I_o=np.zeros_like(b_intensity)

for i, b in enumerate(b_intensity):
    if b<b_c:
        specific_intensity = quad(intensity_integrand,0,1/2*M)[0]
        I_o[i]=specific_intensity
    else:
        uroot = float(optimize.fsolve(Denominator,0.15,xtol=1e-5))
        specific_intensity = quad(intensity_integrand,0, uroot)[0]
        I_o[i]=specific_intensity        

'''
Specific intensity function of b
'''
Io_interpol= make_interp_spline(b_intensity,I_o,k=3, t=None, bc_type=None, axis=0, check_finite=True)

plt.figure(figsize=(10, 10))
plt.plot(b_intensity,I_o,color= 'black')
plt.plot(-b_intensity,I_o,color='black')
plt.axvline(x=  b_c, color='black', linestyle=':', label='r = 10')
plt.axvline(x= -b_c, color='black', linestyle=':', label='r = 10')
#plt.plot(b_intensity,Io_interpol(b_intensity),'--',color='Red')
#plt.plot(-b_intensity,Io_interpol(b_intensity),'--',color='Red')
plt.title('Specific intensity')
plt.xlabel('b/M',fontsize=14)
plt.ylabel('$I_{obs}$',fontsize=14)
plt.xlim(-10,10)
plt.ylim(0.0,1)
plt.grid(True)
{% endhighlight %}

| Figure 1 | Figure 2 |
|----------|----------|
| ![](figure1.png) | ![](figure2.png) |




## Enjoy reading this post while listen the Interstellar music!

{% include embed.html url="https://www.youtube.com/embed/5gO0xpY_Y3E?si=3obwjvQjHsYChMGA"%}
