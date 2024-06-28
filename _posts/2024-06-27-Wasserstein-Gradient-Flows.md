---
layout: post
categories: Stochastics
---

# Wasserstein Gradient Flows

How to understand the heat equation as the gradient flow of entropy in Wasserstein metric?


## Benamou-Brenier Formula
For $\mu \in P_2(\mathbb{R}^n)$, $v: \mathbb{R}^n \to \mathbb{R}^n$ Borel measurable,
$$A(v,\mu):= \int_{\mathbb{R}^n} |v|^2 \mathrm{d} \mu.$$
Theorem 17.2 For all $\mu_0, \mu_1 \in P_2(\mathbb{R}^n)$, 
$$W^2_2(\mu_0,\mu_1) = \min \big\{ \int_0^1 A(v_t,\mu_t) \mathrm{d} t : \partial_t \mu_t + \mathrm{div} (v_t \mu_t) = 0 \quad \text{in} (0,1)\times \mathbb{R}^n \big\}$$
the minimum is over all curves 
$\mu_t:[0,1]\to P_2(\mathbb{R}^n)$ 
continuous wrt the weak topology.

Geodesic represented by solutions to the continuity equation.
Solution of continuity equation is related to the absolutely continuous curve wrt $W^2$

For any AC curve, there exists a velocity field so that the AC curve solves the associated continuity equation and the quadratic action equals to the metric derivative squared.

Elements $s$ of the tangent space $T_{\rho}P^a_2(\bR^n)$ are functions with null mean

The gradient tangent vectors $v=\nabla \phi$ are coupled to tangent vectors $s$ by the PDE $-\mathrm{div}((\nabla \phi)\rho) =s.$ The metric tensor is 
$\langle s,s'\rangle_\rho = \int_{R^n} \langle \nabla \phi , \nabla \phi' \rangle \rho \mathrm{d} x$ where $-\mathrm{div}((\nabla \phi) \rho )= s$.
