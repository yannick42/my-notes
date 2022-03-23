---
{"dg-publish":true,"permalink":"/inbox/a-trier/gmm/"}
---

- A set of models
	- can be : diagonal, spherical, tied and full covariance matrices
- Finite number of Gaussians with unknown parameters
- Generalize k-means clustering with informations about covariance structure of the data
- Use
	- [[___INBOX___/__à trier/Expectation-maximization algorithm|Expectation-maximization algorithm]]
	- **Variational inference** algorithms that add regularization by integrating information about the prior distributions ( `BayesianGaussianMixture` in sklearn)

### Coding
- `sklearn.mixture` : to sample from them, or estimate them from data
	- => [Gaussian Mixture Models (sklearn docs)](https://scikit-learn.org/stable/modules/mixture.html)

### See also
- ?
