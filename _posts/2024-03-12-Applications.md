---
layout: post
categories: OT@Berlin
---

## Optimal transport in quantum many-particle system
Today one interesting talk (Sparse Approximation of Multi-marginal Quantum Optimal Transport Problems with Moment Constraints: Application to Quantum Chemistry) by Virginie Ehrlacher is about application of optimal transport in understanding the quantum many body Schrodinger problem. By reducing the variational problem into a optimal transport problem. Many notions from quantum many body particles appear e.g. Born-Oppenheimer approximation, density functional theory, Hohenberg-Kohn functional, Lieb functional. The connection to optimal transport is due to the fact that in many-body particle system, all particles are identical so the single particle marginals are the same. This allows us to relate the evolution of system to optimal transport. It involves quantum optimal transport when the operator are not communtative. 

The talk of Mark Petletier "Singular-limit Analysis of Training with Noise Injection" adds randomness into the gradient flow problem to understand stochastic gradient descent. The question to answer is find parameters $w$ so that given model function $f(x_i,w)$ approximate the ground truth $g(x_i)$ well, the parameters $w$ determined by finite observations in an optimisation problem gives a good approximation for all observation in the domain. It was called noisy gradient decent. By adding randomness, the gradient flow moves along the zero sets of the functional instead of standing still at the first hit point of the zero set.

There are applications in so-called Bernoulli dropout, Gaussian dropout in machine learning and possibly in adversarial training as raised during quesitons. But I could not find the relevant paper on arXiv. 
