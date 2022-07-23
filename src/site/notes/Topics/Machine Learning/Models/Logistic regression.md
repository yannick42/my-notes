---
{"dg-publish":true,"dg-permalink":"logreg","permalink":"/logreg/","dgHomeLink":true,"dgPassFrontmatter":false}
---


**Logistic regression**
- aka. logistic model, **logit** model
- it's a [[Topics/Machine Learning/Concepts/Supervised learning|supervised learning]] algorithm for [[Topics/Machine Learning/Concepts/Classification|classification]] (==despite its name==)
- **Pros**
	- simple but powerful technique
	- very good performance with linearly separable classes
	- relatively easy interpretable outcome (not a black-box process) => almost "white-box" (?)
- **Cons**
	- other models can have better predicting performance : (eg.?)
		- because of it's restrictive expressiveness (e.g. interactions must be added manually)
	- the interpretation of the weights $\beta$ is not that easy as it is multiplicative and not additive
		- => https://christophm.github.io/interpretable-ml-book/logistic.html#interpretation-1
- it's **not only** the final classification result => it also gives probabilities
	- "*Knowing that an instance has a 99% probability for a class compared to 51% makes a big difference.*"
- **Binomial** regression = binary outcomes => *pass/fail, win/lose, alive/dead, healthy/sick, Republican/Democrat, un/employed, ...*
	- binomial = when dependent variable is **dichotomous** (binary)
	- ==but not only== => it can also be extended to **ordinal** or **multinomial** (--> [[Topics/Machine Learning/Models/Multinomial logistic regression|Multinomial logistic regression]])
- ==used for== : *medicine, social sciences, insurance, banking, econometrics, ...*
- **decision boundary** is a straight line[^1]
- it uses the [[Topics/Mathematics/Statistics and probabilities/Logistic function|Logistic function]] : $\frac{e^{\beta_0 + \beta_1 X}}{e^{\beta_0 + \beta_1 X} + 1}=\frac{1}{1+e^{-(\beta_0 + \beta_1 X)}}$ to squeeze the output of a linear equation (weighted sum) between 0 and 1 (=> a probability)
- Logistic loss is the **log-loss** (aka. (binary) cross entropy function) (--> see also : [[Topics/Machine Learning/Loss functions/Negative log-likelihood|Negative log-likelihood]])
	- There is **no closed-form solution** to $\frac{\partial L}{\partial \theta}=0$, but this function is [[Topics/Mathematics/Convex optimization|convex]] so a local minimum is the global minimum, can be found with an optimization method (eg. [[Topics/Machine Learning/Optimization methods/Gradient descent|Gradient descent]] for minimization)
$$L(\theta)=-log(likelihood)=\sum_{(x,y)\in D}-ylog(y')-(1-y)log(1-y')$$
with **likelihood** : $\ell(\theta)=\prod\limits_{i, y=1}p(x_i) \prod\limits_{j, y=0}(1-p(x_j))$, assuming each sample is **iid** ($p(x)=y$ above)
- we most commonly use [[Topics/Mathematics/Statistics and probabilities/Maximum likelihood estimation|maximum likelihood estimation]] to find parameters $\beta$ (aka. $\theta_{ML}$)
- It's a **special case of** the [[Topics/Mathematics/Statistics and probabilities/Generalized linear models|Generalized linear models]] (**GLM**)
- **Regularization** is **important**
	- $l_2$ regularization
		- **C** parameter (in [[Topics/Machine Learning/Tools, Software/sklearn|sklearn]]) = inverse of regularization strength ($C=1/λ$), its value can be found with "GridSearch"
	- [[___INBOX___/__à trier/Early stopping|Early stopping]] : stop when no more progress

---
### History
- *Verhulst*, in the **1830s** : [[Topics/Mathematics/Statistics and probabilities/Logistic function|Logistic function]] for population growth models
- Evolved gradually, but logistic regression was *refined* notably by statistician ==David Cox== in **1958**
	- Invented by Berkson (**1944**) and applied in biological sciences (early 20th century)
	- as an alternative to **probit model** in bioassays (fr: essais biologiques)
		- logit was dismissed as inferior, but gained popularity in the 1960s/1970s
- "Multinomial" generalization introduced independently in **1966** by *Cox* and in **1969** by *Thiel*
- => for more historical background : see **The Origins of Logistic Regression** by J.S. Cramer (**2002**)

---
### To do/Question/further searches
- [ ] How to interpret the learned weights $\beta$ ? or the log-odd ?
- [ ] Why is there a limitation when the classes are separable ?!
- [ ] Why a linear decision boundary ?
- **What is ?**
	- [ ] log odds
	- [ ] logits / probits
	- [ ] link functions (in [[Topics/Mathematics/Statistics and probabilities/Generalized linear models|GLM]])
	- [ ] Adaline / perceptron => ?

---
### Packages
- [[Topics/Machine Learning/Tools, Software/sklearn|sklearn]].linear_model.**LogisticRegression** in Python
	- with default solver : **lbfgs** to handle multinomial loss (supported penalty/regularization : $l_2$)
		- → [[Topics/Machine Learning/Optimization methods/BFGS|BFGS]]
- as a [[Topics/Machine Learning/Tools, Software/TensorFlow|TensorFlow]] module
- [[Topics/Machine Learning/Tools, Software/Big Data/Apache Spark (2014)|Apache Spark (2014)]] **?**
- `glm` function in [[Topics/IT-Computing/Programming/R|R]]

---
### Interpretation
- https://stats.stackexchange.com/questions/412668/how-to-interpret-a-negative-coefficient-in-logistic-regression
	- **How to interpret a negative coefficient in logistic regression ?**

---
### Ordinal/Ordered Logistic regression
> aka. **proportional odds logistic regression**
- https://scipython.com/blog/logistic-regression-for-image-classification/
	- dependent variable is ordinal (eg. )
- https://towardsdatascience.com/implementing-and-interpreting-ordinal-logistic-regression-1ee699274cf5

---
### Applications
- Social science
- Credit scoring
- Disease prediction
- Fraud detection
- in [[Topics/Machine Learning/Concepts/Natural Language Processing|Natural Language Processing]]
	- Toxic speech detection
	- topic classification for questions to support
	- email sorting / "spam or ham"
	- Sentiment analysis

---
### See also
- **Textbooks**
	- [[___INBOX___/__à trier/Hands-on ML 2 - Chapter 4 - Training models#Logistic regression aka Logit regression|Hands-on ML 2 - Chapter 4 - Training models#Logistic regression aka Logit regression]]
	- [[Topics/Machine Learning/Books/An Introduction to Statistical Learning/An Introduction to Statistical Learning (2013, 2021)#4 3 - The Logistic Model|An Introduction to Statistical Learning (2013, 2021)#4 3 - The Logistic Model]] (MLE, Likelihood function, ...)
- **Other** classification algorithms
	- [[Topics/Mathematics/Linear discriminant analysis|Linear discriminant analysis]] - Linear Discriminant Analysis
	- [[Topics/Machine Learning/Models/Decision Trees|Decision Trees]]
	- [[Topics/Machine Learning/Models/Random Forest (1995)|Random Forest (1995)]]

### Flashcards
Which shape has the decision boundary ?::straight lines, plan, hyperplane <!--SR:2021-08-24,18,250-->

---
https://en.wikipedia.org/wiki/Logistic_regression

- **Image identification** : https://scipython.com/blog/logistic-regression-for-image-classification/
- **Cross validated (StackExchange)**
	- https://stats.stackexchange.com/questions/43538/what-is-the-difference-between-logistic-regression-and-neural-networks
	- https://stats.stackexchange.com/questions/949/when-is-logistic-regression-solved-in-closed-form
- https://www.kdnuggets.com/2019/01/logistic-regression-concise-technical-overview.html
- **Google ML Crash Course** : https://developers.google.com/machine-learning/crash-course/logistic-regression/model-training
- https://towardsdatascience.com/logistic-regression-and-decision-boundary-eab6e00c1e8
- **Interpretable ML** - https://christophm.github.io/interpretable-ml-book/logistic.html
- sklearn's **C parameter** : https://stackoverflow.com/questions/22851316/what-is-the-inverse-of-regularization-strength-in-logistic-regression-how-shoul
- **[[MNIST|MNIST]]** -> https://dmkothari.github.io/Machine-Learning-Projects/Logistic_Regression_with_MNIST.html
- sklearn documentation
	- https://scikit-learn.org/stable/modules/generated/sklearn.metrics.log_loss.html
- [ ] **TODO** : https://chrisyeh96.github.io/2018/06/11/logistic-regression.html - lots of maths

https://www.sciencedirect.com/topics/computer-science/logistic-regression

[^1]: https://stats.stackexchange.com/a/304002/247056
