---
{"dg-publish":true,"dg-permalink":"mml/chap4/ex","permalink":"/mml/chap4/ex/"}
---

↑ [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 4 - Matrix Decompositions|Chapter 4 - Matrix Decompositions]]
<-- [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 3 - Exercices|Chapter 3 - Exercices]] - [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 5 - Exercices|Chapter 5 - Exercices]] -->

---
### Exercices
#### Exercice 4.1
> Compute the determinant using the **Laplace expansion** (using the first row) and the **Sarrus rule** for
> $$A=\begin{bmatrix}1&3&5 \newline 2&4&6 \newline 0&2&4\end{bmatrix}$$

- with ==**Laplace expansion**== for a n by n matrix (along rows $j$, first 1 only...) :
-> see *Example 4.3*
apply the formula : $det(A)=\sum\limits_{k=1}^{n}(-1)^{k+j} a_{jk} det(A_{j,k})$
$det(A)=(-1)^{1+1}\cdot 1 \cdot \begin{vmatrix} 4 & 6  \newline  2 & 4 \end{vmatrix} + (-1)^{1+2}\cdot 3 \cdot \begin{vmatrix} 2 & 6  \newline  0 & 4 \end{vmatrix} + (-1)^{1+3}\cdot 5 \cdot \begin{vmatrix} 2 & 4  \newline  0 & 2 \end{vmatrix}$
$det(A) = 4-24+20 = \colorbox{orange}{0}$
- with ==**Sarrus' rule**== (only for a matrix 3 by 3)
$det(A)=a_{11}a_{22}a_{33}+a_{21}a_{32}a_{13}+a_{31}a_{12}a_{23}-a_{31}a_{22}a_{13}-a_{11}a_{32}a_{23}-a_{21}a_{12}a_{33}$
$det(A)=16+20+0-0-12-24=\colorbox{orange}{0}$

=> ==A is a singular matrix== (not invertible)

#### Exercice 4.2
 > Compute the following determinant efficiently
 > $$\begin{vmatrix}2&0&1&2&0 \newline 2&-1&0&1&1 \newline 0&1&2&1&2 \newline -2&0&2&-1&2 \newline 2&0&0&1&1\end{vmatrix}$$

We can bring A to **row echelon form** (I did it without row exchange so no changes in the sign of the determinant...), and then by only multiplying the elements on the diagonal, we get the **determinant**

$T=REF(A)=\begin{vmatrix}2&0&1&2&0 \newline 0&-1&-1&-1&1 \newline 0&0&1&0&3 \newline 0&0&0&1&-7 \newline 0&0&0&0&-3\end{vmatrix}$ ($T$ is upper triangular)

$det(T)=\prod\limits_{i=1}^{n}T_{ii}$
$det(T) = 2\times -1\times 1\times 1\times -3 = \colorbox{orange}{6}$

---
#### Exercice 4.3
> Compute the eigenspaces of
> **a)** $A:=\begin{bmatrix}1&0 \newline 1&1\end{bmatrix}$
> **b)** $B:=\begin{bmatrix}-2&2 \newline 2&1\end{bmatrix}$

**a)** To find the eigenspaces we need the eigenvalues, we know that :
$p_A(\lambda) = det(A-\lambda I) = det(\begin{bmatrix} 1-\lambda & 0  \newline  1 & 1-\lambda \end{bmatrix})=(1-\lambda)^2$
=> **1 root** : $\lambda=1$ with algebraic multiplicity of $2$

We find the eigenvectors that corresponds to these eigenvalues (here, only 1 root/eigenvalue) by looking at vectors $x$ such that :
$\begin{bmatrix} 1-\lambda & 0  \newline  1 & 1-\lambda \end{bmatrix}x=0$ => for $\lambda=1$ => $\begin{bmatrix} 0 & 0  \newline  1 & 0 \end{bmatrix}x=0$

We solve $x$ and get $x_1=0$ (which spans a vertical line through origin ??)

**b)** Similarly,
$p_B(\lambda) = det(B-\lambda I) = det(\begin{bmatrix} -2-\lambda & 2  \newline  2 & 1-\lambda \end{bmatrix})=\lambda^2+\lambda-6=0$

We get **2 roots** : $\lambda=2$ and $\lambda=-3$

Eigenvector of $\lambda=2$ : $\begin{bmatrix}-4 & 2  \newline  2 & -1 \end{bmatrix}x=0$
-> $E_2=span(\begin{bmatrix}1 \newline 2\end{bmatrix})$

Eigenvector of $\lambda=-3$ : $\begin{bmatrix}1 & 2  \newline  2 & 4 \end{bmatrix}x=0$
-> $E_{-3}=span(\begin{bmatrix}2 \newline -1\end{bmatrix})$

---
#### Exercice 4.4
> Compute all eigenspaces of 
> $A:=\begin{bmatrix}0&-1&1&1 \newline -1&1&-2&3 \newline 2&-1&0&0 \newline 1&-1&1&0\end{bmatrix}$

First we calculate the **eigenvalues** with the ==characteristic polynomial== :
$p_A(\lambda) = det(A-\lambda I) = det(\begin{bmatrix} -\lambda & -1 & 1 & 1  \newline  -1 & 1-\lambda & -2 & 3  \newline  2 & -1 & -\lambda & 0  \newline  1 & -1 & 1 & -\lambda \end{bmatrix})$

With **Laplace expansion**, we get :
$\lambda\cdot\begin{vmatrix}1-\lambda & -2 & 3  \newline  -1 & -\lambda & 0  \newline  -1 & 1 & -\lambda\end{vmatrix} - \begin{vmatrix}-1 & -2 & 3  \newline  2 & -\lambda & 0  \newline  1 & 1 & -\lambda\end{vmatrix} - \begin{vmatrix}-1 & 1-\lambda & 3  \newline  2 & -1 & 0  \newline  1 & -1 & -\lambda\end{vmatrix} + \begin{vmatrix}-1 & 1-\lambda & 2  \newline  2 & -1 & -\lambda  \newline  1 & -1 & 1 \end{vmatrix}=$
$(-\lambda^4+\lambda^3-3\lambda) - (-\lambda^2 - \lambda + 6) - (-\lambda^2 + \lambda - 3) + (-\lambda^2+4\lambda+1) =$
==TO FINISH...==

Then for each eigenvalue, we find corresponding eigenvector(s)
==TODO==

$Eig(A)=span(\begin{bmatrix} ? \newline ? \newline ? \newline ? \end{bmatrix}, \begin{bmatrix} ? \newline ? \newline ? \newline ? \end{bmatrix}, \begin{bmatrix} ? \newline ? \newline ? \newline ? \end{bmatrix}, \begin{bmatrix} ? \newline ? \newline ? \newline ? \end{bmatrix})$

---
#### Exercice 4.5
> Diagonalizability of a matrix is unrelated to its invertibility. Determine for the following four matrices whether they are diagonalizable and/or invertible
> $\begin{bmatrix}1&0 \newline 0&1\end{bmatrix}, \begin{bmatrix}1&0 \newline 0&0\end{bmatrix}, \begin{bmatrix}1&1 \newline 0&1\end{bmatrix}, \begin{bmatrix}0&1 \newline 0&0\end{bmatrix}$

To be diagonalizable, the eigenvectors of a matrix must form a basis :
**a)** $A=\begin{bmatrix}1&0 \newline 0&1\end{bmatrix}$ (already diagonalized...), it is **invertible** $A=A^{-1}$
$p(\lambda)=det(A-\lambda I)=0$ -> $det(\begin{bmatrix}1-\lambda&0 \newline 0&1-\lambda\end{bmatrix})=0$ so $(1-\lambda)^2=0$ -> it's true only if $\lambda=1$ is the only eigenvalue : algebraic multiplicity = 2.
=> how many eigenvector ?
- To find the eigenspace (collection of the eigenvectors) associated with each eigenvalues, we solve for $x$ in $(A-\lambda I)x$
=> $Ax=\begin{bmatrix} 0&0 \newline 0&0 \end{bmatrix} x=0$ => there is infinitely many solution --> if we chose $x_1=1$ we can choose any $x_2$, so let's take $x_2=0$ => one eigenvector is $\begin{bmatrix}1 \newline 0 \end{bmatrix}$, as a second one we can take on orthogonal one $\begin{bmatrix}0 \newline 1 \end{bmatrix}$ so that they both are linearly independent and form a basis
so it **diagonalizable** => $Eig(A)=span(\begin{bmatrix}1 \newline 0\end{bmatrix}, \begin{bmatrix}0 \newline 1\end{bmatrix})$

**b)** $A=\begin{bmatrix}1&0 \newline 0&0\end{bmatrix}$ is **not invertible** as its determinant is $0$
$det(\begin{bmatrix}1-\lambda&0 \newline 0&-\lambda\end{bmatrix})=0$ -> $-\lambda(1-\lambda)=0$ -> roots are $\lambda_0=$ **0** and $\lambda_1=$ **1**
eigenvector $E_{\lambda_0}$ : $\begin{bmatrix}1&0 \newline 0&0\end{bmatrix}x=0$ -> we can take any $x_2$, let's take $1$, $x_1$ must be $0$ -> $\begin{bmatrix}0 \newline 1 \end{bmatrix}$
eigenvector $E_{\lambda_1}$ : $\begin{bmatrix}0&0 \newline 0&-1\end{bmatrix}x=0$ -> we can take any $x_1$, let's take $1$, $x_2$ must be $0$ -> $\begin{bmatrix}1 \newline 0 \end{bmatrix}$
=> both for a basis, to $A$ is **diagonalizable**

**c)** $A=\begin{bmatrix}1&1 \newline 0&1\end{bmatrix}$ is **invertible** as its determinant is different from $0$
$det(\begin{bmatrix} 1-\lambda & 1 \newline 0& 1-\lambda\end{bmatrix})=0$ => $(1-\lambda)^2$
=> ==TODO==

**d)** $det(\begin{bmatrix} -\lambda & 1 \newline 0& -\lambda\end{bmatrix})=0$ => $\lambda^2=0$
=> ==TODO==

---
#### Exercice 4.6
> Compute the eigenspaces of the following transformation matrices. Are they diagonalizable ?
> **a)** For
> $$A=\begin{bmatrix}2&3&0 \newline 1&4&3 \newline 0&0&1\end{bmatrix}$$
> **b)** For
> $$A:=\begin{bmatrix}1&1&0&0 \newline 0&0&0&0 \newline 0&0&0&0 \newline 0&0&0&0\end{bmatrix}$$

**a)** 

**b)** A is not invertible but ...

==TODO==

#### Exercice 4.7
> Are the following matrices diagonalizable ? If yes, determine their diagonal form and a basis with respect to which the transformation matrices are diagonal. If no, give reasons why they are not diagonalizable.
> 
> **a)**
> $$A=\begin{bmatrix}0&1 \newline -8&4\end{bmatrix}$$
> **b)**
> $$A=\begin{bmatrix}1&1&1 \newline 1&1&1 \newline 1&1&1\end{bmatrix}$$
> **c)**
> $$A:=\begin{bmatrix}5&4&2&1 \newline 0&1&-1&-1 \newline -1&-1&3&0 \newline 1&1&-1&2\end{bmatrix}$$
> **d)**
> $$A=\begin{bmatrix}5&-6&-6 \newline -1&4&2 \newline 3&-6&-4\end{bmatrix}$$

**a)**
for $A$ to be diagonalizable its eigenvectors must form a basis
- we must **find the eigenvectors** of $A$ with :
	- $det(A-\lambda I)=det(\begin{bmatrix} -\lambda & 1 \newline -8 & 4-\lambda \end{bmatrix})=0$
	- -> $-\lambda (4-\lambda)+8=\lambda^2-4\lambda +8=0$
	- so the roots are : $\lambda_1=2-2i$ and $\lambda_2=2+2i$
- Then the eigenvectors for each eigenvalues are :
	- $(A-\lambda I)x=0$ -> by **Gaussian elimination** to bring it to reduced form (by multiplying with complex conjugates to get real numbers at times...)
		- with $\lambda_1$ :
			- $\begin{bmatrix} -2+2i & 1 \newline -8 & 2-2i \end{bmatrix} x=0$
			- so after calculation we get $x_2=1$ and $x_1=\frac{1}{4}+\frac{1}{4}i$ => $x=\begin{bmatrix}x_1 \newline x_2 \end{bmatrix}=E_{\lambda_1}=\begin{bmatrix} \frac{1}{4}+\frac{1}{4}i \newline 1 \end{bmatrix}$
		- with $\lambda_2$ :
			- $\begin{bmatrix} -2-2i & 1 \newline -8 & 2+2i \end{bmatrix} x=0$
			- so with the same procedure : $E_{\lambda_2}=\begin{bmatrix} \frac{1}{4}-\frac{1}{4}i \newline 1 \end{bmatrix}$
**These column vectors must form a basis** (they span the eigenspace of $A$) : with $P=\begin{bmatrix} \frac{1}{4}+\frac{1}{4}i  & \frac{1}{4}-\frac{1}{4}i \newline 1 & 1 \end{bmatrix}$
=> so they ==must be **linearly independent==** -> I checked we can put it in row (reduced) echelon form, I also checked that $P^\intercal P=I$ (??)
and the eigenvectors should be used to form the diagonal of $D=\begin{bmatrix} 2-2i & 0 \newline 0 & 2+2i \end{bmatrix}$
(remember that in eigendecomposition $A=PDP^{-1}$, and $A$ & $D$ are *==similar matrices==*)

**b)**
$A$ is **symmetric** so it must be diagonalizable with ==real eigenvalues== (-> see Spectral Theorem - 4.15) (even if it's **not invertible** as its determinant is 0)
$det(A-\lambda I)=det(\begin{bmatrix}1-\lambda&1&1 \newline 1&1-\lambda&1 \newline 1&1&1-\lambda\end{bmatrix})=0$
With the **Sarrus' rule** : $(1-\lambda)^3+2-3(1-\lambda)=0$ after some calculation : $\lambda\lambda(-\lambda+3)=0$ so $\lambda_1=0$, $\lambda_2=0$ and $\lambda_3=3$
($\lambda=0$ has an **algebraic multiplicity of 2**)
- With $\lambda_1$ :
$(A-\lambda_1 I)x=0=\begin{bmatrix} 1 & 1 & 1 \newline 1 & 1 & 1 \newline 1 & 1 & 1 \end{bmatrix} x$ we get $x_1+x_2+x_3=0$ which has infinitely many solutions ...
-> on a plane ?
we set $x_3=0$ and $x_2=1$ => $x_1=-1$
$E_{\lambda_1}=\begin{bmatrix} -1 \newline 1 \newline 0 \end{bmatrix}$
Now if we set $x_3=1$ and $x_2=0$ => $x_1=-1$
$E_{\lambda_2}=\begin{bmatrix} -1 \newline 0 \newline 1 \end{bmatrix}$
- With $\lambda_3=3$ :
$\begin{bmatrix} -2 & 1 & 1 \newline 1 & -2 & 1 \newline 1 & 1 & -2 \end{bmatrix} x = 0$ => the 3rd column is free -> if we set $x_3=1$ => $E_{\lambda_3}=\begin{bmatrix} 1 \newline 1 \newline 1 \end{bmatrix}$
-> infinitely many solutions on a line ?
$P=\begin{bmatrix} -1 & -1 & 1 \newline 1 & 0 & 1 \newline 0 & 1 & 1 \end{bmatrix}$ -> $P^{-1}=\begin{bmatrix} -1/3 & 2/3 & -1/3 \newline -1/3 & -1/3 & 2/3 \newline 1/3 & 1/3 & 1/3 \end{bmatrix}$
$D=\begin{bmatrix} 0 & 0 & 0 \newline 0 & 0 & 0 \newline 0 & 0 & 3 \end{bmatrix}$
When can check that : $A=PDP^{-1}=\begin{bmatrix} -1 & -1 & 1 \newline 1 & 0 & 1 \newline 0 & 1 & 1 \end{bmatrix}\begin{bmatrix} 0 & 0 & 0 \newline 0 & 0 & 0 \newline 0 & 0 & 3 \end{bmatrix}\begin{bmatrix} -1/3 & 2/3 & -1/3 \newline -1/3 & -1/3 & 2/3 \newline 1/3 & 1/3 & 1/3 \end{bmatrix}=\begin{bmatrix} 1 & 1 & 1 \newline 1 & 1 & 1 \newline 1 & 1 & 1 \end{bmatrix}$

**c)**
==TODO==

**d)**
==TODO==


---
---

#### Exercice 4.8
> Find the SVD of the matrix
> $$A=\begin{bmatrix}3&2&2 \newline 2&3&-2\end{bmatrix}$$

==TODO==

#### Exercice 4.9
> Find the singular value decomposition of
> $$A=\begin{bmatrix}2&2 \newline -1&1\end{bmatrix}$$

==TODO==

#### Exercice 4.10
> Find the rank-1 approximation of
> $$A=\begin{bmatrix}3&2&2 \newline 2&3&-2\end{bmatrix}$$

==TODO==

#### Exercice 4.11
> Show that for any $A \in \mathbb{R}^{m\times n}$ the matrices $A^\intercal A$ and $AA^\intercal$ possess the same nonzero eigenvalues.

==TODO==

#### Exercice 4.12
> Show that for $x\neq 0$ Theorem 4.24 holds, i.e., show that
> $$\max\limits_{x}\frac{\lVert Ax \rVert_2}{\lVert x \rVert_2}=\sigma_1$$
> where $\sigma_1$ is the largest singular value of $A \in \mathbb{R}^{m\times n}$.

==TODO==
