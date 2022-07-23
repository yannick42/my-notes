---
{"dg-publish":true,"dg-permalink":"rl","permalink":"/rl/","dgHomeLink":true,"dgPassFrontmatter":false}
---


```ad-warning
title:
🚧 **Page in construction**
```
---

> 
> Learning with (often delayed) rewards and penalties (negative rewards)
> - the study of learning intelligent behavior

### Definitions
- **policy $\pi(s)$** : map **states** to **actions**
- **value $V(s)$** : expected long-term **return** (as opposed to R : short-term reward)
- **Q-value (action-value) $Q(s,a)$** : similar to $V(s)$ but with $a$ (an action)
	- maps ==state action pairs== to **rewards**
- **policy-based** : better for continuous and stochastic environment, faster convergence
	- no need of Q-value as a middleman
	- Q-Learning, DQN, Double dueling Q Networks, ...
- **value-based** : more "sample efficient" (?) and steady
	- requires the transition model ? => **model-based ?**
- **[[___INBOX___/__à trier/Model-free (RL)|Model-free (RL)]]** : doesn't use generated predictions from the (state-)transition probability distribution or the reward function, of the MDP. Those are "unknown".
	- SARSA, Q-Learning, DQN, actor-critic (A3C, ...), ...
	- Generally superior, if you don't have an accurate model as part of the problem definition => ??
- **model-based** : 
	- DP (Policy Iteration, Value Iteration)
- **on-policy** : 
- [[Topics/Machine Learning/Models/RL & DRL/Policy Gradient|Policy Gradient]] : by gradient descent
- [[Topics/Machine Learning/_à trier/Temporal Difference learning|Temporal Difference learning]]
	- model-free
- **look-up table** representation / **tabular methods** : for small and discrete space (greatly restricts real applications...)
	- must be learned for every states, to learn an optimal policy...
- **MDP/Markovian assumption** => ?
- [[___INBOX___/__à trier/Bellman equation|Bellman equation]]

---
### Algorithms
- "Classic" **RL**
	- [[Topics/Machine Learning/Models/RL & DRL/Q-Learning (1989)|Q-Learning (1989)]] : 
	- [[Topics/Machine Learning/Models/RL & DRL/REINFORCE (1992)|REINFORCE (1992)]] - policy gradient method
	- [[Topics/Machine Learning/Models/RL & DRL/Actor-Critic|Actor-Critic]]
- **Deep RL** (DRL)
	- [[Topics/Machine Learning/Models/RL & DRL/DQN (2013)|DQN (2013)]]
	- [[Topics/IT-Computing/Computer Science/Data structures/DDPG (2015)|DDPG (2015)]]
	- [[Topics/Machine Learning/Models/RL & DRL/TRPO (2015)|TRPO (2015)]]
	- [[Topics/Machine Learning/Models/RL & DRL/PPO (2017)|PPO (2017)]]
	- [[Topics/Machine Learning/Models/RL & DRL/PPG (2020)|PPG (2020)]]
	- **SAC** : soft actor-critic

### Tabular methods [^1]
- Dynamic Programming :
- Monte Carlo updates ?
- [[Topics/Machine Learning/_à trier/Temporal Difference learning|Temporal difference]] (model-free, can learn online : no need to wait the end of the "episode")
	- $TD(0)$ : look ahead only 1 step
	- **SARSA** : 
	- Q-Learning ?
	- Double Q-Learning ?

---
### Books
-  by [[Topics/Machine Learning/People/Richard Sutton|Richard Sutton]] & Andrew Barto : **Reinforcement Learning : An Introduction** (==2018==, 2nd edition)
	- http://incompleteideas.net/book/the-book-2nd.html
		- http://incompleteideas.net/book/RLbook2020.pdf (***==#freePDF==***)
- **Chapter 18** of [[Topics/Machine Learning/Books/Hands-on ML with scikit-learn, Keras, and Tensorflow 2 (2017, 2019)|Hands-on ML with scikit-learn, Keras, and Tensorflow 2 (2017, 2019)]] with [[Topics/Machine Learning/Concepts/Deep Reinforcement Learning|Deep Reinforcement Learning]]

---
### Courses/MOOC
- **CS188** (Spring **2014**) http://ai.berkeley.edu/lecture_videos.html
	- UC Berkeley's introductory artificial intelligence course
- [[___INBOX___/__à trier/UCL Course on RL (2015)|UCL Course on RL (2015)]] by [[Topics/Machine Learning/People/David Silver|David Silver]]
- Deep RL Bootcamp (August **2017**)
	- https://sites.google.com/view/deep-rl-bootcamp/lectures
- https://github.com/huggingface/deep-rl-class by [[___INBOX___/__à trier/Hugging Face|Hugging Face]]

---
### Question
- *==What's the difference between model-free & model-based RL ?==* https://ai.stackexchange.com/questions/4456/whats-the-difference-between-model-free-and-model-based-reinforcement-learning/6733

---
### Articles/Blogs
- https://lilianweng.github.io/lil-log/2018/02/19/a-long-peek-into-reinforcement-learning.html - Article with lots of algorithms explained (and maths)
- https://karpathy.github.io/2016/05/31/rl/ by [[Topics/Machine Learning/People/Andrej Karpathy|Andrej Karpathy]]
- http://www.wildml.com/2016/10/learning-reinforcement-learning/ (resources)
- https://en.wikipedia.org/wiki/Reinforcement_learning


[^1]: https://towardsdatascience.com/summary-of-tabular-methods-in-reinforcement-learning-39d653e904af