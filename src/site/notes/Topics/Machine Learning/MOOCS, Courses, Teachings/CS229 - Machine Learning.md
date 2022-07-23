---
{"dg-publish":true,"permalink":"/topics/machine-learning/moocs-courses-teachings/cs-229-machine-learning/","dgHomeLink":true,"dgPassFrontmatter":false}
---


**CS229 - Machine Learning** at [[Topics/Machine Learning/Academia, universities/Stanford University|Stanford University]]
- a **broad introduction** to [[Topics/Machine Learning/Machine Learning|Machine Learning]] and statistical pattern recognition.

> https://cs229.stanford.edu/
> **Syllabus** : http://cs229.stanford.edu/syllabus.html
> https://see.stanford.edu/Course/CS229
--> [Youtube Playlist (20 videos)](https://www.youtube.com/playlist?list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU)

### Prerequisites
- **==basic probability theory==** : **Stat 116** (sufficient but not necessary)
	- **Probability spaces** as models for phenomena with statistical regularity. **Discrete spaces** (binomial, hypergeometric, Poisson). **Continuous spaces** (normal, exponential) and densities. [[___INBOX___/__à trier/Random variables|Random variables]], expectation, independence, [[___INBOX___/__à trier/Conditional probability|conditional probability]]. Introduction to **the laws of large numbers** and **[[___INBOX___/__à trier/Central limit theorem|central limit theorem]]**
- **basic linear algebra** :
	- Math 51
	- Math 103
	- Math 113 or CS 205 (would be much more than necessary)

---
### Content/Lectures
> 2 or 3 lectures per week => `September 21th to December 3nd` (2 months & 10 days)
- **Lecture 2**
	- [[Topics/Machine Learning/Concepts/Supervised learning|Supervised learning]]
- **Lecture 3**
	- Weighted Least-Squares
	- [[Topics/Machine Learning/Models/Logistic regression|Logistic regression]]
	- [[Topics/Mathematics/Calculus/Newton’s method|Newton’s method]]
- **Lecture 4**
	- Dataset split
	- [[Topics/Mathematics/Statistics and probabilities/Exponential family|Exponential family]] at **==14:28==**
		- exponential tilting => ?
		- example with Bernoulli & univariate Gaussian (fixed variance)
	- **GLM** (generalized linear models) at **==36:22==**
- **Lecture 5**
	- Gaussian discriminant analysis - **GDA**
	- [[___INBOX___/__à trier/Naive Bayes|Naive Bayes]]
- **Lecture 6**
	- Naive Bayes & Laplace smoothing
- **Lecture 7**
	- Kernels & [[Topics/Machine Learning/Models/Support Vector Machine (1992)|SVM]]
- **Lecture 8**
	- [[Topics/Machine Learning/Models/Neural Networks|Neural Networks]]
- **Lecture 9**
	- [[Topics/Machine Learning/Concepts/Basics/Backpropagation (1986)|Backpropagation (1986)]]
- **Lecture 10**
	- Bias - Variance
	- Regularization
	- Feature / Model selection
- **Lecture 11**
	- [[Topics/Machine Learning/Models/Decision Trees|Decision Trees]]
	- [[Topics/Machine Learning/Boosting|Boosting]]
- **Lecture 12**
	- [[K-Means|K-Means]]
	- GMM (non EM)
	- [[___INBOX___/__à trier/Expectation-maximization algorithm|EM algorithm]]
	- [[Factor Analysis|Factor Analysis]]
		- https://en.wikipedia.org/wiki/Factor_analysis
- **Lecture 13**
	- [[___INBOX___/__à trier/Expectation-maximization algorithm|EM algorithm]]
	- [[___INBOX___/__à trier/GMM|GMM]]
- **Lecture 14**
	- [[Topics/Mathematics/Statistics and probabilities/PCA (1901)|PCA (1901)]]
	- Types of learning
- **Lecture 15**
	- ML advices
- **Lecture 16**
	- [[Topics/Machine Learning/Concepts/Unsupervised learning|Unsupervised learning]] & [[Topics/Machine Learning/Concepts/Reinforcement Learning|Reinforcement Learning]]
- **Lecture 17**
	- [[___INBOX___/__à trier/Value-based methods (RL)|Value-based methods (RL)]]
		- value iteration
	- policy iteration
- **Lecture 18**
	- Model-based RL, value function approximator
- **Lecture 19&20**
	- Fairness, algorithmic bias, explainability, privacy

---
- Une version [[Topics/Machine Learning/MOOCS, Courses, Teachings/Coursera|Coursera]] existe : https://www.coursera.org/learn/machine-learning#syllabus
	- 4.9 stars / 4.6M students

---
#### Lecture 15 (Autumn 2018) - EM algorithm & Factor Analysis
> https://www.youtube.com/watch?v=tw6cmL5STuY (**1h20**)
- ==Outline==
	- how to monitor if [[___INBOX___/__à trier/Expectation-maximization algorithm|Expectation-maximization algorithm]] is converging
	- EM on [[___INBOX___/__à trier/GMM|Gaussian Mixture Model]]
	- [[Factor Analysis|Factor Analysis]] model
		- high dimensional (even if small number of training example)
- **Recap** on EM on a multinomial with $j$ Gaussians (GMM)
	- already seen last lecture …
	- E-step
	- M-step : maximize by taken the derivative wrt. $\mu$ then set to 0 …
		- to get $\mu_j$
		- idem for $\Sigma$
		- permit to update …
- **Coordinate ascent** algorithm (maximize wrt. to $Q$ in E-step then $\theta$ in M-step)
- GMM used if $m>>n$ or else "Factor analysis" (?)
- **Factor Analysis**
	- $x=\Lambda z + \mu + \epsilon$
	- $z = N(0, I)$
