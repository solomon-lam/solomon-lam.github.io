---
layout: post
categories: Stochastics
---

## Skorohod topology

# Skorohod space on $[0,1]$
* cadlag functions $x: [0,1] \to \mathbb{R}$
* Define
$T\subset [0,1]$,
$w_x(T): = \sup_{s,t \in T} |x(s)-x(t)|$
* Modulus of continuity $w_x(\delta)= \sup_{0\le t \le t 1-\delta}w_x([t,t+\delta])$

# Properities of cadlag functions
Consider cadlag modulus
$w_x'(\delta)= \inf_{\{t_i\}} \max_{1\le i \le v}w_x([t_{i-1},t_i))$
The infimum over all $\delta$-sparese sets $\{t_i\}$, ie. $\min_{1\le i \le v} (t_i -t_{i-1}) > \delta$.
* characterisation: $\lim_{\delta \to 0}w_x'(\delta)=0$ this implies:
* at most countably many discontinuities
* $x$ is bounded
* $x$ can be uniformly approximated by simple functions constant over intervals



# Skorohod toplogy finite time
Class of strictly increasing, continuous mappings from $[0,1]$ onto itself: $\Lambda$. In particular, $\lambda(0)=0, \lambda(1)=1$.
Metric on $D$, $$d(x,y)= \inf_{\lambda \in \Lambda} \{ \|\lambda -I \|_{\infty[0,1]} \vee \| x - y\lambda\|_{\infty [0,1]} \}$$
* Convergence in Skorohod topology iff $\lim_n x_n(\lambda_n t)= x(t)$ uniformly in $t$ and $\lim_n \lambda_n t =t$ uniformly in $t$.
* Uniform convergence implies Skorohod convergence
* Skorohod convergence implies $x_n(t) \to x(t)$ for all $t$ continuity point of $x$.
*  If $x$ is continuous on $[0,1]$, then Skorohod convergence implies uniform convergence.
*  However, $D$ is not complete under $d$. It is under
  $$d^{\circ}(x,y)=\inf_{\lambda\in\Lambda} \{ \| \lambda {\|^{\circ}}_{\infty} \vee \| x- y\lambda\|_{\infty} \}$$,
$$\|\lambda\|^{\circ}=\sup_{s<t}|\log \frac{\lambda t-\lambda s}{t-s} |$$
* $D$ is separable and complete.
* Compactness: Theorem 12.3 analogue of Arzela-Asocli theorem, Theorem 12.4 via
  $${w}^{''}_x(\delta)=\sup_{t_1 \le t \le t_2, t_2 -t_1 \le \delta} \{|x(t)-x(t_1)| \wedge |x(t_2)-x(t)|\}$$
  (Billingsley) 
* Finite dimensional sets

# Weak convergence and tightness in $D$
Compare with the continuous function version Theorem 7.3 via Arzeal-Ascoli.


# Skorohod topology $[0,\infty)$ 
$D[0,\infty)$ cadlag functions on $[0,\infty)$. 
Introduce $D_t$ cadlag functions on $[0,t]$, 
$d_t^{\circ}(x,y)$ which is analogous to $d^{\circ}$ but for functions on $[0,t]$.

Define 
$$g_m(t)=\begin{cases} 1 \quad &\text{if } t\le m-1,\\
                        m-t \quad &\text{if } m-1\le t \le m,\\
                        0 \quad &\text{if } t \ge m.$$
For $x\in D_\infty$, $x^m\in D_\infty$, $x^m(t)=g_m(t)x(t), t\ge 0.$
$$d^{\circ}_\infty(x,y)= \sum_{m=1}^{\infty} 2^{-m} (1 \wedge d_m^{\circ}(x^m, y^m))
Convergence in $d_\infty^{\circ}(x_n,x) \to 0$ in $D_{\infty}$ iff there exists $\lambda_n \in \Gamma_\infty$,
$\sup_{t<\infty}|\lambda_n t -t| \to 0$ and for each $m$ 
$\sup_{t\le m}|x_n(\lambda_n t)- x(t)|\to 0$.

Properties
Compactness
Finite dimensional sets
Weak convergence
Tightness criterion
