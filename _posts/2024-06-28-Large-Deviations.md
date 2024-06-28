---
layout: post
categories: Stochastics
---

# Large Deviations- An introduction
Reference: Rezakhanlou 2017 Lectures on LDP

## What is Large Deviation?

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
$$\lim_{n\to\infty} n^{-1} \log \mathbb{P}(S_n = \[nx])= - I(x)$$ for $x\in\[0,1\]$.
It is consistent with CLT:
$$nI(p+y/\sqrt{n}) = \frac12 I''(p)y^2 + O(n^{-\frac{1}{2}})$$
$$\mathbb{P}(S_n-\[nx]) \approx \frac{1}{\sqrt{2\pi p(1-p)}} e^{-\frac{1}{2} I''(p) y^2}$$.

Example: Wiener measure

The $d$-dimensional Brownian measure can be regarded as $\mathbb{P}$ on $\Omega= C([0,T];\mathbb{R}^d)$ of $x:[0,T]\to \mathbb{R}^d$ such that for $t_0=0<t_1<...<t_{k-1}<t_k = T$ and $y_0=0$,
$$\mathbb{P}(x(t_1) \in \mathrm{d} y_1 ,..., x(t_k) \in \mathbb{d} y_k ) = Z^{-1}_{t_1,...,t_k} \exp(-\frac{1}{2} \sum_{i=1}^k \frac{|y_i-y_{i-1}|^2}{t_i - t_{i-1}}) \mathrm{d}y_1... \mathrm{d} y_k$$


How to interpret large deviation results?
The rate function $I$ is interpreted as the difference between an energy function and some kind of entropy.

The energy fuction relates to the probability of such a microstates via $\exp(-n H(x))$.
The entropy relates to the counting of the microstates (set of possible combinations of $X_i$) correspond to the macrostate $S_n = \[nx\]$ via 
$$\binom{n}{\[nx]}\approx \exp(n J(x) ).$$ Here we also see the 'competition' between energy and entropy to compute $\mathbb{P}(S_n= \[nx\])$.

Another interpretation is the relative entropy of the law of $X$ with respect to the uniform distribution.

## Defintions of LDP, transformations of LDP

Defintion rate function $I:E \to [0,\infty]$
1. I has compact sublevel set
2. for every open set $U$
$$ \liminf_{n\to\infty} n^{-1} \log \mathbb{P}_n(U) \ge -\inf_{x\in U} I(x),$$
3. for every closed set $C$
$$ \limsup_{n\to\infty} n^{-1} \log \mathbb{P}_n (C) \le -\inf_{x\in C} I(x).$$

Or understand as $\lim_n n^{-1} \log \mathbb{P}_n(A) = -\inf_{A} I$.

Alternative for 2,3
For every continuous bounded function $F:E \to \mathbb{R}$
$$\Lambda(F):= \lim_{n\to\infty} n^{-1} \log \int e^{n F} \mathrm{d} P_n = \sup_{E}(F-I).$$
and 
$$I(x) = \sup_{F \in C_b(E)} (F(x) - \Lambda(F)).$$

1. Contraction principle $\Phi : E \to E'$ continuous function, then the family ${P_n'}$ defined by
$$\mathbb{P}_n'(A) := \mathbb{P}_n (\Phi^{-1}(A))$$ satisfies an LDP with rate function 
$I'(x')= \inf\{ I(x) : \Phi(x) = x'\}.$

2. If $G:E\to\mathbb{R}$ is a bounded continuous function, then the family
$$\mathrm{d} \mathbb{P}_n^G := \frac{1}{Z_n(G)} e^{nG} \mathrm{d}\mathbb{P}_n$$ with $Z_n(G)$ normalization
satisfies an LDP with rate function $I^G(x) = I(x) - G(x) + \sup_E (G-I)$

Cramer's theorem

Assume $\int e^{x \cdot v} \mu (\mathrm{d} x)<+\infty$, for every $v\in\mathbb{R}^d$. Then $\{\mathbb{P}_n\}$ defined via $\mathbb{P}_n(A)= \mathbb{P}( n^{-1}(X_1+...+X_n) \in A)$ satisfies LDP with 
$$I(x) = \lambda^* (x) = \sup_{v\in \mathbb{R}^d} (x \cdot v - \lambda(v)),$$ where $\lambda(v)= \log \int e^{x \cdot v} \mu(\mathrm{d} x).$

Sanov's theorem 
$\mu$ probability measure on a Polish space $E$ and assume $X_1,...,X_2$ a sequence of $E$-values iid random variable with law $\mu$. Consider $M$
 space of Radon probability measures on $E$ with Wasserstein distance $D$. The family of probability measures $P_n$ on $M$ by
 $$\mathbb{P}_n (A) = \mathbb{P}( n^{-1} (\delta_{X_1} + ...+\delta_{X_n}) \in A )$$ 
 
for every Borel set $A \subset M$. 

The family $\{P_n\}$, law of mean of iid rv, satisfies  LDP with a rate function $I(\nu) = H(\nu\vert \mu).$

Theorem 
$$H(\mu|\nu)=\sup_{f \in C_b(E)}( \int f \mathrm{d} \nu - \lambda (f) )= \sup_{f \in B_b(E)} ( \int f \mathrm{d} \nu -\lambda(f))$$

How is it applied?
How does it help to show the absolute continuity of measure with respect to Lebesgue measure under a specific dynamics?
