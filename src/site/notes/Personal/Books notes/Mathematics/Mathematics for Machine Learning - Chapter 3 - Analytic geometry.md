---
{"dg-publish":true,"dg-permalink":"Chapter 3 - Analytic geometry","permalink":"/Chapter 3 - Analytic geometry/"}
---

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
- a particular **type of** inner product : $x^\intercal y=\sum_{i=1}^{n}x_i y_i$

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
- Orthogonal matrice : $A^{-1}=A^\intercal$
- 

---
#### 3.5 **Orthonormal basis**
- ==Gram-Schmidt process== : put a B (a non orthonormal and unnormalized **basis vectors**) in this augmented form : [BB^T|B] to a row reduced form through Gaussian elimination -> get a orthonormal basis ?

---
#### 3.6 **Orthogonal Complement**
- a subspace $U^\perp$ that contains all vectors orthogonal to every vector in U
- $U \cap U^\perp=\{0\}$

---
#### 3.7 **Inner product of functions** (a few lines about it...)
- real & functional analysis : Hilbert space, ...
- Fourier series

---
#### 3.8 **Orthogonal projection**
- *Definition 3.10* (Projection) : a linear mapping is called a projection if $\pi^2=\pi\circ\pi=\pi$
- $\pi_U(x) = \lambda b$ (a multiple of the basis vector)
- $<x-\lambda b, b>=0$ (exploit the bilinearity of the inner product)-> $<x,b>-\lambda<b,b>=0$
- $\lambda=\frac{b^\intercal x}{b^\intercal b}$
	- if $\lVert b \rVert =1$ -> $\lambda=b^\intercal x$
- projection matrix : $P_{\pi}=\frac{bb^\intercal}{\lVert b\rVert^2}$
	- symmetric matrix of rank 1


##### 3.8.3 - ==Gram-Schmidt orthogonalization==
- Projections are at the core of this constructive method
- the basis (ONB) always exists

---
#### 3.9 **Rotations**
- It perform a basis change ...
- automorphism
- **3.9.1** - Rotations in R^2
	- $R(\theta)=\begin{bmatrix}\cos\theta&-\sin\theta\\\sin\theta&\cos\theta\end{bmatrix}$
- **3.9.2** - in R^3
- **3.9.3** - in n dimensions
	- `Givens rotation` -> $R_{ij}(\theta)$ : each time the identity matrix, except on 4 entries
- **3.9.4** - Properties of rotations
	- preserve distances & angles
	- in 3 or more dimension, it's generally not commutative (even if they rotate about the same point)

---
#### 3.10 **Further readings**
- Axler (2015) -> [[___INBOX___/__à trier/Linear Algebra Done Right (Axler, 2015)|Linear Algebra Done Right (Axler, 2015)]]
- Boyd & Vandenberghe (2018) -> [[___INBOX___/__à trier/Introduction to Applied Linear Algebra (book, 2018)|Introduction to Applied Linear Algebra (book, 2018)]]

---
### See also
- [[Topics/Machine Learning/Books/Mathematics for Machine Learning (2020)|Mathematics for Machine Learning (2020)]]

---
### Exercices
-> [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 3 - Exercices|Mathematics for Machine Learning - Chapter 3 - Exercices]]
