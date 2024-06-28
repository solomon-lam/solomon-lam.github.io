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
The function $I$ is convex, $I\ge 0$ and attains $0$ at $x=p$ which is consistent with $n^{-1} S_n \to p$ as $n\to +\infty$. It satisfies 
$$\lim_{n\to\infty} n^{-1} \log \mathbb{P}(S_n = \[nx\])= - I(x)$$ for $x\in\[0,1\]$.
It is consistent with CLT:
$$nI(p+y/\sqrt{n}) = \frac12 I''(p)y^2 + O(n^{-\frac{1}{2}})$$
$$\mathbb{P}(S_n-\[nx\]) \approx \frac{1}{\sqrt{2\pi p(1-p)}} e^{-\frac{1}{2} I''(p) y^2}$$.

How to interpret large deviation results?
The rate function $I$ is interpreted as the difference between an energy function and some kind of entropy.

The energy fuction relates to the probability of such a microstates via $\exp(-n H(x))$.
The entropy relates to the counting of the microstates (set of possible combinations of $X_i$) correspond to the macrostate $S_n = \[nx\]$ via 
$$\binom{n}{\[nx\]}\approx \exp(n J(x) )$$. Here we also see the 'competition' between energy and entropy to compute $\mathbb{P}(S_n \[nx\])$.

What is rate function?
How is it applied?
How does it help to show the absolute continuity of measure with respect to Lebesgue measure under a specific dynamics?
