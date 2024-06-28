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
$$W^2_2(\mu_0,\mu_1) = \min \int_0^1 A(v_t,\mu_t) \mathrm{d} t : \partial_t \mu_t + \mathrm{div} (v_t \mu_t) = 0 \text{in} (0,1)\times \mathbb{R}^n$$
