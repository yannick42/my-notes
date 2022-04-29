---
{"dg-publish":true,"dg-permalink":"logreg","permalink":"/logreg/","dgHomeLink":true,"dgPassFrontmatter":false}
---


**Logistic regression**
- aka. logistic model, **logit** model
- It's a [[Topics/Machine Learning/Concepts/Supervised learning|Supervised learning]] algorithm for [[Topics/Machine Learning/Concepts/Classification|Classification]] (==despite its name==)
- **Pros**
	- simple but powerful technique
	- very good performance with linearly separable classes
	- easily interpretable outcome (not a black-box process) => almost "white-box" (?)
- **Cons**
	- Other models can have better predicting performance : (eg.?)
	- The interpretation of the weights **(?)** is not that easy...
- It's **not only** the final classification result => it also gives probabilities
	- "*Knowing that an instance has a 99% probability for a class compared to 51% makes a big difference.*"
- **Binomial** regression = binary outcomes => *pass/fail, win/lose, alive/dead, healthy/sick, ...*
	- binomial = when dependent variable is dichotomous (binary)
	- ==but not only== => it can also be extended to **ordinal** or **multinomial** ([[Topics/Machine Learning/Models/Multinomial logistic regression|Multinomial logistic regression]])
- Special case of the [[___INBOX___/__à trier/Generalized linear models|Generalized linear models]] (**GLM**)
- available in
	- [[Topics/Machine Learning/Tools, Software/sklearn|sklearn]]
	- as a **TensorFlow** module
	- [[Topics/Machine Learning/Tools, Software/Big Data/Apache Spark (2014)|Apache Spark (2014)]] **?**
	- `glm` function in [[Topics/IT-Computing/Programming/R|R]]
- ==Used for== : *medicine, social sciences, insurance, banking, econometry, ...*
- We can use [[Topics/Mathematics/Statistics and probabilities/Maximum likelihood estimation|Maximum likelihood estimation]] to find parameters W & b
- Decision boundary is a straight line[^1]
- Logistic loss is the **log-loss**
	- There is no closed-form solution, but convex so a local minimum is the global minimum, can be found with an optimization method
$$L(\theta)=\sum_{(x,y)\in D}-ylog(y')-(1-y)log(1-y')$$

- **Regularization** is **important**
	- $l_2$ regularization
		- **C** parameter (in sklearn) = inverse of reguralization strengh ($C=1/λ$)
	- [[___INBOX___/__à trier/Early stopping|Early stopping]]

### History
- Verhulst, in the 1830s : [[Topics/Mathematics/Statistics and probabilities/Logistic function|Logistic function]] for population growth models
- Evolved gradually, but logistic regression was developed (or refined) by statistician ==David Cox== in **1958**
- "Multinomial" introduced independently in **1966** by *Cox* and in **1969** by *Thiel*

---
### Applications
- Credit scoring
- Disease prediction
- Fraud detection
- in [[Topics/Machine Learning/Concepts/Natural Language Processing|Natural Language Processing]]
	- Toxic speech detection
	- topic classification for questions to support
	- email sorting / "spam or ham"
	- Sentiment analysis

### Further searches/Questions/What is?/==TODO==
- logits / probits
- link functions (in GLM ?) / log odds
- Adaline / perceptron => ?

### See also
- [[Topics/Machine Learning/Books/Hands-on ML with scikit-learn, Keras, and Tensorflow 2 (2017, 2019)#Logistic regression|Hands-on ML with scikit-learn, Keras, and Tensorflow 2 (2017, 2019)#Logistic regression]]
- **Other** classification algorithms
	- [[Topics/Mathematics/Linear discriminant analysis|Linear discriminant analysis]] - Linear Discriminant Analysis
	- [[Topics/Machine Learning/Models/Decision Trees|Decision Trees]]
	- [[Topics/Machine Learning/Models/Random Forest (1995)|Random Forest (1995)]]

### Flashcards
Which shape has the decision boundary ?::straight lines, plan, hyperplane <!--SR:2021-08-24,18,250-->

---
- **Cross validated (StackExchange) **
	- https://stats.stackexchange.com/questions/43538/what-is-the-difference-between-logistic-regression-and-neural-networks
	- https://stats.stackexchange.com/questions/949/when-is-logistic-regression-solved-in-closed-form
- https://www.kdnuggets.com/2019/01/logistic-regression-concise-technical-overview.html
- **Google ML Crash Course** : https://developers.google.com/machine-learning/crash-course/logistic-regression/model-training
- https://towardsdatascience.com/logistic-regression-and-decision-boundary-eab6e00c1e8
- **Interpretable ML** - https://christophm.github.io/interpretable-ml-book/logistic.html
- sklearn's **C parameter** : https://stackoverflow.com/questions/22851316/what-is-the-inverse-of-regularization-strength-in-logistic-regression-how-shoul
- **[[MNIST|MNIST]]** -> https://dmkothari.github.io/Machine-Learning-Projects/Logistic_Regression_with_MNIST.html

https://www.sciencedirect.com/topics/computer-science/logistic-regression

[^1]: https://stats.stackexchange.com/a/304002/247056
