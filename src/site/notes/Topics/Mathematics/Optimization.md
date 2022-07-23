---
{"dg-publish":true,"permalink":"/topics/mathematics/optimization/","dgHomeLink":true,"dgPassFrontmatter":false}
---


Pour maximiser/minimiser une function analytiquement ou numériquement
- [[___INBOX___/__à trier/Evolutionary algorithms|Evolutionary algorithms]]
	- [[___INBOX___/__à trier/Particle Swarm Optimization (1995)|Particle Swarm Optimization (1995)]]
- [[Topics/IT-Computing/Computer Science/Algorithms/Simulated annealing|Simulated annealing]]
- in Neural Networks/Logistic regression/Linear regression/…
	- [[Topics/Machine Learning/Optimization methods/Gradient descent|Gradient descent]]
	- [[Topics/Machine Learning/Optimization methods/Stochastic Gradient Descent|Stochastic Gradient Descent]]
	- No gradient methods => https://towardsdatascience.com/the-fascinating-no-gradient-approach-to-neural-net-optimization-abb287f88c97
		- PSO
		- Simulated annealing
		- …
-  **L-BFGS** (by default as [[Topics/Machine Learning/Tools, Software/sklearn|sklearn]]'s Logistic Regression solver)
	- Limited memory
	- [[Topics/Machine Learning/Optimization methods/BFGS|BFGS]]
- conjugate-gradient method
	- to invert the local [[___INBOX___/__à trier/Hessian|Hessian]] ?!
- Newton-like methods → [[Topics/Mathematics/Calculus/Newton’s method|Newton’s method]]
	- Apparu au XVIIe siècle
	- iterative method
- [[___INBOX___/__à trier/Nelder-Mead method (1965)|Nelder-Mead method (1965)]]
- **Test functions (artificial landspaces)** : to determine robustness, precision, convergence rate
	- Rosenbrock banana function (1960)
	- Himmelblau's function
	- Simionescu's function

---
**SLSQP** : sequential LS
https://stackoverflow.com/questions/59808494/how-does-the-slsqp-optimization-algorithm-work

### Quadratic optimization
fr: Optimisation quadratique
- la fonction objectif est une **forme quadratique**

### Python
- with [[___INBOX___/__à trier/SciPy|SciPy]] : https://scipy.github.io/devdocs/tutorial/optimize.html

### Resourcs
- [[___INBOX___/__à trier/Probabilistic Machine Learning - An Introduction (2022)|Probabilistic Machine Learning - An Introduction (2022)]] - Chapter 8
- [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 7 - Continuous Optimization|Mathematics for Machine Learning - Chapter 7 - Continuous Optimization]]
