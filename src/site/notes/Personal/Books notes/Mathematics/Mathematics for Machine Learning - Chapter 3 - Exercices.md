---
{"dg-publish":true,"dg-permalink":"Chapter 3 - Analytic Geometry - Exercices","permalink":"/Chapter 3 - Analytic Geometry - Exercices/"}
---

↑ [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 3 - Analytic geometry|Chapter 3 - Analytic geometry]]
<-- [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 2 - Exercices|Chapter 2 - Exercices]] - [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 4 - Exercices|Chapter 4 - Exercices]] -->

---
#### Exercice 3.1
> Show that $\langle.,.\rangle$ defined for all $x=[x1, x2]^\intercal \in \mathbb{R}^2$ and $y=[y1, y2]^\intercal \in \mathbb{R}^2$ by $\langle x,y\rangle := x_1y_1 - (x_1y_2 + x_2y_1) + 2(x_2y_2)$ is an **inner product**

- => To be an inner product, it must be **a positive definite, symmetric bilinear mapping**
	- To be a **bilinear mapping**, it must be linear with both arguments
		- $\langle \lambda x + \psi y,z \rangle = (\lambda x_1 + \psi y_1)z_1 - [(\lambda x_1 + \psi y_1)z_2 + (\lambda x_2 + \psi y_2)z_1] + 2(\lambda x_2 + \psi y_2)z_2 =...= \lambda\langle x,z \rangle + \psi\langle y,z \rangle$
		- $\langle x, \lambda y + \psi z \rangle = \textcolor{green}{x_1\lambda y_1} + \textcolor{red}{\psi z_1 x_1} - (\textcolor{green}{x_1 \lambda y_2} + \textcolor{red}{x_1 \psi z_2} + \textcolor{green}{x_2\lambda y_1} + \textcolor{red}{x_2\psi z_1}) + \textcolor{green}{2x_2\lambda y_2} + \textcolor{red}{2x_2\psi y_2} = \textcolor{green}{\lambda\langle x,y \rangle} + \textcolor{red}{\psi\langle x,z \rangle}$
	- **Is it symmetric ?** => so the order of the arguments doesn't matter => $\langle x,y \rangle=\langle y,x \rangle$ ?
	we get $\langle y,x \rangle=y_1x_1 - (y_1x_2 + y_2x_1) + 2(y_2x_2)$, ==which is the same as $\langle x,y \rangle$== after some rearrangements
	- **Positive definite ?** -> so $\forall x \in V\setminus\{0\} : \Omega(x,x)>0$ and $\Omega(0,0)=0$ ?
	this last condition is true after calculation. And we must also check weither : $\langle x,x \rangle=x_1^2 - 2x_1x_2 + 2x_2^2 \overset{?}{>} 0$
	-> we can factorize and get $(x_1-x_2)^2+x_2^2$ which is always positive because of the squares, and is 0 only when both $x$ are 0	

---
#### Exercice 3.2
> Consider $\mathbb{R}^2$ with $\langle .,. \rangle$ defined for all $x$ and $y$ in $\mathbb{R}^2$ as $\langle x,y \rangle := x^\intercal \begin{bmatrix} 2 & 0 \\ 1 & 2 \end{bmatrix}y$. Is $\langle .,. \rangle$ an **inner product** ?

We see that the matrix is **==not symmetric==** (...positive definite), and if we continue and try to calculate $\langle x,y \rangle$ and $\langle y,x \rangle$ then we get : $2x_1y_1 + \textcolor{red}{x_2y_1} + x_2y_2 \neq 2x_1y_1 + \textcolor{red}{x_1y_2} + x_2y_2$

---
#### Exercice 3.3
> Compute the distance between
> $x=\begin{bmatrix}1\\2\\3\end{bmatrix}$, $y=\begin{bmatrix}-1 \newline -1 \newline 0\end{bmatrix}$
> using
> **a)** $\langle x,y \rangle :=x^\intercal y$
> **b)** $\langle x,y \rangle :=x^\intercal A y$, $A:=\begin{bmatrix}2&1&0 \newline 1&3&-1 \newline 0&-1&2\end{bmatrix}$

The definition of a distance between two vector is $d(x,y):=\lVert x-y \rVert =\sqrt{\langle x-y, x-y \rangle}$
- **a)** with the dot product as the inner product -> Euclidean distance : 
we have $x - y = \begin{bmatrix}2 \newline 3 \newline 3\end{bmatrix}$ => $d(x,y) = \sqrt{2^2+3^2+3^2} = \sqrt{22}$
- **b)** with an inner product defined by A (which is symmetric and positive definite (?))
 $d(x,y)=\sqrt{\begin{bmatrix}2&3&3\end{bmatrix}A\begin{bmatrix}2 \newline 3 \newline 3\end{bmatrix}}=\sqrt{47}$

---
#### Exercice 3.4
> Compute the angle between
> $x=\begin{bmatrix}1 \newline 2\end{bmatrix}$, $y=\begin{bmatrix}-1 \newline -1\end{bmatrix}$
> using
> **a)** $\langle x,y \rangle :=x^\intercal y$
> **b)** $\langle x,y \rangle :=x^\intercal B y$, $B:=\begin{bmatrix}2&1 \newline 1&3\end{bmatrix}$

$\cos \omega=\frac{\langle x,y \rangle}{\sqrt{\langle x,x \rangle \langle y,y \rangle}}=\frac{x^\intercal y}{\sqrt{x^\intercal x y^\intercal y}}$
- **a)** we get
$\cos \omega=-\frac{3}{\sqrt{5\times 2}}$ -> $\omega=\arccos(\cos\omega)\approx \colorbox{orange}{161.56°}$
- **b)** we get these products (with matrix $B$)
$\langle x,y \rangle=-11$
$\langle x,x \rangle=18$
$\langle y,y \rangle=7$
=> $\cos\omega=-\frac{11}{\sqrt{18\times 7}}\rightarrow \omega\approx \colorbox{orange}{168.5°}$


---
#### Exercice 3.5
> Consider the Euclidean vector space $\mathbb{R}^5$ with the dot product. A subspace $U \subseteq \mathbb{R}^5$ and $x \in \mathbb{R}^5$ are given by
> $U = span[\begin{bmatrix}0 \newline -1 \newline 2 \newline 0 \newline 2\end{bmatrix}, \begin{bmatrix}1 \newline -3 \newline 1 \newline -1 \newline 2\end{bmatrix}, \begin{bmatrix}-3 \newline 4 \newline 1 \newline 2 \newline 1\end{bmatrix}, \begin{bmatrix}-1 \newline -3 \newline 5 \newline 0 \newline 7\end{bmatrix}],  x=\begin{bmatrix}-1 \newline -9 \newline -1 \newline 4 \newline 1\end{bmatrix}$
> **a)** Determine the orthogonal projection $\pi_U(x)$ of $x$ onto $U$
> **b)** Determine the distance $d(x, U)$

**a)** $\pi_U(x)$ must be an element of $U$, and be represented by $\pi_U(x)=\sum\limits_{i=1}^{m}\lambda_i b_i$.
As in the 1D-case (-> see *chap. 3.8.1*), we must follow the 3 step procedure to find $\pi_U(x)$ (and also the projection matrix $P_\pi$ as a bonus...)

$\pi_U(x)=\sum\limits_{i=1}^{m}\lambda_i b_i = B\lambda$ *(3.57)* with $B=[b_1,...,b_m] \in \mathbb{R}^{n\times m}$ (n=5, m=4)
- **Step 1**, with the formula : $\lambda=(B^\intercal B)^{-1}B^\intercal x$ after computation we get
$$\lambda=\begin{bmatrix}-4 \newline 2 \newline 0 \newline 1\end{bmatrix}$$
- **Step 2**, $\pi_U(x)=B\lambda$
$$\pi_U(x)=\begin{bmatrix}1 \newline -5 \newline -1 \newline -2 \newline 3\end{bmatrix}$$

- **Step 3** ==optional==, $P_\pi x=B(B^\intercal B)^{-1}B^\intercal x$, with the shape of $P_\pi$ equals (5x4) ((4x5)(5x4)) (4x5) => **(5x5)**
$P_\pi=$ (with Python/numpy)
![Pasted image 20220313071930.png](data:image/png;base64,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)

**b)** to determine the distance (simple dot product) between $x$ and the subspace $U$, aka. `projection error` between the original and its projection :
$\lVert x - \pi_U(x)\rVert$ = $\lVert \begin{bmatrix}-2&-4&0&6&-2\end{bmatrix}^\intercal \rVert = \sqrt{60}\approx \colorbox{orange}{7,74}$


---
#### Exercice 3.6
> Consider $\mathbb{R}^3$ with the inner product
> $\langle x,y \rangle :=x^\intercal A:=\begin{bmatrix}2&1&0 \newline 1&2&-1 \newline 0&-1&2\end{bmatrix} y$
> Furthermore, we define $e_1,e_2,e_3$ as the standard/canonical basis in $\mathbb{R}^3$
> **a)** Determine the orthogonal projection $\pi_U(x)$ of $e_2$ onto
> $$U = span[e_1,e_3]$$
> Hint: Orthogonality is defined through the inner product
> **b)** Compute the distance $d(e_2, U)$
> **c)** Draw the scenario: standard basis vectors and $\pi_U(x)$

(*remark* : $A$ is positive definite if $x^\intercal Ax > 0$ -> ==see if it's the case==)
If it was the simple dot product, $e_2$ would just project onto point $(0,0)$... in $U = span[\begin{bmatrix}1 \newline 0 \newline 0\end{bmatrix},\begin{bmatrix}0 \newline 0 \newline 1\end{bmatrix}]$, but the orthogonality is defined through (/depends on) the inner product (which use the $A$ symmetric positive definite matrix, above). So to determine the orthogonal projection $\pi_U(x)$ of $e_2$, it must be orthogonal to all basis vectors of $U$.

=> Can we cannot simple use the formula $\pi_U(x) = B\lambda =B(B^\intercal B)^{−1}B^\intercal x$ but with the inner product (matrix A) ... as it was using the dot product.
With $\lambda$, the (only 2) coordinates in the basis of $U$ and $x=e_2=\begin{bmatrix}0 \newline 1 \newline 0\end{bmatrix}$, $B=\begin{bmatrix}1&0 \newline 0&0 \newline 0&1\end{bmatrix}$
$\langle e_2, e_1 \rangle = \langle e_2, e_3 \rangle = 0$ if all are orthonormal, but it's not the case with this inner product, eg.
$\langle e_2, e1 \rangle = \begin{bmatrix}0&1&0\end{bmatrix} \begin{bmatrix}2&1&0 \newline 1&2&-1 \newline 0&-1&2\end{bmatrix} \begin{bmatrix}1 \newline 0 \newline 0\end{bmatrix} = 1$

> (dead end ?)
> We have $\langle e_1, e_2 - \pi_U(x) \rangle = \langle e_3, e_2 - \pi_U(x) \rangle=0$ where $\pi_U(x)$
> -> $\sqrt{\begin{bmatrix}1&0&0\end{bmatrix}\cdot \begin{bmatrix}2&1&0 \newline 1&2&-1 \newline 0&-1&2\end{bmatrix} \cdot (e_2 - \pi_U(x)) }$

$\pi_U(x)=B\lambda$ and from the definitions with inner products we can get : $B^\intercal A (x - B\lambda)=0$ => $\lambda=\frac{B^\intercal A}{B^\intercal A B}x=(B^\intercal A B)^{-1}B^\intercal A x=P_\pi x$
$(B^\intercal A B)^{-1}=\begin{bmatrix}1/2&0 \newline 0&1/2 \end{bmatrix}$
$\pi_U(e_2)=P_\pi e_2=\begin{bmatrix}1 & 1/2 & 0 \newline 0&-1/2&1 \end{bmatrix} \begin{bmatrix}0 \newline 1 \newline 0\end{bmatrix}=\begin{bmatrix}1/2 \newline -1/2 \end{bmatrix}=\lambda=\begin{bmatrix}\lambda_1 \newline \lambda_3 \end{bmatrix}$
$$\pi_U(x)=\begin{bmatrix}1/2 \newline 0 \newline -1/2\end{bmatrix}$$

**b)** Compute the distance :
> *"In vector spaces with general inner products, we have to pay attention when computing angles and distances, which are defined by means of the inner product."* **(p. 88)**

The distance $d(e_2,U)$ is simply $\lVert e_2 - \pi_U(e_2) \rVert = \sqrt{\begin{bmatrix}-1/2 & 1 & 1/2\end{bmatrix} \begin{bmatrix}2&1&0 \newline 1&2&-1 \newline 0&-1&2\end{bmatrix} \begin{bmatrix}-1/2 \newline 1 \newline 1/2\end{bmatrix}}=1$

**c)** ==DRAW==

---
#### Exercice 3.7
> Let $V$ be a vector space and $\pi$ an endormorphism of $V$.
> **a)** Prove that $\pi$ is a projection if and only if $id_V-\pi$ is a projection, where $id_V$ is the identity endomorphism on $V$.
> **b)** Assume now that $\pi$ is a projection. Calculate $Im(id_V-\pi)$ and $ker(id_V-\pi)$ as a function of $Im(\pi)$ and $ker(\pi)$.

==TODO==

An endormorphism $\Phi:V\rightarrow V$ linear


---
#### Exercice 3.8
> Using the **Gram-Schmidt method**, turn the basis $B=(b_1,b_2)$ of a two dimensional subspace $U \subseteq\mathbb{R}^3$ into an **ONB** $C=(c_1,c_2)$ of $U$, where
> $b_1:=\begin{bmatrix}1 \newline 1 \newline 1\end{bmatrix}$, $b_2:=\begin{bmatrix}-1 \newline 2 \newline 0\end{bmatrix}$

The Gram-Schmidt method, tell us that :
$c_1=b_1$ and $c_2=b_k - \pi_{span[c_1]}(b2)$
$\pi_{span[c_1]}(b2)=\frac{BB^\intercal}{B^\intercal B} b_2$ where $B=[c_1]$

$c1=\begin{bmatrix}1 \newline 1 \newline 1\end{bmatrix}$
$c_2 = \begin{bmatrix}-1 \newline 2 \newline 0\end{bmatrix} - \frac{1}{3}\begin{bmatrix}1&1&1 \newline 1&1&1 \newline 1&1&1 \end{bmatrix} \begin{bmatrix}-1 \newline 2 \newline 0\end{bmatrix} = \begin{bmatrix}-1 \newline 2 \newline 0\end{bmatrix} - \begin{bmatrix}1/3 \newline 1/3 \newline 1/3 \end{bmatrix}=\begin{bmatrix}-4/3 \newline 5/3 \newline -1/3\end{bmatrix}$
After normalization :
$c1=\begin{bmatrix}1/\sqrt{3} \newline 1/\sqrt{3} \newline 1/\sqrt{3}\end{bmatrix}$
$c_2=\frac{3}{\sqrt{42}}\begin{bmatrix}-4/3 \newline 5/3 \newline -1/3\end{bmatrix}$

---
#### Exercice 3.9
> Let $n\in\mathbb{N}$ and let $x_1,...,x_n>0$ be $n$ positive real numbers so that $x_1+...+x_n=1$. Use the Cauchy-Schwarz inequality and show that
> **a)** $\sum_{i=1}^{n}x_i^2 \geq\frac{1}{n}$
> **b)** $\sum_{i=1}^{n}\frac{1}{x_i} \geq n^2$
> Hint: Think about the dot product on $\mathbb{R}^n$. Then, choose specific vectors $x, y \in \mathbb{R}^n$ and apply the Cauchy-Schwarz inequality.

--> The Cauchy-Schwarz inequality states that : $|\langle x,y \rangle|\leq \lVert x \rVert \lVert y \rVert$

==TODO==

---
#### Exercice 3.10
> Rotate the vectors
> $x_1:=\begin{bmatrix}2 \newline 3\end{bmatrix},x_2:=\begin{bmatrix}0 \newline -1\end{bmatrix}$
> by **30°**

to rotate by $\theta$ = 30° (->$\frac{\pi}{6}$ radians) ==counterclockwise== (by convention as the angle is positive), (in 2D?) we can multiply $X$ containing the column vectors $[x_1,x_2]$ by the rotation matrix $R(\theta)=\begin{bmatrix}\cos\theta&-\sin\theta \newline \sin\theta&\cos\theta\end{bmatrix}$
-> $R(\theta)X = XR(\theta) = \begin{bmatrix}2\cos\theta-3\sin\theta&\sin\theta \newline 2\sin\theta+3\cos\theta&-\cos\theta\end{bmatrix} = \begin{bmatrix}\frac{2\sqrt{3}-3}{2}&\frac{1}{2} \newline \frac{2+3\sqrt{3}}{2}&-\frac{\sqrt{3}}{2}\end{bmatrix}$
We get in each columns the rotated vectors $x_1^\prime = \frac{1}{2}\begin{bmatrix}2\sqrt{3}-3 \newline 2+3\sqrt{3}\end{bmatrix}$ and $x_2^\prime = \frac{1}{2} \begin{bmatrix}1 \newline -\sqrt{3}\end{bmatrix}$
- [ ] Make a grid with colored vector + angle, ...etc in Python -> put code in here + image of the result #todo 
- [ ] XR = RX in 2-d only
