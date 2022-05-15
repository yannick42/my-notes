---
{"dg-publish":true,"permalink":"/topics/machine-learning/machine-learning/","dgHomeLink":true,"dgPassFrontmatter":false}
---


### Toggl recent activity
```toggl
summary PAST 3 DAYS
include projects "AI/ML/DL/RL", "Algorithms", "Technical reading", "Maths", "MOOC", "Python", "Tehnical reading"
SORT DESC
```
```toggl
LIST PAST 5 DAYS
INCLUDE projects "AI/ML/DL/RL", "Algorithms", "Technical reading", "Maths", "MOOC", "Python"
SORT DESC
```

---
### Current topics
```dataview
TABLE 
	category,
	"![progress](https://progress-bar.dev/" + progress + "/)" AS progress,
	difficulty,
	filter(file.tags, (t) => t != "#ml/todo" AND t != "#ml" AND t != "#DIIGO" AND t != "#MEMEX" AND t != "#not_found" AND t != "#task") as tags,
	wip
FROM #ml/todo
WHERE status != "done"
SORT progress DESC
```

---
### News/websites
- https://lastweekin.ai/

### Concepts
- Bayesian learning : [[Topics/Mathematics/Statistics and probabilities/Bayesian inference, analysis ...|Bayesian inference, analysis ...]]

### Models
- [[___INBOX___/__à trier/Linear Models|Linear Models]] (Ridge Regression, LASSO, ElasticNet, ...)
- [[Topics/Machine Learning/Models/Logistic regression|Logistic regression]] for classification
- [[Topics/Machine Learning/Models/Support Vector Machine (1992)|Support Vector Machine (1992)]]
- [[Topics/Machine Learning/Models/Random Forest (1995)|Random Forest (1995)]]
- [[Topics/Machine Learning/Models/Probabilistic Graphical Models|Probabilistic Graphical Models]]

### Books

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">

<div class="markdown-embed-title">



</div>



- [[Topics/Machine Learning/Books/The Elements of Statistical Learning (2009, 2016)|The Elements of Statistical Learning (2009, 2016)]]
- [[Topics/Machine Learning/Books/An Introduction to Statistical Learning (2013, 2021)|An Introduction to Statistical Learning (2013, 2021)]]
- [[Topics/Machine Learning/Books/Hands-on ML with scikit-learn, Keras, and Tensorflow 2 (2017, 2019)|Hands-on ML with scikit-learn, Keras, and Tensorflow 2 (2017, 2019)]]
- [[Topics/Machine Learning/Books/Pattern Recognition and Machine Learning (2006)|Pattern Recognition and Machine Learning (2006)]]


### See also
- [[___INBOX___/__à trier/Books on Data Science|Books on Data Science]]
- [[Topics/Mathematics/Books on Statistics|Books on Statistics]]


</div></div>


### Tasks
- [[___INBOX___/__à trier/Binary classification|Binary classification]]
	- eg. [[Topics/Machine Learning/Concepts/Sentiment analysis|Sentiment analysis]]
