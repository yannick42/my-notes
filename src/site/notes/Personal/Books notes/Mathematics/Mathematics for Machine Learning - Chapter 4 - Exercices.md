---
{"dg-publish":true,"dg-permalink":"Chapter 4 - Matrix Decomposition - Exercices","permalink":"/Chapter 4 - Matrix Decomposition - Exercices/"}
---


↑ [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 4 - Matrix Decompositions|Chapter 4 - Matrix Decompositions]]
<-- [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 3 - Exercices|Chapter 3 - Exercices]] - **TODO** -->

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

First we calculate the eigenvalues :
$p_A(\lambda) = det(A-\lambda I) = det(\begin{bmatrix} -\lambda & -1 & 1 & 1  \newline  -1 & 1-\lambda & -2 & 3  \newline  2 & -1 & -\lambda & 0  \newline  1 & -1 & 1 & -\lambda \end{bmatrix})$

With **Laplace expansion**, we get :
$\lambda\cdot\begin{vmatrix}1-\lambda & -2 & 3  \newline  -1 & -\lambda & 0  \newline  -1 & 1 & -\lambda\end{vmatrix} - \begin{vmatrix}-1 & -2 & 3  \newline  2 & -\lambda & 0  \newline  1 & 1 & -\lambda\end{vmatrix} - \begin{vmatrix}-1 & 1-\lambda & 3  \newline  2 & -1 & 0  \newline  1 & -1 & -\lambda\end{vmatrix} + \begin{vmatrix}-1 & 1-\lambda & 2  \newline  2 & -1 & -\lambda  \newline  1 & -1 & 1 \end{vmatrix}=$
$(-\lambda^4+\lambda^3-3\lambda) - (-\lambda^2 - \lambda + 6) - (-\lambda^2 + \lambda - 3) + (-\lambda^2+4\lambda+1) =$

==TO FINISH...==

---
#### Exercice 4.5
> Diagonalizability of a matrix is unrelated to its invertibility. Determine for the following four matrices whether they are diagonalizable and/or invertible
> $\begin{bmatrix}1&0 \newline 0&1\end{bmatrix}, \begin{bmatrix}1&0 \newline 0&0\end{bmatrix}, \begin{bmatrix}1&1 \newline 0&1\end{bmatrix}, \begin{bmatrix}0&1 \newline 0&0\end{bmatrix}$

To be diagonalizable, the eigenvectors of a matrix must form a basis :

**a)** $det(A-\lambda I)=0$ -> $det(\begin{bmatrix}-\lambda&0 \newline 0&-\lambda\end{bmatrix})=0$ so $\lambda^2=0$ -> it true only if it's equal to 0, ... how many eigenvector ?!
- If $det(A)=0$, A is **not invertible**

**b)** $det(\begin{bmatrix}1-\lambda&0 \newline 0&-\lambda\end{bmatrix})=0$ -> $-\lambda(1-\lambda)=0$ -> roots are 0 and 1
eigenvector $E_{\lambda_0}$ : $\begin{bmatrix}1&0 \newline 0&0\end{bmatrix}x=0$
eigenvector $E_{\lambda_1}$ : $\begin{bmatrix}0&0 \newline 0&-1\end{bmatrix}x=0$
=> ==TODO==

**c)** ==TODO==

**d)** ==TODO==

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
> Are the following matrices diagonlizable ? If yes, determine their diagonal form and a basis with respect to which the transformation matrices are diagonal. If no, give reasons why they are not diagonalizable.
> 
> **a)**
> $$A=\begin{bmatrix}0&1 \newline -8&4\end{bmatrix}$$
> **b)**
> $$A=\begin{bmatrix}1&1&1 \newline 1&1&1 \newline 1&1&1\end{bmatrix}$$
> **c)**
> $$A:=\begin{bmatrix}5&4&2&1 \newline 0&1&-1&-1 \newline -1&-1&3&0 \newline 1&1&-1&2\end{bmatrix}$$
> **d)**
> $$A=\begin{bmatrix}5&-6&-6 \newline -1&4&2 \newline 3&-6&-4\end{bmatrix}$$

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
