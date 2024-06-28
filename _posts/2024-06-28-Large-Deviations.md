---
layout: post
categories: Stochastics
---

# Large Deviations- An introduction
Reference: Rezakhanlou 2017 Lectures on LDP

What is Large Deviation?

Motivation: 
Gibbs measure
$$\nu_\beta(x)=\frac{1}{Z_\beta}e^{-\beta H(x)}=e^{-\beta H(x)-\log Z_\beta} =: e^{-\beta I(x)}$$
where $\beta>0$, $E$ finite state space, $H:E\to\mathbb{R}$ the energy function.
LDP: means probability measures close to the Gibbs measure with $\beta \to \infty$ as the size of $E \to \infty$.

Example: Bernoulli trial
$S_n = X_1 + ... + X_n$ where $X_i$ is the value of the $i$ th trial with outcomes either $0$ or $1$. $X_i$ is $p$-Bernoulli random variable.
By Stirling formula,
$P(S_n = \[nx\]) = \exp(-n I(x)+ O(\log n))$ where $I(x)=x\log \frac{x}{p} + (1-x)\log\frac{1-x}{1-p}$

How to interpret large deviation results?
What is rate function?
How is it applied?
How does it help to show the absolute continuity of measure with respect to Lebesgue measure under a specific dynamics?
