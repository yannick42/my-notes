---
{"dg-publish":true,"dg-permalink":"spearman-rho","permalink":"/spearman-rho/","dgHomeLink":true,"dgPassFrontmatter":false}
---


**Spearman's rank correlation**
- **aka.** : Spearman's $\rho$ (rho), Spearman's rank(-order) correlation coefficient (fr: corrélation de Spearman)
	- or also noted $r_s$
- developed by [[Topics/Psycho/People/Charles Spearman|Charles Spearman]] (1863-1945), in **1904**
- the $\rho$ value is between **-1** and **+1**
- it's based on ranks of the values => it is **rank correlation statistic**, and it's non-parametric
- it summarizes the strength and direction of a relationship (statistical dependence) between (only) 2 variables (<mark style="background: #ABF7F7A6;">sets of data which can be continuous or ordinal</mark>) when we have not necessarily an "affine/linear" relation, but a **monotonous function**
	- **Continuous** can be : age, weight, height, test scores, survey scores, yearly salary, etc
	- **Monotonicity** -> monotonically increasing or decreasing...
- method often used (more robust) if there are <mark style="background: #BBFABBA6;">outliers</mark> in the data, or non-normal, or <mark style="background: #BBFABBA6;">skewed distribution</mark> 
- Application/Examples
	- to find a correlation in the ==price of a bottle of water== vs. the ==distance== from a key ==area of gentrification==
	- ==TODO==
- **Guideline**
	- .00-.19 “very weak”
	- .20-.39 “weak”
	- .40-.59 “moderate”
	- .60-.79 “strong”
	- .80-1.0 “very strong” 
- It allows to detect monotonous tendencies
	- if affine tendency => it is similar to [[Topics/Mathematics/Statistics and probabilities/Pearson correlation coefficient|Pearson's correlation]]
	- if +1 ou -1 : perfect monotonic correlation
	- if 0 => no correlation between ranks and no monotonic behavior (but doesn't mean no correlation as it can be a quadratic relation, ...etc)

---
**Formulas :**
$$r_s=\frac{cov(R(X), R(Y))}{\sigma_{R(X)} \sigma_{R(Y)}}$$
If ranks are distinct integer (=no tied rank), the "full version" can be simplified to this popular formula :
$$r_s=1-\frac{6\sum d^2}{n^3-n}$$ where $d=R(X_i)-R(Y_i)$

> ⚠️ **Correlation** doesn't necessarily means that one thing affects the other

### Prerequisite
- [[Topics/Mathematics/Statistics and probabilities/Correlation|Correlation]]
- [[Topics/Mathematics/Statistics and probabilities/Pearson correlation coefficient|Pearson correlation coefficient]] (parametric / based on covariance)

### Ranks
- in [[SciPy|SciPy]] : `scipy.stats.rankdata(a)`
- in [[___INBOX___/__à trier/Excel|Excel]] : Rank.EQ or Rank.AVG

### Python
- `scipy.stats.spearmanr(x, y)`
- in [[Topics/Machine Learning/Tools, Software/Pandas|Pandas]] : `df.corr(method='spearman')`

### TODO
- [ ] Find a practical application in a real dataset
- [ ] Complete this note with charts and more example of usage
- [ ] When a Spearman rho **table** (when doing [[Topics/Mathematics/Statistics and probabilities/Statistics/Hypothesis testing|Hypothesis testing]]) is needed ?
	- only if up to 30 samples ?
	- https://www.real-statistics.com/statistics-tables/spearmans-rho-table/
	- https://www.real-statistics.com/correlation/spearmans-rank-correlation/spearmans-rank-correlation-detailed/
- [ ] What is the link with [[___INBOX___/__à trier/t-test|t-test]] ?
	- when $n \geq 10$ ?

### Sources
- [[Personal/Books notes/Mathematics/Think Stats - Exploratory Data Analysis (2014)|Think Stats - Exploratory Data Analysis (2014)]] > *Chapter 7.7*
- [Encyclopedia of Math](https://encyclopediaofmath.org/wiki/Spearman_coefficient_of_rank_correlation)
- [Wikipedia (fr)](https://fr.wikipedia.org/wiki/Corr%C3%A9lation_de_Spearman) #MEMEX

### See also
- [[Topics/Mathematics/Statistics and probabilities/Pearson correlation coefficient|Pearson correlation coefficient]]
- [[p-value|p-value]] & [[Topics/Mathematics/Statistics and probabilities/Confidence interval|Confidence interval]]
- Other tests based on ==rank correlation==
	- **Kendall's tau** : $\tau$ (non parametric, too)
		- as with the $\rho$ : it is also a special case of a more general correlation coefficient => ??
		- ==$\tau$ is recommended first== (it has more desirable statistic properties ?), then use $\rho$
	- Friedman test
	- Kruskal-Wallis test
	- ...
- (inverse) Fisher transformation => ?

---
https://geographyfieldwork.com/SpearmansRank.htm - applied to **geography** topics
