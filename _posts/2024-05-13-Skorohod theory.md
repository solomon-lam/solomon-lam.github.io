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
  $`d^{\circ}(x,y)=\inf_{\lambda\in\Lambda}\{\|\lambda\|^{\circ}_{\infty} \vee \| x- y\lambda\|_{\infty} \}`$,
$`\|\lambda\|^{\circ}=\sup_{s<t}|\log \frac{\lambda t-\lambda s}{t-s}|`$

# Skorohod topology $[0,\infty)$ 
Definition
Properties
Compactness
Finite dimensional sets
Weak convergence
Tightness criterion
