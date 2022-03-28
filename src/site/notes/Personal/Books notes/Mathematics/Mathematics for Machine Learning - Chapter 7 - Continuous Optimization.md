---
{"dg-publish":true,"dg-permalink":"mml/chap7","permalink":"/mml/chap7/"}
---

↑ [[Topics/Published notes/MML (home)|Mathematics for Machine Learning (home)]]
<-- [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 6 - Probability and Distributions|Chapter 6 - Probability and Distributions]] - [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 8 - When Models Meet Data|Chapter 8 - When Models Meet Data]]

---

- **Optimization algorithms** to find best (optimum) values of parameters, in a model (eg. : [[Topics/Machine Learning/Concepts/Loss functions|objective function]], probabilistic models)
	- Unconstrained / Constrained optimization
- we assume our objective function is differentiable (-> so we have access to its derivative)
- The goal is to move "downhill" (the opposite of the gradient direction)
- **Convex optimization** problems : special class of problems where global optimum can be reached (?)

---
### 7.1 - Optimization using Gradient Descent
-> [[Topics/Machine Learning/Optimization methods/Gradient descent|Gradient descent]]

*Remark :*
- ***condition number*** : $\kappa$  is the ratio of the maximum over the minimum ==singular value== : $\frac{\sigma_{max}(A)}{\sigma_{min}(A)}$
- ***preconditioner*** : instead of directly solving $Ax=b$, one could solve $P^{-1}(Ax-b)=0$,  where $P$  is designed so that $P^{-1}A$ have a better *condition number*

#### 7.1.2 - GD with Momentum
-> [[Topics/Machine Learning/Optimization methods/Extensions of SGD/Momentum method (1964)|Momentum method (1964)]], [[Topics/Machine Learning/Optimization methods/Extensions of SGD/Nesterov momentum (1983)|Nesterov momentum (1983)]]

#### 7.1.3 - Stochastic Gradient Descent
-> [[Topics/Machine Learning/Optimization methods/Stochastic Gradient Descent|Stochastic Gradient Descent]]

---
### 7.2 - Constrained Optimization & Lagrange Multipliers
- [[Topics/Mathematics/Lagrange multipliers (1788)|Lagrange multipliers (1788)]]
	- $\lambda_i\geq 0$
- duality -> ?

---
### 7.3 - Convex Optimization
-> see [[Topics/Mathematics/Convex optimization|Convex optimization]]
- Jensen's inequality -> ?


#### 7.3.1 - Linear Programming
- *by convention* : minimize the primal & maximize the dual


#### 7.3.2 - Quadratic Programming
- We'll see an application in Chapter 12 : for the squared norm in [[Topics/Machine Learning/Models/Support Vector Machine (1992)|SVM]]


#### 7.3.3 - Legendre-Fenchel Transform & Convex Conjugate
> **Physics students** are often introduced to the **Legendre transform** as relating the **Lagrangian** and the **Hamiltonian** in **classical mechanics**

---
### 7.4 - Further Readings
- Continuous optimization is an active area of research
- Other methods
	- Quasi-Newton methods:  L-BFGS (cheaper approximation to estimate the [[___INBOX___/__à trier/Hessian|Hessian]])
	- Mirror descent (2003?)
	- Natural gradient (2012?)
	- subgradient methods (see Bertsekas, 1999)
