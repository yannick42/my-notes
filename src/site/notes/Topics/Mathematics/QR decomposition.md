---
{"dg-publish":true,"dg-permalink":"QR","permalink":"/QR/","dgHomeLink":true,"dgPassFrontmatter":false}
---


**QR decomposition**
> $A=QR$
> **A** must be a *square matrix*
> **Q** is a *orthogonal matrix* -> $Q^\intercal Q=I$
> **R** is a *upper triangular matrix*
- it's a method in [[Topics/Mathematics/Linear Algebra|Linear Algebra]], aka. QR factorization
- the resulting decomposition is not unique => several methods will produce different results
- **Methods**
	- ==**Gram-Schmidt**== (**1907**? but already known before...!)
		- see History & applications -> https://www.researchgate.net/publication/264259023_Gram-Schmidt_orthogonalization_100_years_and_more
	- **Householder method** (**1958**)
	- **Givens method**
		- 50% more "expensive" than Householder QR
- <u>Extensions</u> : RQ, QL, LQ


---
### Applications
- calcul de solutions de systèmes linéaires **non carrés**
	- notamment pour determiner la **pseudo-inverse** d'une matrice -> celle-ci [[Topics/Mathematics/Moore-Penrose inverse|Pseudoinverse]] ?
	- sans avoir à calculer $A^{-1}$
- Computation of the solutions to the [[___INBOX___/__à trier/Least-squares method|least-squares]] problems
	- https://johnwlambert.github.io/least-squares/ #DIIGO
- in **telecommunication**, as a preprocessing step for MiMo antenna systems (wifi, 4G, …)


---
### Householder's method
> An other unrelated method as this name is used in **numerical analysis** (with [[Topics/Mathematics/Calculus/Newton’s method|Newton’s method]])

- introduced in **1958**
-> https://www.youtube.com/watch?v=gvnFVCWI044&ab_channel=NathanKutz
- with a series of successive Householder transformations (reflections) $P=I-2vv^H$ which introduces subdiagonal zeros
	- symmetric and 
- Householder reflector $F$
- http://mlwiki.org/index.php/Householder_Transformation
- https://en.wikipedia.org/wiki/Householder_transformation

---
### See also
- [[Topics/Mathematics/Cholesky decomposition (1902)|Cholesky decomposition (1902)]]
- [[Topics/Mathematics/LU decomposition (1938)|LU decomposition (1938)]]
- [[Topics/Mathematics/Eigendecomposition|Eigendecomposition]]


---
[Décomposition QR (wikipedia)](https://fr.wikipedia.org/wiki/D%C3%A9composition_QR)
[QR decomposition (wikipedia)](https://en.wikipedia.org/wiki/QR_decomposition)
