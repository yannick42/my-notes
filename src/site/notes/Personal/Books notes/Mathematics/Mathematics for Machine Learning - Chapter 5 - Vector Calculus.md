---
{"dg-publish":true,"dg-permalink":"Chapter 5 - Vector Calculus","permalink":"/Chapter 5 - Vector Calculus/"}
---

<-- [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 4 - Matrix Decompositions|Chapter 4 - Matrix Decompositions]] - [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 6 - Probability and Distributions|Chapter 6 - Probability and Distributions]] -->

---

-> in curve fitting, density estimation (GMM), ...

(sub-differentials : functions that are continuous but not differentiable at certain points)

## 5.1 Differentiation of Univariate Functions

Difference quotient : $\frac{\delta y}{\delta x}=\frac{f(x+\delta x) - f(x)}{\delta x}$
Definition of the derivative : $\frac{df}{dx}=\lim\limits_{h\rightarrow 0}\frac{f(x+h)-f(x)}{h}$
-> the secant becomes a tangent

Example 5.2 -> ==TODO==

### 5.1.1 - Taylor series
 -> a **Taylor series** is a representation of a function as an infinite sum of terms (determined using derivatives of $f$ evaluated at $x_0$)
 - **Taylor polynomials** of degree $n$ : $T_n(x)$ -> it is in general an approximation of a function
 - for $x_0=0$ we get a special case : **The MacLaurin series**
 - if $f(x)=T_\infty(x)$ then $f$ is called ***analytic***
 - $C^\infty$ mean continuously differentiable

### 5.1.2 - Differentiation Rules
- Product Rule -> 
- Quotient Rule -> 
- Sum Rule -> 
- [[Topics/Mathematics/Calculus/Chain Rule|Chain Rule]] -> 

## 5.2 - Partial Differentiation and Gradients

## 5.3

## 5.4

## 5.5 - Useful Identity for Computing Gradients

## 5.6 - Backpropagation and Automatic Differentiation
- the [[Topics/Machine Learning/Concepts/Basics/Backpropagation (1986)|backpropagation]] algorithm (Kelley, 1960; Bryson, 1961; Dreyfus, 1962; Rummelhart et al., 1986)

### 5.6.2 - Automatic Differentiation
- Backpropagation is a special case of a general techniques in [[___INBOX___/__à trier/Numerical analysis|Numerical analysis]] called *==automatic differentiation==*
	- numerically (instead of symbolically) compute gradient by working with intermediate variables & applying the [[Topics/Mathematics/Calculus/Chain Rule|Chain Rule]].
	- forward / reverse modes
		- -> see Baydin et al. (**2018**) - *Automatic Differentiation in Machine Learning: A Survey* => https://arxiv.org/abs/1502.05767
 
---
## 5.7 - Higher-Order Derivatives
- ex: in [[___INBOX___/__à trier/Newton’s method|Newton’s method]] for optimization, we need second-order derivatives

## 5.8 - Linearization and Multivariate Taylor Series
- einsum -> in [[___INBOX___/__à trier/Numpy|Numpy]] : Einstein's sum

## 5.9 - Further readings
- **[[___INBOX___/__à trier/Matrix differential Calculus with Applications in Statistics and Econometrics (2007)|Matrix differential Calculus with Applications in Statistics and Econometrics (2007)]]** : Magnus & Neudecker (2007)
- **Automatic differentiation** (history) : Griewand & Walther (2003, 2008), Elliott (2009)
