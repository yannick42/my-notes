---
{"dg-publish":true,"permalink":"/topics/mathematics/moore-penrose-inverse/","dgHomeLink":true,"dgPassFrontmatter":false}
---


- most widely known generalization of the inverse matrix
- aka. pseudoinverse (only...)
- independently described in **1920**, **1951**, **1955** ([[Topics/Sciences/Physics/People/Roger Penrose|Roger Penrose]])
- applications/usage :
	- to compute "best fit" (least-squares) solution to [[___INBOX___/__à trier/Systems of Linear Equations|Systems of Linear Equations]] that lacks solutions
		- or find "minimum (Euclidian) norm" solution when multiple solutions
	- facilitate statements and proofs of results in [[Topics/Mathematics/Linear Algebra|Linear Algebra]]
- can be computed using [[Topics/Mathematics/Singular Value Decomposition|Singular Value Decomposition]]
- exists and is unique for every matrices ?
- provided in
	- [[___INBOX___/__à trier/Numpy|Numpy]] : `np.linalg.pinv` (SVD-based algorithm)
	- [[SciPy|SciPy]] : `scipy.linalg.pinv` (least-squares solver)

---
https://en.wikipedia.org/wiki/Moore%E2%80%93Penrose_inverse
