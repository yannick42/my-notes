---
{"dg-publish":true,"dg-permalink":"isl","permalink":"/isl/","dgHomeLink":true,"dgPassFrontmatter":false}
---


> 2013, **2021** (2nd ed. => [[ISLRv2.pdf]])

---
### To do next
- [ ] (accountability/"peer-pressure")
- [ ] Watch : http://fs2.american.edu/alberto/www/analytics/ISLRLectures.html
- [ ] a MOOC exists here : https://www.edx.org/course/statistical-learning

---
| Section                                                                                                                                                                                                                                                                                                         | Task                                                                                 | Tasks.completed | Status | Due Date | Priority | Keyword |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ | --------------- | ------ | -------- | -------- | ------- |
| [[Topics/Machine Learning/Books/An Introduction to Statistical Learning/An Introduction to Statistical Learning (2013, 2021)#To do next\|An Introduction to Statistical Learning (2013, 2021) > To do next]]                                                                                                 | (accountability/"peer-pressure")                                                     | false           | 🔴     | \-       | \-       | \-      |
| [[Topics/Machine Learning/Books/An Introduction to Statistical Learning/An Introduction to Statistical Learning (2013, 2021)#To do next\|An Introduction to Statistical Learning (2013, 2021) > To do next]]                                                                                                 | Watch : http://fs2.american.edu/alberto/www/analytics/ISLRLectures.html              | false           | 🔴     | \-       | \-       | \-      |
| [[Topics/Machine Learning/Books/An Introduction to Statistical Learning/An Introduction to Statistical Learning (2013, 2021)#To do next\|An Introduction to Statistical Learning (2013, 2021) > To do next]]                                                                                                 | a MOOC exists here : https://www.edx.org/course/statistical-learning                 | false           | 🔴     | \-       | \-       | \-      |
| [[Topics/Machine Learning/Books/An Introduction to Statistical Learning/An Introduction to Statistical Learning (2013, 2021)#QUESTIONS\|An Introduction to Statistical Learning (2013, 2021) > QUESTIONS]]                                                                                                   | What's the difference between **statistical learning** & **statistical inference** ? | true            | 🟢     | \-       | \-       | \-      |
| [[Topics/Machine Learning/Books/An Introduction to Statistical Learning/An Introduction to Statistical Learning - Chapter 4 - Classification#4 4 - Generative Models for classification\|An Introduction to Statistical Learning - Chapter 4 - Classification > 4 4 - Generative Models for classification]] | Test LDA/QDA/LogReg/… on MNIST ?                                                     | false           | 🔴     | \-       | \-       | \-      |
| [[Topics/Machine Learning/Books/An Introduction to Statistical Learning/An introduction to Statistical Learning - Chapter 3 - Linear Regression#Chapter 3 - Linear Regression\|An introduction to Statistical Learning - Chapter 3 - Linear Regression > Chapter 3 - Linear Regression]]                     | ==TODO== #ml/MSG/todo                                                                | false           | 🔴     | \-       | \-       | \-      |
| [[Topics/Machine Learning/Books/An Introduction to Statistical Learning/An Introduction to Statistical Learning - Chapter 4 - Classification#4 3 - The Logistic Model\|An Introduction to Statistical Learning - Chapter 4 - Classification > 4 3 - The Logistic Model]]                                     | What the use of **log-odds** ?                                                       | false           | 🔴     | \-       | 🟥       | \-      |


---
- "An Introduction to Statistical Learning with applications in [[Topics/IT-Computing/Programming/R|R]]"
	- aka. **ISL**
	- website : https://www.statlearning.com/
	- by Gareth James, Daniela Witten, [[Topics/Mathematics/People/Trevor Hastie|Trevor Hastie]] & [[Topics/Mathematics/People/Robert Tibshirani|Robert Tibshirani]]
		- some of them also wrote : [[Topics/Machine Learning/Books/The Elements of Statistical Learning (2009, 2016)|The Elements of Statistical Learning (2009, 2016)]], first published in **2001**
- broad and **less technical** treatment of topic (than the **ESL**)
- ==audience==
	- appropriate for **advanced undergraduates** or **master’s students** in Statistics or related quantitative fields, or for individuals in other disciplines who wish to use statistical learning tools to analyze their data
	- We expect that **the reader will have had at least one elementary course in statistics**
	- The mathematical level of this book is **modest**, and a detailed knowledge of matrix operations is not required.
- textbook of a course **spanning two semesters**
- Youtube playlists of chapters : https://www.youtube.com/channel/UCB2p-jaoolkv0h22m4I9l9Q/playlists

---
- [[Statistical learning|Statistical learning]] : making sense of complex datasets...

---
### QUESTIONS
- [x] What's the difference between **statistical learning** & **statistical inference** ?
	- => **Inference** : is to find/choose a "configuration" based on a single input, **Learning** : to extract statistical patterns and predict on unseen data
	- https://stats.stackexchange.com/questions/205253/what-is-the-difference-between-learning-and-inference

---
### Chapter 1 : Introduction

#### A brief history of  Statistical Learning
- in the beginning of **19th century** : [[___INBOX___/__à trier/Least-squares method|Least-squares]]
- [[Topics/Mathematics/Linear discriminant analysis|Linear discriminant analysis]] is proposed in **1936**
- [[Topics/Machine Learning/Models/Neural Networks|Neural Networks]] in the **1980s**
- [[Topics/Machine Learning/Models/Support Vector Machine (1992)|SVM]] arose in the **1990s**

---
- [[Topics/Machine Learning/Books/The Elements of Statistical Learning (2009, 2016)|The Elements of Statistical Learning (2009, 2016)]] was first published in **2001**, important reference for the fundamentals of statistical learning (comprehensive and detailed). Companion for professionals (==with **graduate degrees in statistics, machine learning**, or related fields==) to understand technical details.
- **ISL** is based on ==4 premises==
	- "(...methods) **relevant and useful** in a wide range of academic and non-academic disciplines"
	- "Statistical learning **should not be viewed as** a series of **black boxes**"
	- "we have **minimized discussion of technical details** related to fitting procedures and theoretical properties"
	- "We presume that ==the reader is interested== in **applying statistical learning methods to real-world problems**."
→ `less technical, more accessible`

---
## Chapters
- [[Topics/Machine Learning/Books/An Introduction to Statistical Learning/An Introduction to Statistical Learning - Chapter 2 - Statistical Learning|Chapter 2 - Statistical Learning]]
	- Regression vs Classification
	- [[Topics/Mathematics/Statistics and probabilities/Statistics/Bias-Variance trade-off|Bias-Variance trade-off]]
	- KNN (non parametric)

---
### Chapter 3 - Linear Regression
- <u>Topics</u>
	- simple/multiple [[___INBOX___/__à trier/Linear regression|linear regression]]
	- extensions of the linear model
	- comparison with KNN (?)

- [[Topics/Machine Learning/Books/An Introduction to Statistical Learning/An Introduction to Statistical Learning - Chapter 2 - Statistical Learning|An Introduction to Statistical Learning - Chapter 2 - Statistical Learning]]

---
### Chapter 4 - Classification
- [[Topics/Machine Learning/Concepts/Classification|Classification]]
	- existing "classifiers"
		- [[Topics/Machine Learning/Models/Logistic regression|Logistic regression]]
		- Generative models ?
			- [[Topics/Mathematics/Linear discriminant analysis|Linear discriminant analysis]]
			- Quadratic discriminant analysis
			- [[___INBOX___/__à trier/Naive Bayes|Naive Bayes]]
		- [[Topics/Machine Learning/Models/K-Nearest Neighbors|K-Nearest Neighbors]]
	[[Topics/Mathematics/Statistics and probabilities/Generalized linear models|Generalized linear models]] (Poisson regression)

→ [[Topics/Machine Learning/Books/An Introduction to Statistical Learning/An Introduction to Statistical Learning - Chapter 4 - Classification|An Introduction to Statistical Learning - Chapter 4 - Classification]]

---
### Chapter 5 - Resampling methods
- Cross validation (CV)
	- k-fold CV : ?

==TODO==

#### 5.2 - The Bootstrap (p. 209 -> 212)
- widely applicable, extremely powerful approach
- it can be used to quantify the **uncertainty** of a statistical method or estimator
	- eg. by **estimating the standard error** of a linear regression fit

==TODO==

---
### Chapter 6 - 
- [[Topics/Machine Learning/Techniques/Ridge regression|Ridge regression]]
- [[Lasso regression|Lasso regression]]
- principal components regression

---
### Chapter 7 - Moving beyond linearity
- **Polynomial regression**
	- by raising the original predictors to a power. Eg. *cubic regression* ($X,X^2,X^3$), …
- Step functions : 
- [[Generalized additive model|GAM]]

---
### Chapter 8 - Tree-based methods
- [[Topics/Machine Learning/Models/Decision Trees|Decision Trees]]
- [[Topics/Machine Learning/Models/Random Forest (1995)|Random Forest (1995)]]
- Bagging, Boosting, …

---
### Chapter 9 - Support Vector Machine
-> see [[Topics/Machine Learning/Models/Support Vector Machine (1992)|SVM]] note

---
### Chapter 10 - Deep Learning
- CNN
- RNN
- 

---
- [[Topics/Machine Learning/Books/An Introduction to Statistical Learning/An Introduction to Statistical Learning - Chapter 11 - Survival analysis & Censored data|Chapter 11 - Survival analysis & Censored data]]

---
### Chapter 12 : Unsupervised Learning
- [[Topics/Mathematics/Statistics and probabilities/PCA (1901)|PCA (1901)]]
- Clustering methods : [[K-Means|K-Means]], hierarchical clustering, …

---
- [[Topics/Machine Learning/Books/An Introduction to Statistical Learning/An Introduction to Statistical Learning - Chapter 13 - Multiple testing|Chapter 13 - Multiple testing]]
