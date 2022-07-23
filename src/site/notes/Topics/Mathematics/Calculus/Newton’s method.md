---
{"dg-publish":true,"permalink":"/topics/mathematics/calculus/newton-s-method/","dgHomeLink":true,"dgPassFrontmatter":false}
---


aka. **Newton-Raphson's method**
- **iterative** procedure in [[___INBOX___/__à trier/Numerical analysis|Numerical analysis]]
- powerful technique (?) to approximate solution of "x-intercepts" (aka. zeros or **roots**)
	- for equations hard to solve by hand
- generally convergence is quadratic => precision roughly double at each step (?)
- pour trouver numériquement une approximation d'une racine (un zéro) d'une fonction
- initial guess => ?? eg. the OLS result … ?
$$x_{n+1}=x_n-\frac{f(x_n)}{f'(x_n)}$$
=> until the difference is $<\epsilon$
- 

---
### Applications
- in [[Topics/Mathematics/Statistics and probabilities/Maximum likelihood estimation|Maximum likelihood estimation]]
	- → https://www.jorgelopezperez.com/posts/maximum-likelihood-estimation-and-the-newton-raphson-method/

---
### Other root-finding algorithms
- Householder's methods
- …

---
https://en.wikipedia.org/wiki/Newton%27s_method

> https://fr.wikipedia.org/wiki/M%C3%A9thode_quasi-Newton - pour les **systèmes d'équations non-linéaires** !
