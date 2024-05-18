---
layout: post
categories: Differential equations
---
# Lorenz attractor and the butterfly effect

The Lorenz system is given by

$$ \frac{d x}{d t} = \sigma(y-x) $$

$$ \frac{d y}{d t} = x(\rho -z) - y$$

$$ \frac{d z}{d t} = x y -\beta z$$

This is a prototypical example of chaotic behaviour in deterministic system. It is a simple model for the atmosphere. The slight change in initial condition results in drastic change in the future behaviour is interpreted as the butterfly effect in which the flap of the wings of a butterfly can cause an extreme weather event. 

The trajectory in the phase space also resemble a butterfly. One can see in the animation there are two attractors.

<video width="320" height="240" controls>
  <source src="https://solomon-lam.github.io/assets/lorenz_attractor_sensitivity.mp4" type="video/mp4">
</video>
