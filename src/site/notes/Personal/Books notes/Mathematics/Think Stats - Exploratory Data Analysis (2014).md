---
{"dg-publish":true,"dg-permalink":"think-stats-2","permalink":"/think-stats-2/","dgHomeLink":true,"dgPassFrontmatter":false}
---


- by Allen B. Downey (Oct ==2014==, [[___INBOX___/__à trier/O'Reilly books|O'Reilly Media]], **242 pages**)
- **==Online free PDF==** : [https://greenteapress.com/thinkstats2/thinkstats2.pdf](https://greenteapress.com/thinkstats2/thinkstats2.pdf) -> [Table of content](https://greenteapress.com/thinkstats2/html/index.html)
- => [[thinkstats2.pdf]]

> An introduction to practical tools in **EDA**






- It takes a "computational" approach over a mathematical one (Python code rather than math. notations)
- use [[Topics/Machine Learning/Tools, Software/Pandas|Pandas]], [[SciPy|SciPy]] & StatsModels

### Topics
- ...
- Distributions (exponential, normal, lognormal, Pareto, ...)
- correlation
- covariance
- <mark style="background: #FFB86CA6;">hypothesis testing</mark> (p-values, chi-squared tests, power, [[Topics/Mathematics/Statistics and probabilities/Statistics/t-test|t-test]], ...), Linear least squares (residuals, goodness of fit, ...)
- [[Topics/Machine Learning/Concepts/Regression|Regression]]
- [[___INBOX___/__à trier/Time series|Time series]] analysis
- [[___INBOX___/__à trier/Survival analysis|Survival analysis]]
- Analytic methods ([[___INBOX___/__à trier/Central limit theorem|Central limit theorem]] (CLT), ...)

---
### Chapter 5 - Modeling distributions
- empirical distribution defined by their CDF (cumulative distribution function)

#### 5.1 - Exponential distribution
- $CDF(x)=1-e^{-\lambda x}$
- $\lambda$ determines the shape of the function : only **one parameter** to summarize this distribution
	- it can be interpreted as a "rate" of events that occurs in a unit of time
	- the mean is $\frac{1}{\lambda}$
- it appears when measuring times between events ("interarrival times") if events are equally likely to occur
	- eg. ==baby births in an hospital== in a day
- to verify you can model your data with an exponential distribution, one can take the "complementary CDF" from the sample data (*empirical distribution*), and use a log-scale on the y axis : it should be a straight line of slope $-\lambda$ 

#### 5.2 - Normal distribution

==TODO==

#### 5.3 - Normal probability plot
- to test whether the normal distribution is a good model to use for the problem at hand
- ==TODO==

#### 5.4 - The lognormal distribution
- If the $\log$ of the data values have a normal distribution
- eg. ==the distribution of adult weight ?!==
- ==TODO==

#### 5.5 - The Pareto distribution
- Named after an economist Vilfredo Pareto to describe to distribution of wealth
	- "*Since then, it has been used to describe phenomena in the natural and social sciences including **sizes of cities and towns**, **sand particles and meteorites**, **forest fires and earthquakes***"
- ==TODO==

---
### Chapter 7

#### 7.7 - Spearman's rank correlation (p. 101)
-> see note [[Topics/Mathematics/Statistics and probabilities/Statistics/Spearman's rank correlation|Spearman's rank correlation]]

