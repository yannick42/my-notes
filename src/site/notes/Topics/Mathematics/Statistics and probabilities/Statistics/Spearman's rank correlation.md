---
{"dg-publish":true,"dg-permalink":"spearman-rho","permalink":"/spearman-rho/"}
---

**Spearman's rank correlation**

- ***aka.*** $\rho$ (rho) de Spearman, Spearman's rank(-order) correlation coefficient (fr: corrélation de Spearman)
	- or also noted $r_s$
- developed by [[Topics/Psycho/People/Charles Spearman|Charles Spearman]] (1863-1945), in **1904**
- the value ranges between **-1** and **+1**
- it's based on ranks of the values => it is **rank correlation statistic**, and it's nonparametric
- it summarizes the strength and direction of a relationship (statistical dependence) between 2 variables (sets of data) when we have not necessarily an "affine" relation, but a monotonous function (whether linear/affine or not) => ?
- Application/Examples
	- to find a correlation in the ==price of a bottle of water== vs. the ==distance== from a key ==area of gentrification==
- It allows to detect monotone tendencies => ?
	- if affine tendency => it is similar to [[Topics/Mathematics/Statistics and probabilities/Pearson correlation coefficient|Pearson's correlation]]
$$r_s=\frac{cov(R(X), R(Y)}{\sigma_{R(X)} \sigma_{R(Y)}}$$
If ranks are distinct integer, it can be simplified to this popular formula :
$$r_s=1-\frac{6\sum d^2}{n^3-n}$$ where $d=R(X_i)-R(Y_i)$

> **Correlation** doesn't necessarily means that one thing affect the other

### Ranks
- in [[SciPy]] : `scipy.stats.rankdata(a)`
- in [[___INBOX___/__à trier/Excel|Excel]] : Rank.EQ or Rank.AVG

### Python
- `scipy.stats.spearmanr(x, y)`

### Sources
- [[Personal/Books notes/Mathematics/Think Stats - Exploratory Data Analysis (2014)|Think Stats - Exploratory Data Analysis (2014)]] - Chapter 7
- https://encyclopediaofmath.org/wiki/Spearman_coefficient_of_rank_correlation
- https://fr.wikipedia.org/wiki/Corr%C3%A9lation_de_Spearman #MEMEX

### See also
- [[Topics/Mathematics/Statistics and probabilities/Pearson correlation coefficient|Pearson correlation coefficient]]
- Other tests based on ==rank correlation==
	- Kendall's tau : $\tau$
		- as with the $\rho$ : it is also a special case of a more general correlation coefficient => ??
	- Friedman test
	- Kruskal-Wallis test
	- ...

---
https://geographyfieldwork.com/SpearmansRank.htm - applied to **geography** topics
