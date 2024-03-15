---
layout: post
categories: OT@Berlin
---

## Approximation via Langevin dynamics

Taiji Suzuki: Convergence of mean field Langevin dynamics and its application to neural network feature learning

Consider $\min_{\mu\in P} L(\mu), L(\mu):= F(\mu)+ \lambda_2 \operatorname{Ent}(\mu)$, where $F$ is convex, $\operatorname{Ent}=\int \log (\mu) \d \mu$.

The idea is to use mean field Langevin dynamics to minimise $L$.


Gradient Langevin dynamics $d X_t = -\nabla L(X_t) \mathrm{d} t + \sqrt{2 \lambda} \mathrm{d} B_t$ where $L(X)= \frac{1}{n} \sum_{i=1}^n l_i(X) + R(X)$ is non-convex.

The discrete approximation via Eule-Meruyama scheme is 
$X_{k+1}=X_k - \eta \nabla L(X_k) + \sqrt{2 \eta}\lambfa \xi_k $ where $xi_k \sim N(0,I)$.

GLD as Wasserstein gradient flow
![From paper](https://github.com/solomon-lam/solomon-lam.github.io/assets/43318214/b3f0b527-c89f-4e30-add2-aa1efe890c51)

Approximate Mean-field Langevin dynamics by discrete finite particle system in discrete time.

Assuming $log$-Sobolev inequality, he can show convergence of the approximation of the loss function.
 
![image](https://github.com/solomon-lam/solomon-lam.github.io/assets/43318214/861ce79e-afb1-475f-8afe-acb97246dba1)




Reference: [Convergence of mean-field Langevin dynamics: Time and space discretization, stochastic gradient, and variance reduction](https://arxiv.org/abs/2306.07221)
