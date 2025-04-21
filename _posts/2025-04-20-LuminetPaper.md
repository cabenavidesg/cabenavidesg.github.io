---
title:  "Image of spherical black hole with thin accretion disk (Luminet 1979)"
mathjax: true
layout: post
categories: media
---

![First black hole image](/assets/Image1979.png)
## Abstract

Black hole accretion distks are crretnly a topic of widespread interest in astrophysics and are suppose to play and important role in a number of high-energy situations. The present paper contains an investigation of the optical appearance of a spherical black hole sourrounde by a thin accretion disk. Isoradial curves corresponding to photons emitted at constant radius from the hole as seen by a distant observer in arbitrary direction have been plotted, as well as spectral shifts arising from gravitational and doppler shifts. By the results of Page and Thorne (1974) the relative intrisinc intensiy of radiation emitted by the disk at a given radius is a known function of the radius only, so that it is possible to calculate the exact distribution of observerd  bolometric flux. Direct and secondary images are plotted and the strong asymmetry in the flux distribution due to the rotation of the disk  is exhibited. Finally, a simulated photograph is constructed, valid for black holes of any mass accreting matter at any moferate rate. 

## Introduction

In order to be visible a black hole has of course to by illuminated, like any ordinary body. One of the simplest possibilities would be for the black hole to be illuminated by a distant localized source which in practice might be a companion star in a loosely bound binary system. A more interesting and observationally important possibility is that in which the light source is provided by an emitting accretion disk around the black hole, such as may occurt in a tight binary system with overflow from the primary, and perhaps also on a much larger scale in a dense galactic nucleus. The general problem of a the oprical appearance of a black hole is relared to the analysis of trajectories in the gravitational field of black holes. For spherical, static, electric-free black holes (whose external space-time geometry is described by Schwarzschild metric) this problem is already well know (Hagihara, 1931; Darwin, 1959; for a summary, see Miner etal. 1973 MTW). In Sec. 2 we give only a brief outline of it with basic equations, trying to point out the major features which appear latter. All our calculations are don in the geometrical optics approximation (for a study of wave-aspects, see Sanchez, 1977). In Sec. 3 we calculate the apparent shape of the circular rings orbiting a non-rotating black hole and the results are depicted in Figs. 5-6. In Sec. 4 we recall the standard analysis by Novikov and Thorne (1973) of the problem of energy release by a thin accretion disk in a general astrophysical context, focusing attention more particularly on the analytic solution for the surface distribution of energy release that was derived by Page and Thorne (1974) in the limiting case of a sufficiently low accretion rate. In terms of this idealized (but appropriate circumstances, realistic) model, we calculate the distribution of bolometric flux as seen by distant observers at various angles above the plane of the disk (Figs. 9-11).

## Images of Bare Black holes

Before analyzing the general problems of a spherical black hole surrounded by an emitting accretion disk, it is instructive to investigate a more simple case in which all the dynamics are already contained, namely the problem of the return of ligth from a bare black hole illuminated by a light beam projected by a distant source. It is conceptually interesting to calculate the precise apparent pattern of the reflected light, since some of the main characteristics features of the general geometrical optics problem are illustrated thereby.

The Schawarzschild metric for a static pure vacuum black hole may be written as

$$ds^2 = -\left(1-\frac{2M}{r}\right)dt^2+\left(1-\frac{2M}{r}\right)^{-1}dr^2+r^2\left(d\theta^2+\sin^2\theta d\varphi^2\right)\quad(1)$$

where $$r$$, $$\theta$$ and $$\varphi$$ are spherical coordinates and the unit system is chosen such that $$G=c=1$$. $$M$$ is the relativistic mass of the black hole (which has dimenssions of lenght). In this standard coordinate system the horizon forming the surface of the hole is located a the Schwarzschild radius $$r_s=2M$$, see Eq.(1).

## MathJax

You can enable MathJax by setting `mathjax: true` on a page or globally in the `_config.yml`. Some examples:

[Euler's formula](https://en.wikipedia.org/wiki/Euler%27s_formula) relates the  complex exponential function to the trigonometric functions.

$$ e^{i\theta}=\cos(\theta)+i\sin(\theta) $$

The [Euler-Lagrange](https://en.wikipedia.org/wiki/Lagrangian_mechanics) differential equation is the fundamental equation of calculus of variations.

$$ \frac{\mathrm{d}}{\mathrm{d}t} \left ( \frac{\partial L}{\partial \dot{q}} \right ) = \frac{\partial L}{\partial q} $$

The [Schrödinger equation](https://en.wikipedia.org/wiki/Schr%C3%B6dinger_equation) describes how the quantum state of a quantum system changes with time.

$$ i\hbar\frac{\partial}{\partial t} \Psi(\mathbf{r},t) = \left [ \frac{-\hbar^2}{2\mu}\nabla^2 + V(\mathbf{r},t)\right ] \Psi(\mathbf{r},t) $$

## Code

Embed code by putting `{{ "{% highlight language " }}%}` `{{ "{% endhighlight " }}%}` blocks around it. Adding the parameter `linenos` will show source lines besides the code.

{% highlight c %}

static void asyncEnabled(Dict* args, void* vAdmin, String* txid, struct Allocator* requestAlloc)
{
    struct Admin* admin = Identity_check((struct Admin*) vAdmin);
    int64_t enabled = admin->asyncEnabled;
    Dict d = Dict_CONST(String_CONST("asyncEnabled"), Int_OBJ(enabled), NULL);
    Admin_sendMessage(&d, txid, admin);
}

{% endhighlight %}

## Gists

With the `jekyll-gist` plugin, which is preinstalled on Github Pages, you can embed gists simply by using the `gist` command:

<script src="https://gist.github.com/5555251.js?file=gist.md"></script>

## Images

Upload an image to the *assets* folder and embed it with `![title](/assets/name.jpg))`. Keep in mind that the path needs to be adjusted if Jekyll is run inside a subfolder.

A wrapper `div` with the class `large` can be used to increase the width of an image or iframe.

![Flower](https://user-images.githubusercontent.com/4943215/55412447-bcdb6c80-5567-11e9-8d12-b1e35fd5e50c.jpg)

[Flower](https://unsplash.com/photos/iGrsa9rL11o) by Tj Holowaychuk

## Embedded content

You can also embed a lot of stuff, for example from YouTube, using the `embed.html` include.

{% include embed.html url="https://www.youtube.com/embed/eVv6P0VcuJo?si=KLCf1Q6270RbyWHy"%}
