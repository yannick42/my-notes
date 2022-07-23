---
{"dg-publish":true,"dg-permalink":"simulated-annealing","permalink":"/simulated-annealing/","dgHomeLink":true,"dgPassFrontmatter":false}
---


**Simulated annealing** (SA)
- *fr: recuit simulé*
- An [[Topics/Mathematics/Optimization|optimization]] method (metaheuristic) inspired by a process (annealing : heating & controlled cooling) used in **metallurgy** to approximate(?) the global optimum in a large search space.
- Independently developed (and named) in **1983** (Kirkpatrick, Gelatt Jr. & Vecchi, IBM, for [[Topics/IT-Computing/Traveling salesman problem|TSP]]) and **1985** (Cerny). Similar techniques existed from 1970 (?)
- used in
	- [[NP-hard|NP-hard]] problems
		- [[Topics/IT-Computing/Traveling salesman problem|traveling salesman problem]]
		- boolean satisfiability problem (SAT)
		- job-shop scheduling (JSP)
			- TSP is a special case of JSP
	- protein structure prediction
- may be preferable to "exact" algorithms as [[Topics/Machine Learning/Optimization methods/Gradient descent|Gradient descent]] or [[Topics/IT-Computing/Computer Science/Methods/Branch & Bound (1960)|Branch & Bound (1960)]]


---
https://fr.wikipedia.org/wiki/Recuit_simul%C3%A9
https://en.wikipedia.org/wiki/Simulated_annealing