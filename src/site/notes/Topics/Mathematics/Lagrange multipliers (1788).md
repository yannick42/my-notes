---
{"dg-publish":true,"dg-permalink":"Lagrange multipliers","permalink":"/Lagrange multipliers/"}
---

<!--
Vu sur le MOOC [[Coursera]](?) de l'Imperial College of London avec : [[PCA]] ...etc
-->

- a basic (and powerful) mathematical tool for non-linear [[Topics/Mathematics/Optimization|optimization]] problems that can be equality or inequality constrained
- the goal is to find a *local* extrema of a real function $f(x,y,...)$ subject to a constraint $g(x,y,...)=k$
- it's widely used/applied in science, economics and engineering, and "everyday life" (?)
	- maximizing profit subject to a limited resource
	- $\lambda$ often has an identifiable significance
	- in power systems : (economic) $\lambda-$dispatch is used to minimize the hourly cost of production
		- => calculate the optimal generation scheduling : to know which of the $i$ generators to use
- the "max" is when both gradients are identical : $\nabla f(x_0,y_0) = \lambda \nabla g(x_0,y_0)$
	- tangent line (or surface, ...)
- They can be multiple constraints => ? at least 2...?
- ...

---
### Definition
- the Lagrange function $\mathcal{L}(x,\lambda)=f(x)-\lambda g(x)$
- (KKT conditions ?)

---
### Applications
- **The problem of Dido** : which curve has the maximum area for a given perimeter
	- https://mathematicalgarden.wordpress.com/2008/12/21/the-problem-of-dido/
		- it uses
			- [[___INBOX___/__à trier/Green's theorem (vector calculus)|Green's theorem (vector calculus)]]
			- Euler-Lagrange equations

#### Applications in ML
- in **PCA** and **SVM**

---
### Source
- [[___INBOX___/__à trier/Calculus - James Stewart|Calculus - James Stewart]] - Chapter 14.8
- [[Topics/Machine Learning/Books/Mathematics for Machine Learning (2020)|Mathematics for Machine Learning (2020)]] - Chapter 7.2
- Paper
	- "Lagrange Multipliers and their Applications" - Huijuan Li (2008)
- ['Nice' applications of Lagrange multiplier (math SE)](https://math.stackexchange.com/questions/2157958/nice-applications-of-lagrange-multipliers)
- [Good examples of Lagrange multiplier problems](https://matheducators.stackexchange.com/questions/8371/good-examples-of-lagrange-multiplier-problems)

---
https://math.stackexchange.com/questions/769437/history-of-lagrange-multipliers
- 1764 ?
