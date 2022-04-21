---
{"dg-publish":true,"dg-permalink":"determinant","permalink":"/determinant/","dgHomeLink":true,"dgPassFrontmatter":false}
---


- if the determinant is 0 => the matrix is not invertible
- Sarrus' rule : mnemotechnic for 3 by 3 matrices
- for lower or upper triangular matrices : $det(A)=\prod\limits_{i=1}^{n}T_{ii}$
- determinant is **the signed volume of a n-dimensional parrellelepiped formed by columns** of the matrix A
- for n > 3 => use ==Laplace extension==
	- minor / cofactor -> ?
- **properties**
	- $det(AB)=det(A)det(B)$
	- determinants are invariable to transposition
	- if A is regular (=invertible) => $det(A^{-1})=\frac{1}{det(A)}$
	- **similar matrices** possess the same determinant
	- the determinant is **invariant** to the choice of basis of a linear mapping
	- swapping 2 rows/columns change the sign of $det(A)$
- -> the determinant can be calculated with Gaussian elimination by put A in row-echelon form -> then multiply the elements on the diagonal to get $det(A)$
- $det(A)\neq 0$ if $rk(A)=n$ -> is invertible only if it is **==full rank==**

### See also
- [[___INBOX___/__à trier/Matrices|Matrix]]
- [[___INBOX___/__à trier/Trace (matrix)|Trace (matrix)]]
- [[Characteristic polynomial (matrix)|Characteristic polynomial (matrix)]]
- [[___INBOX___/__à trier/Eigenvalues|Eigenvalues]]
