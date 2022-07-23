---
{"dg-publish":true,"dg-permalink":"fisher-exact-test","permalink":"/fisher-exact-test/","dgHomeLink":true,"dgPassFrontmatter":false}
---


**Fisher's exact test**
- proposed in **1934** by [[Topics/Mathematics/People/Ronald A. Fisher|Ronald A. Fisher]], in [[Topics/Mathematics/Statistics and probabilities/Statistics/Statistics|statistics]] for [[Topics/Mathematics/Statistics and probabilities/Statistics/Hypothesis testing|hypothesis testing]]
- it's a <mark style="background: #BBFABBA6;">test of independence</mark>, which is **non-parametric** (do not require assumptions/distribution-free)
- it allows to ==reject or accept== the **independence** ($H_0$) of (two?) categorical (aka. qualitative) variables
	- **examples** :
		- **efficacy** (cured/not cured) of **drugs** (treatment/control group)
		- Is the propensity to **buy a particular item** is independent of **gender** ?
- used in the analysis of ($2\times 2$ ?) [[Topics/Mathematics/Statistics and probabilities/Statistics/Contingency table|contingency tables]] of frequency counts
- it's an **exact test**, contrary to other tests (eg. $\chi^2$-test) => it is ==preferable when small sample size== (**say, N<1000**)
	- ==> the probabilities (the [[Topics/Mathematics/Statistics and probabilities/Statistics/p-value|p-value]]) can be computed "exactly"
	- it uses a **hypergeometric distribution** -> eg. $p=\frac{(a+b)!(c+d)!(a+c)!(b+d)!}{N!a!b!c!d}$, $N=a+b+c+d$
- We generally use one-tailed(/sided) tests, but can be a two-tailed test -> ???
- Definitions
	- **Odds ratio** (OR) : measures how far from independence the 2x2 table is. $OR=\frac{ad}{bc}$
	- **Table margins** = totals (see below : $a+c$, $c+d$, ...)
- **Alternatives**
	- Barnard's exact test (1945)
		- a variant : Boschloo's test (1970)
	- Chi-squared test (if N is bigger than 1000)
- it conditions on both margin => ?
	- contrary to Barnard's exact test which is conditioning on only one margin

---
### Example
With this [[Topics/Mathematics/Statistics and probabilities/Statistics/Contingency table|Contingency table]], we look for a "discovery" of dependence between gender & smoking behavior :
$$\begin{array}{|c|c|c|} \hline  & \text{Male} & \text{Female} & \text{total} \newline \hline \text{Smoker} & 15 & 9 & 24 \newline \hline \text{Non-smoker} & 30 & 45 & 75 \newline \hline \text{total} & 45 & 54 & N \newline \hline \end{array}$$
- $OR=2.5$ -> odds of 1st cell (of being a male smoker) is around x2.5 -> it seems to be not entirely gender-independent
- The *two-sided* $p=0.063091$, and if we use ***one-sided*** $p=0.04544$ (when we have prior assumptions ?) -> which is below the "classical" choice of $p=0.05$, so ==we do **reject the null hypothesis==** and we conclude that gender is **dependent** with the fact of smoking. As it's statistically significant (chance might not have produce this).

---
### Python
- in [[___INBOX___/__à trier/SciPy|SciPy]] : `scipy.stats.fisher_exact(crosstab, alternative='two-sided(Default)|less|greater')`
	- Documentation : https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.fisher_exact.html

---
### Resources
StackExchange
- [What does the assumption of the Fisher test that the row and column total should be fixed mean ?](https://stats.stackexchange.com/questions/441139/what-does-the-assumption-of-the-fisher-test-that-the-row-and-column-totals-shou)
- [What does conditioning on the margins of ... means ?](https://stats.stackexchange.com/questions/103876/what-does-conditioning-on-the-margins-of-mean)
- [When is a one-sided test used vs. a two-sided test in Fisher's Exact Test](https://stats.stackexchange.com/questions/325744/when-is-a-one-sided-test-used-versus-a-two-sided-test-in-a-fishers-exact-test)

---
### See also
- [[Topics/Mathematics/Statistics and probabilities/Statistics/Contingency table|Contingency table]]
- **Hypergeometric distribution** -> (see note on [[Topics/Mathematics/Statistics and probabilities/Probability distributions|Probability distributions]])
	- a discrete distribution
	- "sampling without replacement" -> ?
	- uses the [[___INBOX___/__à trier/Binomial coefficient|Binomial coefficient]]
- **Post-hoc test** : when statistical analysis is specified and done after the data is seen
- effect size : ?
- "**The lady tasting tea**" : in the book "*The Design of Experiments*" (**1935**)

---
https://en.wikipedia.org/wiki/Fisher%27s_exact_test
https://fr.wikipedia.org/wiki/Test_exact_de_Fisher

https://fr.wikipedia.org/wiki/The_lady_tasting_tea
https://en.wikipedia.org/wiki/Lady_tasting_tea
