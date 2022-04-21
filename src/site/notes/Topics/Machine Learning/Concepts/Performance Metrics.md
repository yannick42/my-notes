---
{"dg-publish":true,"permalink":"/topics/machine-learning/concepts/performance-metrics/","dgHomeLink":true,"dgPassFrontmatter":false}
---


#### Performance Metrics in Classification
- **accuracy** : ratio (%) of $\frac{TP+TN}{TP+FP+TN+FN}$ (generally not the preferred performance measure)
- accuracy of positive predictions = **precision** = $\frac{TP}{TP+FP}$
- **recall** = sensitivity = TPR (true positive rate) = $\frac{TP}{TP+FN}$
- The **F1 score** is the harmonic mean of precision and recall. It's a single metric that combine precision and recall. -> $2\frac{precision\times recall}{precision+recall}$
	- this score must be favored over accuracy when imbalanced class situation
- "***Unfortunately, you can’t have it both ways: increasing precision reduces recall, and vice versa. This is called the precision/recall trade-off.***"
- **TIP** : =="If someone says, “Let’s reach 99% precision,” you should ask, “At what recall?”"==
- The ROC Curve
	- "**R**eceiver **O**perating **C**haracteristic"
	- used in [[___INBOX___/__à trier/Binary classification|Binary classification]]
	- Instead of plotting "Precision *vs* Recall", its ""**Recall** *vs* **False Positive Rate**" (FPR)
		- **Sensitivity** (=recall) vs. **1 - Specificity**
		- **Specificity** -> $\frac{TN}{TN+FP}$ -> proportion of correctly identified negative elements
	- A way to compare models is to calculate "area under the curve" of ROC => ==ROC AUC score==

