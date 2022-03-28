---
{"dg-publish":true,"dg-permalink":"Chapter 3 - Analytic geometry","permalink":"/Chapter 3 - Analytic geometry/"}
---

↑[[Topics/Published notes/MML (home)|Mathematics for Machine Learning (home)]]
<-- [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 2 - Linear Algebra|Chapter 2 - Linear Algebra]] - [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 4 - Matrix Decompositions|Chapter 4 - Matrix Decompositions]] -->


**Goals**
- to have a geometric intuition/interpretation of [[Topics/Mathematics/Linear Algebra|Linear algebra]]
- equip [[___INBOX___/__à trier/Vector spaces|Vector spaces]] with an inner product which induce a geometry
- notions of : similarity / distances / angles ...

---
### Topics
#### 3.1 **Norms**
- it's a function $\lVert...\rVert : V\rightarrow R$, with the following "properties"
	- *absolutely homogeneous* (function?) : $\lVert \lambda x \rVert= |\lambda| \lVert x \rVert$
	- *triangle inequality*
	- *positive definite* -> ?
- Euclidean norm = $l_2$ norm
- Manhattan norm = $l_1$ norm

#### 3.2 **Inner products**
> purposes / goals
> - allow the introduction of **length** of a vector, **angle** or **distance** between two vectors
> - to find if two vectors are **orthogonal**

##### 3.2.1 - Dot product
- a particular(ly simple) **type of** inner product : $x^\intercal y=\sum_{i=1}^{n}x_i y_i$

##### 3.2.2 - General inner products
- **bilinear** : linear in each arguments
- a positive definite, symmetric `bilinear mapping` -> inner product on V
- (V,<.,.>) -> *inner product space*

##### 3.2.3 - Symmetric positive definite matrices (p. 73)
- key in the definition of Kernels (Section 12.4)
- defined by inner product
- if must satisfy : $\forall x \in V\setminus\{0\}: x^\intercal Ax\gt 0$

```ad-info
title:
#### What's the formula for the `dot product` ? #card

$x^\intercal y=\sum_{i=1}^{n}x_i y_i$

---
#### What's a SPD matrix ? #card

Symmetric positive definite (or just positive definite) means that the matrix satisfies : $\forall x \in V\setminus\{0\}: x^\intercal Ax\gt 0$
*Remark: if $\geq 0$ it's called semidefinite*

---
```

---
#### 3.3 **Lengths and distances**
- dot product -> euclidean distance
- a metric is a mapping **d** from $V\times V \rightarrow \mathbb{R}$
- ==Very similar x and y will result in a **large value for the inner product** and a **small value for the metric**.==

```ad-info
title:
#### Very similar vectors $x$ and $y$ will result in a small value for the inner product and a large value for the metric ? #card

False, it's the opposite

---
```

---
#### 3.4 **Angles and orthogonality**
- Orthogonal matrix : its columns are orthonormal $AA^\intercal=I=A^\intercal A$ -> $A^{-1}=A^\intercal$
	- the inverse is obtained by transposing the matrix
- Orthogonal matrix do rotations (-> see *Section 3.9*)

---
#### 3.5 **Orthonormal basis**
- ==Gram-Schmidt process== (Strang, 2003) : put a B (a non orthonormal and unnormalized **basis vectors**) in this augmented form : [BB^T|B] to a row reduced form through Gaussian elimination -> get a orthonormal basis ?

---
#### 3.6 **Orthogonal Complement**
- **Important** role in Chapter 10 on linear dimensionality reduction
- a subspace $U^\perp$ that contains all vectors orthogonal to every vector in U
- $U \cap U^\perp=\{0\}$
- generally used to describe hyperplanes (?)

---
#### 3.7 **Inner product of functions** (a few lines about it...)
- real & functional analysis : Hilbert space, ...
- Fourier series

---
#### 3.8 **Orthogonal projection**
- An **important** class of linear transformations (besides: rotations & reflections)
	- in Graphics, Coding theory, [[Topics/Mathematics/Statistics and probabilities/Statistics|statistics]] and Machine Learning
- *Definition 3.10* (Projection) : a linear mapping is called a projection if $\pi^2=\pi\circ\pi=\pi$
- projection matrix $P_\pi^2=P_\pi$

##### 3.8.1 - Projection onto One-Dimensional Subspaces (Lines)
- 
- $\pi_U(x) = \lambda b$ so the coordinate $\lambda$ it is a multiple of the basis vector, and is an element of $U$ ...
- $<x-\lambda b, b>=0$ (exploit the bilinearity of the inner product)-> $<x,b>-\lambda<b,b>=0$
- $\lambda=\frac{\langle x, b \rangle}{\langle b, b \rangle}=\frac{b^\intercal x}{b^\intercal b}$
	- if basis is "normal" $\lVert b \rVert =1$ -> simply $\lambda=b^\intercal x$
- $\pi_U(x) = P_\pi x$
	- projection matrix (are always symmetrix) : $P_{\pi}=\frac{bb^\intercal}{\lVert b\rVert^2}$
		- here it is symmetric matrix of rank 1 ...
	- Remark : we can show that $\pi_U(x)$ is an eigenvector of $P_\pi$ with an eigenvalue = 1
		- => ==TODO==

##### 3.8.2 - Projection onto General Subspaces
- 
- Info : we can find approximate solutions to unsolvable linear equations using projections
- If basis is ONB it simplifies the equations (no longer have to compute the inverse)

##### 3.8.3 - ==Gram-Schmidt orthogonalization==
- Projections are at the core of this constructive method
- the basis (ONB) always exists
- see Liesen & Mehrmann (2015)
- $u_1:=b_1$
- $u_k:=b_k-\pi_{span[u_1, ..., u_{k-1}]}(b_k), \quad k=2,...,n$

##### 3.8.4 - Projection onto Affine subspaces
- affine space $L=x_0+U$
- 

---
#### 3.9 **Rotations**
- It perform a basis change ...
- automorphism
- **3.9.1** - Rotations in R^2
	- $R(\theta)=\begin{bmatrix}\cos\theta&-\sin\theta \newline \sin\theta&\cos\theta\end{bmatrix}$
- **3.9.2** - in R^3
- **3.9.3** - in n dimensions
	- `Givens rotation` -> $R_{ij}(\theta)$ : each time the identity matrix, except on 4 entries
- **3.9.4** - Properties of rotations
	- preserve distances & angles
	- in 3 or more dimension, it's generally not commutative (even if they rotate about the same point)

---
#### 3.10 **Further readings**
- broader and more in-depth :
	- Axler (2015) -> [[___INBOX___/__à trier/Linear Algebra Done Right (Axler, 2015)|Linear Algebra Done Right (Axler, 2015)]]
	- Boyd & Vandenberghe (2018) -> [[___INBOX___/__à trier/Introduction to Applied Linear Algebra (book, 2018)|Introduction to Applied Linear Algebra (book, 2018)]]
- Orthogonal bases (Gram-Schmidt)
	- important in **optimization** and **numerical algorithms** for solving SLE (Krylov subspaces methods : conjugate gradient, GMRES, minimize residual errors that are orthogonal to each other) -> Stoer & Burlirsch (2002)
- inner product
	- in **ML**, important in ==Kernel method== (Schölkopf & Smola (2002)) which exploit the fact that many linear algorithm can be expressed as purely inner product computations => ??. Implicitly computed with the "Kernel trick" in a potentially infinite-dimensional feature space.
		- Kernel-PCA (Schölkopf, 1997) for dimensionality reduction
		- Gaussian processes (Rasmussen & Williams, 2006) in probabilitistic regression
	- --> see **Chapter 12**
- Projections
	- in **computer graphics** to generate shadows
	- in **Optimization** : orthogonal projections to (iteratively) minimize residual errors
	- Bishop (2006) -> [[Topics/Machine Learning/Books/Pattern Recognition and Machine Learning (2006)|Pattern Recognition and Machine Learning (2006)]]
	- Linear regression
	- PCA

---
### See also
- [[Topics/Machine Learning/Books/Mathematics for Machine Learning (2020)|Mathematics for Machine Learning (2020)]]

---
### Exercices
-> [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 3 - Exercices|Mathematics for Machine Learning - Chapter 3 - Exercices]]
