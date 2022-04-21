---
{"dg-publish":true,"permalink":"/topics/mathematics/statistics-and-probabilities/maximum-likelihood-estimation/","dgHomeLink":true,"dgPassFrontmatter":false}
---


> shortened to **MLE**

- Developed by [[Topics/Mathematics/People/Ronald Fisher|Ronald Fisher]] in **1922** (he worked on it since 1912?)
- ==a probabilistic framework== & the **dominant method** in Statistical inference for parameter estimation
	- Intuitive and flexible => ?
	- Unified approach to estimation
	- based on an assumption (bet?) on the distribution of y
- Properties => ?
- Used in
	- Linear Regression model
	- Logit/Probit models
	- ...
- a method to find/estimate the parameters of a probability distribution (ex: $\mu$, $\sigma^2$) by maximizing a **likelihood function** $L(\theta)$
$$\theta_{ML}=\operatorname*{arg\,max}_\theta p(y|x,\theta)$$
- the **likelihood** = $p(y|x,\theta)$, is not a probability distribution in $\theta$
	- it doesn't integrate to 1 = *is unnormalized*, and may not even be integrable wrt. $\theta$)
	- = probability of getting the data we observed
- The point in "parameter space" that maximize this function is called the ==maximum likelihood estimate==
	- **estimate** (realization) = the value of $\theta$ at which we have the maximum likelihood
- **estimator** (random variable) = 
- ==log-likelihood== => generally simpler to optimize than likelihood
	- especially for the functions in the [[Topics/Mathematics/Statistics and probabilities/Exponential family|Exponential family]]
- Solutions
	- if **closed-form solution** possible => "faster" ?
	- **iterative gradient ascent** (or descent if negative log-likelihood)
	- EM algorithm ? -> see [[___INBOX___/__à trier/Expectation-maximization algorithm|Expectation-maximization algorithm]]

---
### Example where MLE fails(?)

"**German tank problem**" : a historical application of statistics in World War II by Allied forces to estimate the monthly production of German tanks from very limited data (the serial numbers of those captured or destroyed)
- $\hat{N} = \frac{k+1}{k} m – 1 = m + \frac{m}{k} – 1$
	- m = highest serial number encountered
	- k = number of tank captured
=> MLE would have use the max seen value... ?

---
- in [[Topics/Mathematics/Statistics and probabilities/Bayesian inference, analysis ...|Bayesian inference, analysis ...]], **MLE** is a special case a **MAP** (Maximum a posteriori estimation)

### TODO
- joint probability + likelihood of the sample
- invariance principle = ?
- Conditional log-likelihood

### See also/things to know/refresher
- [[Topics/Mathematics/Statistics and probabilities/Probability distributions|Probability distributions]] & their parameters
- [[___INBOX___/__à trier/Probabilité conditionnelle|Conditional probability]]
- [[___INBOX___/__à trier/Random process|Random process]]
- Marginal distribution => ?
- Joint probability

### Resources
- https://en.wikipedia.org/wiki/Maximum_likelihood_estimation
- https://fr.wikipedia.org/wiki/Maximum_de_vraisemblance
- https://towardsdatascience.com/probability-concepts-explained-maximum-likelihood-estimation-c7b4342fdbb1

### References
https://en.wikipedia.org/wiki/German_tank_problem
- Livre sur les stats et la guerre ? : https://www.persee.fr/doc/polit_0032-342x_1991_num_56_2_4046_t1_0568_0000_3

### Course/Notes
- https://www.probabilitycourse.com/chapter8/8_2_3_max_likelihood_estimation.php
- https://online.stat.psu.edu/stat415/lesson/1/1.2 - PennState - **STAT 415**
- https://www.univ-orleans.fr/deg/masters/ESA/CH/Chapter2_MLE.pdf - Advanced Econometrics - HEC Lausanne (PDF slides)
