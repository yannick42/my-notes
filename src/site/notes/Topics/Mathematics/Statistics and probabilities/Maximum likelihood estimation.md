---
{"dg-publish":true,"permalink":"/topics/mathematics/statistics-and-probabilities/maximum-likelihood-estimation/","dgHomeLink":true,"dgPassFrontmatter":false}
---


**Maximum likelihood estimation**
> shortened to **MLE**
- Developed by [[Topics/Mathematics/People/Ronald Fisher|Ronald Fisher]] in **1922** (he worked on it since 1912?)
- fr: Maximum de vraisemblance
- ==a probabilistic framework== & the **dominant method** in [[Statistical inference|Statistical inference]] for parameter estimation
	- intuitive and flexible => ?
	- unified approach to estimation
	- based on an assumption (bet?) on the distribution of $y$ (Poisson (eg. for non-negative count data), Gamma, …) : a model (a data generating process)
	- but it **should not always be used** (it has some disadvantages)
	- can be sensitive to the choice of starting value
- Used in
	- Linear Regression model ? (instead of [[___INBOX___/__à trier/Least-squares method|Least-squares]] ?!)
	- **GLM**
		- [[Topics/Machine Learning/Models/Logistic regression|Logistic regression]]
		- Logit / Probit models (Chester Bliss, **1934**)
		- [[___INBOX___/__à trier/Poisson regression|Poisson regression]]
- the **probability (density function) of the observed sample** $f(x_1,x_2,…,x_n|\theta)=\prod\limits_{i=1}^n f(x_i|\theta)$ because we suppose each data sample as independent from others, and it is also equivalent to the **likelihood** $L(\theta|x_1,...,x_n)$ because we can ignore the prior $p(x)$ and evidence (denominator $p(\theta)$) as it doesn't change the shape of the function to maximize (in the [[Topics/Mathematics/Statistics and probabilities/Bayes' formula|Bayes' formula]] : $\text{posterior}=\frac{\text{likelihood} \times \text{prior}}{\text{evidence}}$)
- so it's a method to find/estimate the parameters of a probability distribution (eg. for a Gaussian dist. : $\mu$, $\sigma^2$) by maximizing a **likelihood function** $L(\theta)$ with the data $x_i$ :
$$\theta_{ML}=\operatorname*{arg\,max}_\theta P(y|x,\theta)$$
- the **likelihood** = $p(y|x,\theta)$, it is **not** a probability distribution in $\theta$ (with is unknown)
	- it doesn't integrate to 1 (=*is unnormalized*), and may not even be integrable wrt. $\theta$)
	- -> it's the probability of getting the data we observed

---
### Statistical properties
> https://fr.wikipedia.org/wiki/Maximum_de_vraisemblance#Propri%C3%A9t%C3%A9s
- convergent
- most efficient (=small variance?) estimator (if the model is assumed correctly) (?)
- results in *unbiased* estimates in larger samples => ??? (can be biased in smaller samples)

---
- The point in "parameter space" that maximize this function is called the ==maximum likelihood estimate==
	- **estimate** (realization) = the value of $\theta$ at which we have the maximum likelihood
- **estimator** (random variable) = 
- ==log-likelihood== => generally simpler to optimize than likelihood (sums rather than products)
	- especially for the functions in the [[Topics/Mathematics/Statistics and probabilities/Exponential family|Exponential family]] → <mark style="background: #FF5582A6;">why ?</mark>
	- the log function is monotone transform, so the max/min is not changed
	- see [[Topics/Machine Learning/Loss functions/Negative log-likelihood|Negative log-likelihood]]
- <u>Solutions</u>
	- if **closed-form solution** possible => "faster" ? (as in [[___INBOX___/__à trier/Least-squares method|Least-squares]] with [[___INBOX___/__à trier/The Normal Equation|The Normal Equation]] ?)
	- it's an [[Topics/Mathematics/Optimization|optimization]] problem computed with **numerical methods**
		- **iterative gradient ascent** (or descent if negative log-likelihood)
			- [[Topics/Mathematics/Calculus/Newton’s method|Newton’s method]]
		- [[Topics/Mathematics/Lagrange multipliers (1788)|Lagrange multipliers (1788)]]
		- **EM algorithm** ? -> see [[___INBOX___/__à trier/Expectation-maximization algorithm|Expectation-maximization algorithm]]
		- [[___INBOX___/__à trier/Nelder-Mead method (1965)|Nelder-Mead method (1965)]]
- Alternatives/other methods
	- (generalized) [[___INBOX___/__à trier/Method of moments|method of moments]] estimate
	- least square regression (for linear model)
- in [[Topics/Mathematics/Statistics and probabilities/Bayesian inference, analysis ...|Bayesian inference, analysis ...]], **MLE** is a special case a **MAP** (Maximum a posteriori estimation)

---
### Example where MLE fails
#### German tank problem
> https://www.youtube.com/watch?v=L73kGEw_YkY
> https://andre-ye.medium.com/how-data-science-gave-the-allied-forces-an-edge-in-world-war-ii-7fe92a74add5
- a historical application of statistics in World War II by Allied forces to estimate the monthly production of German tanks from very limited data (the serial numbers of those captured or destroyed)
- but **MLE** would have use **the max seen value** (because when we take the derivative, it's never equal to $0$ => there is no max…?)
=> ==it is a biased estimator !==
- → so they used(?) **MVUE** : minimum-variance unbiased estimator
	- https://en.wikipedia.org/wiki/Minimum-variance_unbiased_estimator
- $\hat{N} = \frac{k+1}{k} m – 1 = m + \frac{m}{k} – 1$ (??)
	- $m$ = highest serial number encountered
	- $k$ = number of tank captured

---
### Prerequisites / See also / things to know / refresher
- [[___INBOX___/__à trier/Joint probability distribution|Joint probability]] + likelihood of the sample
- [[Topics/Mathematics/Statistics and probabilities/Probability distributions|Probability distributions]] & their parameters
- [[___INBOX___/__à trier/Conditional probability|Conditional probability]]
- [[___INBOX___/__à trier/Random process|Random process]]
- invariance principle = ?
- Conditional log-likelihood
- [[___INBOX___/__à trier/Marginal distribution|Marginal distribution]]
- [[Topics/Machine Learning/Books/An Introduction to Statistical Learning/An Introduction to Statistical Learning (2013, 2021)#4 3 2 - Estimating the regression coefficients|An Introduction to Statistical Learning (2013, 2021)#4 3 2 - Estimating the regression coefficients]] (MLE, Likelihood function, ...)
	- There is a link to "**likelihood ratio test**" in statistics and **Neyman-Pearson lemma**

---
### Resources
- https://en.wikipedia.org/wiki/Maximum_likelihood_estimation
- https://fr.wikipedia.org/wiki/Maximum_de_vraisemblance
- https://towardsdatascience.com/probability-concepts-explained-maximum-likelihood-estimation-c7b4342fdbb1

---
### References
https://en.wikipedia.org/wiki/German_tank_problem
- Livre sur les stats et la guerre ? : https://www.persee.fr/doc/polit_0032-342x_1991_num_56_2_4046_t1_0568_0000_3

---
### Course/Notes/Blogs articles
- https://www.probabilitycourse.com/chapter8/8_2_3_max_likelihood_estimation.php
	- simple exercices with solution
- https://online.stat.psu.edu/stat415/lesson/1/1.2 - PennState - **STAT 415**
- https://www.univ-orleans.fr/deg/masters/ESA/CH/Chapter2_MLE.pdf - Advanced Econometrics - HEC Lausanne (PDF slides)
- https://python.quantecon.org/mle.html
	- [ ] => https://colab.research.google.com/drive/1dlmWjabeE18I7ZJMYYwPOtDp3qyO7ny1
	- on [[___INBOX___/__à trier/Poisson regression|Poisson regression]]
- [ ] Read https://towardsdatascience.com/a-gentle-introduction-to-maximum-likelihood-estimation-9fbff27ea12f #ml/MSG/todo 
- [x] https://www.aptech.com/blog/beginners-guide-to-maximum-likelihood-estimation-in-gauss/ - **Beginner's Guide**
	- eg. with linear model + probit

### See also
- [[___INBOX___/__à trier/Least-squares method|Least-squares method]]
- Méthode des moments => ? [[___INBOX___/__à trier/Method of moments|Method of moments]]
