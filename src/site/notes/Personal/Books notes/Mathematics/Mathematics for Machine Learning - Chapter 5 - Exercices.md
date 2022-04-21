---
{"dg-publish":true,"dg-permalink":"mml/chap5/ex","permalink":"/mml/chap5/ex/","dgHomeLink":true,"dgPassFrontmatter":false}
---


↑ [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 5 - Vector Calculus|Chapter 5 - Vector Calculus]]
<-- [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 4 - Exercices|Chapter 4 - Exercices]] - **TODO** -->

---
### Exercice 5.1
> Compute the derivative $f^\prime(x)$ for
> $$f(x)=\log(x^4)\sin(x^3)$$

We must use the **product rule** ($(fg)^\prime=f^\prime g+fg^\prime$) and the **chain rule** ($(g(f))^\prime=g(f)^\prime f^\prime$)

so $f^\prime (x)=(\log(x^4))^\prime sin(x^3)+\log(x^4)(\sin(x^3))^\prime$
we put $v=log(u), u=x^4$ so with the **chain rule** : $(\log(x^4))^\prime=\frac{4}{x}$ (derivative of $log(x)$ is $\frac{1}{x}$)
same thing for derivative of $\sin(x^3)$ we get $3\cos(x^3)x^2$
==so the result is : $4\frac{\sin(x^3)}{x}+3\log(x^4)\cos(x^3)x^2$== (checked on Wolfram Alpha)


### Exercice 5.2
> Compute the derivative $f^\prime(x)$ of the logistic sigmoid
> $$f(x)=\frac{1}{1+\exp(-x)}$$

-> **Quotien rule** $(\frac{f}{g})^\prime=\frac{f^\prime g+fg^\prime}{g^2}$

After calculation, we get $\frac{\exp(-x)}{(1+\exp(-x))^2}$ (checked on Wolfram Alpha)


### Exercice 5.3
> Compute the derivative $f^\prime (x)$ of the function
> $$f(x)=\exp(-\frac{1}{2\sigma^2}(x-\mu)^2)$$
> where $\mu, \sigma \in \mathbb{R}$ are constants.

We must use the **chain rule**

and get $f^\prime (x)=-\frac{x-\mu}{\sigma^2}f(x)$


### Exercice 5.4
> Compute the Taylor polynomials $T_n, n=0,...,5$ of $f(x)=\sin(x)+\cos(x)$ at $x_0=0$.

The formula is $T_n(x):=\sum\limits_{k=0}^n \frac{f^{(k)}(x_0)}{k!}(x-x_0)^k$ at $x_0=0$ it becomes :
$T_n(x):=\sum\limits_{k=0}^n \frac{f^{(k)}(0)}{k!}(x)^k$
- Compute the k-derivatives $f^k(0)$ at each step :
	- $f^0(0)=1$
	- $f^\prime(0)=\cos(0)-\sin(0)=1$
	- $f^{\prime\prime}(0)=-\sin(0)-\cos(0)=-1$
	- $f^{\prime\prime\prime}(0)=-\cos(0)+\sin(0)=-1$
	- $f^4(0)=\sin(0)+\cos(0)=1$ (same as step 0)
	- $f^5(0)=1$

with **n = 0** : $T_0(x):=\sum\limits_{k=0}^0 \frac{f^0(0)}{k!}x^k=1$
with **n = 1** : $T_1(x):=\sum\limits_{k=0}^1 \frac{f^k(0)}{k!}x^k=1+x$
with **n = 2** : $T_2(x):=\sum\limits_{k=0}^2 \frac{f^k(0)}{k!}x^k=1+x-\frac{1}{2}x^2$
with **n = 3** : $T_3(x):=\sum\limits_{k=0}^3 \frac{f^k(0)}{k!}x^k=1+x-\frac{1}{2}x^2-\frac{1}{6}x^3$
with **n = 4** : $T_4(x):=\sum\limits_{k=0}^4 \frac{f^k(0)}{k!}x^k=1+x-\frac{1}{2}x^2-\frac{1}{6}x^3+\frac{1}{24}x^4$
with **n = 5** : $T_3(x):=\sum\limits_{k=0}^3 \frac{f^k(0)}{k!}x^k=1+x-\frac{1}{2}x^2-\frac{1}{6}x^3+\frac{1}{24}x^4+\frac{1}{120}x^5$


### Exercice 5.5
> Consider the following functions :
> $$f_1(x)=\sin(x_1)\cos(x_2), x\in\mathbb{R}^2$$
> $$f_2(x, y)=x^\intercal y, x,y \in\mathbb{R}^n$$
> $$f_2(x)=xx^\intercal, x\in\mathbb{R}^n$$
> **a)** What are the dimension of $\frac{\partial f_i}{\partial x}$ ?
> **b)** Compute the Jacobians.

**a)**
$f_1$ has dimension 1 x 2
$f_2$ has dimension 2 x 1 ?
$f_3$ has dimension 1 x 1 ??

**b)**
$J_1=\begin{bmatrix} \frac{\partial f}{\partial x_1} & \frac{\partial f}{\partial x_2} \end{bmatrix}=\begin{bmatrix} \cos(x_1)\cos(x_2) & -\sin(x_2)\sin(x_1) \end{bmatrix}$

$J_12\begin{bmatrix} \frac{\partial f}{\partial x} \newline \frac{\partial f}{\partial y} \end{bmatrix}=\begin{bmatrix} ? \newline ? \end{bmatrix}$
==TODO==

$J_3=\begin{bmatrix} \frac{\partial f}{\partial x} \end{bmatrix}=\begin{bmatrix} ? \end{bmatrix}$
==TODO==


### Exercice 5.6
> Differentiate $f$ with respect to $t$ and $g$ with respect to $X$, where
> $f(t)=\sin(\log(t^\intercal t)), t\in\mathbb{R}^D$
> $g(X)=tr(AXB), A\in\mathbb{R}^{D\times E}, X\in \mathbb{R}^{E\times F}, B\in \mathbb{R}^{F\times D}$
> where $tr(.)$ denotes the trace.

==TODO==


### Exercice 5.7
==TODO==


### Exercice 5.8
==TODO==


### Exercice 5.9
==TODO==

