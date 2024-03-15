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



Wuchen Li: Information Gamma Calculus: Convexity Analysis for Stochastic Differential Equations
Problem: Sample target measure $\pi(x) = \frac{1}{Z} e^{-V(x)}$ given $V: \Omega \to \mathbb{R}$. But $V$ is only partially known.
$\dotX(t)=b(X_t)+\sqrt{2}a(X_t) B_t$ assume invariant measure $\pi$ exists. 
Question: convergence to invariant measure.

Lypunavo method: calculate second derivative of KL divergence, entropy dissipation analysis for non-gradient and degenerate stochastic dynamics system.

Lafferty 1988

Mi Jung Park:Privacy-preserving Data Generation in the Era of Foundation Models: Generative Transfer Learning with Differential Privacy


Synthetic data is vulnerable to linkage attacks which connects to a original datapoint. 
Differential privacy: learn as much as possible about a group while learning as little as possible about individuals.
Fine tuning models using DP method to avoid model remembering data. e.g. Type in a name recover the origin portrait of a woman.
Method: Kernel mean embedding
Application: (Latent) Diffusion model, attention modules, Image generation: 
Future: Tabular data
Connection between robustness and DP?
