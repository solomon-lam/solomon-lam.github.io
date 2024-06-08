---
layout: post
categories: Differential_equations
---
# Lorenz attractor and the butterfly effect

The butterfly image from [Wikipedia](https://en.wikipedia.org/wiki/Butterfly_effect) is the visualization of the solution of the Lorenz system in a phase portrait.<img src="https://github.com/solomon-lam/solomon-lam.github.io/assets/43318214/0c8bf191-0242-4481-a1b0-bb2208f71350" width="500"/>


The Lorenz system is a deterministic system of ordinary differential equations given by

$$ \frac{d x}{d t} = \sigma(y-x) $$

$$ \frac{d y}{d t} = x(\rho -z) - y$$

$$ \frac{d z}{d t} = x y -\beta z$$

The image above in fact is a 2D projection of the trajectory of the 3D system in xyz-coordinates.

This system is famous because it a prototypical example of chaotic behaviour in deterministic system. It is a simple model for the atmosphere. The slight change in initial condition results in drastic change in the future behaviour is interpreted as the butterfly effect in which the flap of the wings of a butterfly can cause an extreme weather event. 

The trajectory in the phase space also resemble a butterfly. One can see in the animation below with slightly different initial conditions, the trajectory in long time can be very different. This is shown by the colour blue and orange to represent the trajectory of two initial conditions.

<video width="500" height="350" controls>
  <source src="https://solomon-lam.github.io/assets/lorenz_attractor_sensitivity.mp4" type="video/mp4">
</video>
