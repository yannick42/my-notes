---
{"dg-publish":true,"permalink":"/topics/mathematics/cholesky-decomposition-1902/"}
---

> **Cholesky decomposition**, aka. "**factorisation** de Cholesky"

$A=LL^T$

- -> it transforms a matrix $A$ to a **lower matrix** multiplied by its transpose
- L est donc une sorte de "racine carré" de A
- Il faut que la matrice A soit **==symétrique== définie positive**

### Application/Examples
- https://math.stackexchange.com/questions/1944373/what-is-the-cholesky-decomposition-used-for
- permet de ==calculer la matrice inverse $A^{-1}$==
	- $A^{-1}=(LL^\intercal)^{-1}=L^{-\intercal}L^{-1}$
	- => https://scicomp.stackexchange.com/questions/30885/computing-the-inverse-of-a-matrix-using-the-cholesky-decomposition
- permet de ==calculer le determinant de A== very efficiently
	- $det(A)=det(L)det(L^T)=det(L)^2$
- to solve a [[___INBOX___/__à trier/Systems of Linear Equations|Systems of Linear Equations]] $Ax=b$ (in a faster way?), with $A=LL^*$ then solve for y in $Ly=b$ by ==forward substitution==, then solve for x in $L^*x=y$ by ==back substitution==
	- roughly twice as efficient as [[Topics/Mathematics/LU decomposition (1938)|LU decomposition (1938)]] (when applicable)
	- arise quite often in applications (positive, from physical considerations), numerical solution of [[Topics/Mathematics/PDE|PDE]]
- **Example** : the covariance matrix of a variable multivariate-Gaussian (is symmetric and positive definite)
- used in [[Topics/Machine Learning/Techniques/Ridge regression|Ridge regression]] (sklearn : solver="cholesky")
- Linear regression ?
- Monte-Carlo simulation ?
- Utilisé en chimie quantique pour accélérer les calculs ?
- méthode centrale en **analyse numérique**

> ***What is the Cholesky decomposition used for ?***
> --> https://math.stackexchange.com/questions/1944373/what-is-the-cholesky-decomposition-used-for
> - **Normal equations** for least squares problems.
> - Discretizations of self adjoint partial differential equation **boundary value problems**.
> - **Hessians of convex functions** (in many cases the Hessian is made to be convex) in optimization.
> - Systems of equations arising from the ==primal-dual barrier method== for **linear programming**.

### History
- méthode probablement découverte en **1902**
- **André-Louis Cholesky** : officier et ingénieur français
- posthumously published in **1924**, after he died in WW1
	- found as he was a map maker in late 19th century

### Coding
- in [[___INBOX___/__à trier/Numpy|Numpy]] -> routine `numpy.linalg.cholesky`
	- https://numpy.org/doc/stable/reference/generated/numpy.linalg.cholesky.html

### See also
- [[Topics/Mathematics/QR decomposition|QR decomposition]]
- [[Topics/Mathematics/LU decomposition (1938)|LU decomposition (1938)]]
- [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 4 - Matrix Decompositions|Mathematics for Machine Learning - Chapter 4 - Matrix Decompositions#4 3 - Cholesky Decomposition p 114]]

### References
- [Why is computing ridge regression with a Cholesky decomposition much quicker than using SVD?](https://stats.stackexchange.com/questions/396914/why-is-computing-ridge-regression-with-a-cholesky-decomposition-much-quicker-tha)
- https://towardsdatascience.com/behind-the-models-cholesky-decomposition-b61ef17a65fb

---
https://en.wikipedia.org/wiki/Cholesky_decomposition
