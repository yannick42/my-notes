---
{"dg-publish":true,"permalink":"/topics/mathematics/singular-value-decomposition/"}
---

<!--
Note créée le 15 novembre 2013, vide ...
-->

---
### Intro
- **SVD** : Singular Value Decomposition (-> fr : Décomposition en valeurs singulière)
- In [[Topics/Mathematics/Linear Algebra|Linear Algebra]], it is a factorization of a matrix into $A=U\Sigma V^*$
	- it **generalizes eigendecomposition** (fr : décomposition en valeurs propres $A=XD^{-1}X$) (for square normal matrices) => if A is square and diagonalizable
- **U** : m x m, unitary
- **V** : n x n, unitary
- $\Sigma$ : m x n, diagonal with real positive coefficients
- versions : **réduite** et **complète** : selon si on calcule un Û ou U (en ajoutant des colonnes à Û)
	- reduced / full SVD

---
### Courses / MOOCs / Taught at
- [[___INBOX___/__à trier/INSA|INSA#Lyon - Parcours Bioinformatique et modélisation BiM]] - **3ème année** : cours - **Algèbre linéaire & analyse matricielle** (Mathématiques et Statistiques)
	- Notes de cours -> http://math.univ-lyon1.fr/~bernard/teach/numalg/algebre_notes_de_cours_3.pdf

---
### Applications
- To compute the [[Topics/Mathematics/Moore-Penrose inverse|Pseudoinverse]] of a matrix
	- to solve **linear least square problems** (curve fitting, to statistical modelling of noisy data, and to geodetic modeling)
		- other methods : [[___INBOX___/__à trier/The Normal Equation|The Normal Equation]], [[Topics/Mathematics/QR decomposition|QR decomposition]]

---
### History
> [Singular value decomposition > History (wikipedia)](https://en.wikipedia.org/wiki/Singular_value_decomposition#History)
- Camille Jordan & Eugenio Beltrami : independently in **1873/4**, then **1889**, **1915**
- Practical methods for computing SVD since **1954** & **1965/70**

### Books
- *Algèbre des matrices* de Jean Fresnel (**2013**)
- *Numerical Linear Algebra* de LN Trefethen et D Bau III (**1997**)

### See also
- [[___INBOX___/__à trier/Forme bilinéaire|Forme bilinéaire]] : = bilinear mapping(?)
- [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 4 - Matrix Decompositions|Mathematics for Machine Learning - Chapter 4 - Matrix Decompositions#4 5 - Singular Value Decomposition p 119]]
