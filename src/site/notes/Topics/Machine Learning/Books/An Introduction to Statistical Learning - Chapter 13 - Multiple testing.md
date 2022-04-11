---
{"dg-publish":true,"dg-permalink":"isl/chap13","permalink":"/isl/chap13/"}
---

Book's main note : [[Topics/Machine Learning/Books/An Introduction to Statistical Learning (2013, 2021)|An Introduction to Statistical Learning (2013, 2021)]]

### Chapter 13 : ==Multiple testing==
- this chapter focuses on [[Topics/Mathematics/Statistics and probabilities/Statistics/Hypothesis testing|Hypothesis testing]] (<mark style="background: #FF5582A6;">but not the basics, as lots of book already cover that !</mark>)
- brief overview of 
	- null hypothesis $H_0$
	- p-values : to quantify the results of a hypothesis test
	- test statistics
- Classical solution to "multiple hypothesis testing" : ==§13.3==
- More recent ones : ==§13.4== (**false discovery rate**, it dates from the **1990s**) & ==13.5==

#### 13.1 - A quick review of Hypothesis testing
<mark style="background: #CACFD9A6;">a rigorous statistical framework for answering simple “yes-or-no” questions</mark> 
##### 13.1.1 Testing a hypothesis
**4 steps :**
- we ==divide the world== into 2 possibilities : **null hypothesis** ($H_0$, *default state of belief of the world*) & **alternative hypothesis** ($H_1$ or $H_a$ ...)
	- we focus on using data to reject $H_0$ (hopefully)
	- if we fail : maybe $H_0$ really holds or we may need a higher-quality dataset or something...
- we ==construct/compute== a test statistic T
	- eg. : a two-sample **t-statistic** (for treatment/control groups of mice **mean** blood pressure)
- ==Compute the p-value==
	- **p-value** = the probability of observing a test statistic equal or bigger than the one observed (in previous step) under the assumption that $H_0$ is in fact true
	- ==> **Therefore, a small p-value provides evidence against the null hypothesis**
- ==Decide== whether to reject $H_0$
	- If the p-value is suﬃciently small, then we will want to reject $H_0$ (and, therefore, make a “discovery”)
	- <mark style="background: #FFB86CA6;">data analyst should report the p-value, not only the threshold used</mark> 
	- in some fields : 0.05 (5%) is used. In physics it can be $10^{-9}$

---
##### 13.1.2 Type I & Type II Errors
**Type I error** (false positive) : rejecting the true null hypothesis
**Type II error** (false negative) : we do not reject a false null hypothesis

Their is a trade-off to find...
> Type I errors are more "serious"

---
#### 13.2 The challenge of multiple testing
- when lots of null hypothesis to test => we can get very small p-value "by chance"

#### 13.3 Family-wise Error Rate (FWER)
- a generalization of Type I errors to multiple testing
- controlling FWER at level $\alpha$

##### 13.3.2 Approches to control the FWER
- The Bonferroni method
	- the simplest yet the strictest ?
- Holm's Step-Down procedure (1979)
	- 
- 2 special cases
	- Tukey's method
	- Scheffé's method

##### 13.3.3 Trade-off between the FWER and Power

#### 13.4 False discovery rate (FDR)

#### 13.5 

---
https://towardsdatascience.com/multiple-hypothesis-testing-correction-for-data-scientist-46d3a3d1611d (FWER (Bonferroni correction), FDR, Python package : MultiPy (for Multiple Hypothesis Correction))