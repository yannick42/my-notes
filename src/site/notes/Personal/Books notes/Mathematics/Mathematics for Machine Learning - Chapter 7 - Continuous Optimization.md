---
{"dg-publish":true,"dg-permalink":"Chapter 7 - Continuous Optimization","permalink":"/Chapter 7 - Continuous Optimization/"}
---

<-- [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 6 - Probability and Distributions|Chapter 6 - Probability and Distributions]] - [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 8 - When Models Meet Data|Chapter 8 - When Models Meet Data]]

---

- **Optimization algorithms** to find best (optimum) values of parameters, in a model (eg. : [[Topics/Machine Learning/Concepts/Loss functions|objective function]], probabilistic models)
	- Unconstrained / Constrained optimization
- we assume our objective function is differentiable (-> so we have access to its derivative)
- The goal is to move "downhill" (the opposite of the gradient direction)
- **Convex optimization** problems : special class of problems

---
### 7.1 - Optimization using Gradient Descent
-> [[Topics/Machine Learning/Optimization methods/Gradient descent|Gradient descent]]

*Remark :*
- ***condition number*** : $\kappa$  is the ratio of the maximum over the minimum ==singular value== : $\frac{\sigma(A)_{max}}{\sigma(A)_{min}}$
- ***preconditioner*** : instead of directly solving $Ax=b$, one could solve $P^{-1}(Ax-b)=0$,  where $P$  is designed so that $P^{-1}A$ have a better *condition number*

#### 7.1.2 - GD with Momentum
-> [[Topics/Machine Learning/Optimization methods/Extensions of SGD/Momentum method (1964)|Momentum method (1964)]], [[Topics/Machine Learning/Optimization methods/Extensions of SGD/Nesterov momentum (1983)|Nesterov momentum (1983)]]

#### 7.1.3 - Stochastic Gradient Descent
-> [[Topics/Machine Learning/Optimization methods/Stochastic Gradient Descent|Stochastic Gradient Descent]]

---
### 7.2 - Constrained Optimization & Lagrange Multipliers
-> [[Topics/Mathematics/Lagrange multipliers (1788)|Lagrange multipliers (1788)]]

### See Also
- [[Topics/Mathematics/Convex optimization|Convex optimization]]
- 