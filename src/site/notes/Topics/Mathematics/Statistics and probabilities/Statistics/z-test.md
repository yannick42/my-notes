---
{"dg-publish":true,"permalink":"/topics/mathematics/statistics-and-probabilities/statistics/z-test/","dgHomeLink":true,"dgPassFrontmatter":false}
---


**z-test**
- used in [[Topics/Mathematics/Statistics and probabilities/Statistics/statistical tests|statistical tests]] for [[Topics/Mathematics/Statistics and probabilities/Statistics/Hypothesis testing|hypothesis testing]]
- it dates from the 19th century ?
- when distribution of the data is **normal** and independent (with a mean & a variance/standard deviation)
- used when the sample is at minimum **more than 30**, or else use Student's [[___INBOX___/__à trier/t-test|t-test]]
- used in **z tests** (a general class of tests statistic which use the normal distribution)
- ==the z-test is **rarely used in practice**==, as the population deviation $\sigma$ is difficult to determine => is it mandatory ?
- one tailed / two tailed "versions" :
	- to test whether the mean is greater or less than $\mu_0$ / or different from $\mu_0$
- z statistic = z-score ?
- z-distribution = normal distribution
- the value of $z$ correspond to a $p$-value (or an other approach to get **a critical value**)

### Z-score
- aka. standard score, or z-statistic (?)
- measures how many standard deviation above/below the population mean a **raw score** is
- to calculate it we must know the mean and the population standard deviation $\sigma$
- *==formulas==*
	- one sample : $z_i=\frac{x_i-\overline{x}}{s}$
	- **single sample z-score** : to check the sample is drawn from a population **with known mean & variance**
		- $z=\frac{M-\mu}{\sqrt{\sigma^2/n}}$, $M$ : the sample mean, $n$ : sample size, $\sigma$ : population std
		- it is a "location test" (?)
	- **two sample z-score**
		- appropriate to **compare 2 sample's means** => and see if it's possible they comes from the same population or if there is a statistically significant difference
		- but rarely used as both $\sigma$ are not often known => use sample standard deviation or t-distribution (?)
- **z-table** : to convert between z-score and a %

![Pasted image 20220212111032.png](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAjoAAAGMCAYAAADTMwg1AAAgAElEQVR4nO3d0bniOLb//Z/fdy47gVNpSPeTQFcCJwApgBNAVwXQAVhpdCcw91YAk8BUAnPv/4UsI4wNBsxGNt9PP/tRgcF47wYhLy9pNX3f9wIAADig/+/dBwAAAPAqDHQAAMBhMdABAACHxUAHAAAcFgMdAABwWAx0AADAYTHQAQAAh8VABwAAHBYDHQAAcFgMdAAAwGEx0AEAAIfFQAcAABwWAx0AAHBYDHQAAMBhMdABcJW1Vk3TXPwAwB4w0AEwy3sva60kyTkjSTLGyDkjY4yaplEI4Z2HCAA3NX3f9+8+CAD1iDHKey9JMkZyzskYyfsgKaptO8UYFWMcBjpGzjk559563AAwh4gOgFEIQdZaGSO1rVPbtjLGSDLDI8rIjlPXdXLOKIQwDo4AoCYMdABI0jhYOR/gxGFrVNu2RdTmdH+K5phxkARsJno1jVWItx/6pfvCrjDQ2UAMOVnzpz7mM0SncSghxHGQc34J6jKSM3d/iu60kkRk51Cigp0kovuFD330appGs5uvbXv4mMr+Nupn06ix4XP6YKz2EQOd6M8/qDbE5z54Z8+N+ttHmbZT3/8hs+kH+hnDB//9B4LKpZwcOxnkxLtbY4za1nEZ6zCifjZWPv5Q1/fq+15918rEOD+YMK36vldrJMUgW/aD5banGRlnJP04nWjFoB+SjDPa5CVwKIcf6MRgZYNR2xUfVOm5D9615276gQZez9rpIEc6j9hETSM4S9vzYOeUqIzdGgYPrvvjNHgwTl3nZIYTKRviENH+qThGeaOC94rSKfIyiQCfnXzaoDgMjM7uu3JoxjgZpUiklAbrkpEzZhxkXd1XeTyTQdn5ifEHRekP7PADnSTK50+YcWqdmVx6uQzP+qgxcnPxpi+eG73VD6W28VHTSzqrP9BLrzW3j+l9d34YL587Dfueh4b54B9XSjw2xSWpuYiNWbh/fnvO2fHeD19A2KM8eLh2zha9lb2IGhu5Np1Quq5Pke7yOZOTz84pDaDGqJGTor9+WdwYOSMpRkVFxRAlk2YH3r2vi2PLEaxOrfkx8/thbw4/0DGu1Q9JCvZ8EFOIwcvH4YOXIz4F1w0fmDJUmvffdilk2nbqJ2GcRz7Q09ea3ccTH8b5D7L0e5vOhGKUFKNClEz7+1Ovhbrly0tt6xZzbx5t05R0Q1Rnx3Iy+tXxRtulvmwymLkqFoMSScadIkT5ZG7F0cm1buizUn/lWjccw737mhybfgwno7aCFARs4fADHcnoj3JgoVO4czT54C3t5+6rUQ9/oIvXmtnHUx/GheemAWFUiFExBkX9GCJffPCPKISgEEIxyLk/J+dW23Xt+DrYIeP0Q1KwRRQ3BtlnE35NcVIlKYag4K1+aDih6laux2Rc6rN86q+GNS2HKPud+yqPTUWqQ99fnMBifw4/0ImhiJgMH9wLxkjx1/YvvsUHemYfT30YF59r9LsbjjFEyf0+5DLxwT+iEMLkktVr2q5ruYS1W0Z/9J1+jCc6jRrrFc2Kk77h0tLl7CjJuE6di/I2Tw4ZTuDy66yOwgx9Viz6K63c1zBI8nb4nRaO7eosM+xHf3Bda3pJpx/T9l3f933nesn0bbrR/ygfI/Wuy4/J/257c3b/+XNNujHZ1vedm7z2sM/VrzW3j+l9Uq/84NNvfvE73Xzu8Lrl8V+8fn785PfEfrRt20vqu67t+77t+757aeuc6Y0xX/b7AUCJEhBT0auxUW3XjaFQ4EiaphkW//uaN3iMUdb6yYKDAPA1Dn/papVyJpQNMm3LIAeH5L0fLlnle7bPzZm2+RJZCIFLWAC+HBEd4EOkyMrcmjnlOjmzz3xye2KtlXNEdQB8LSI6wIdICcgaBhqPr5Nz//bEGMeKyQC+HBEd4APkaE7ft1oTfXnVMXgfhgUFieoA+BpEdKr0RQXqnijMORYyZerlLnjvh8HFtRWQX9saY8Yq5+Tq7EXdxTLph7AGA50KxeDTWjude9O5923GdWkdoMAigrXLg4rzWVavXT/n2orJklhEcCdq74voh7AGA53qpLotpv29yo7ljGnVOQ0rk6JWaVARX7YC8n2txgrnRHVqt5O+iH4INzDQqU2uM1XWo7hS8LN40HJhzhdW800lKU4rN6M+qdRDO9x6TySnzAsyZljwmzdN3Wb6ovO+YOmSVlHmprisdFmceFJMuei7LiqjX7w2/RDWY6BTpfkl1lMl4GFJdh9P16eHZdSXCnOal1bzNTI3Cv/hfdKU7q9dN+d2ayj4uRvnfZFph+LCQ9mYtnVnBZNtiOe1poaSMfPFiSfFlKOXLzqmsjI6/RCewUBnh/5nLPDZjfWnOmeWC3OuKiS6gKKeu3XKzSmTkOfa+OXb27ZNVacZ7OxP9LI+yg2rx8/1Q6aoj2VD1GJx4nzfUBurjMicVUanH8ITGOhU6fqZya+ohUrr84U5X1vNNyo+UtkdLxdCVIxrcnPesf2Uq4OaTfqioXq5aTst1vYdI8jpMTHE5eLExX3L/Zroh/CcL66thZu6vjVFkdC+Hwt+alKcc/7pM4U5rxYSvVHYtL9eQLRzN44HbyOZ3jnXp+Ka9f10XdsbY/qu491Tp2lflG7f6ovO+4srBY6n+xv3NSmUPLtf+iGsx4KBFYrByvrv6vo/0hlK9GpskOv65bOod6j1uKAQgrz36rq2iOjU16aVkk2RLI2aXPRFNaIfwg0MdKoU9bOx+mHatH5FhR/k1AFGyXWTEDJqYK2XMbH6AUQakAXRDdVq0he9+3Am6IewBgMd4GByuYcUzZFqiNwstelY06rNtQ/KAOwTAx3gYNLloPqjOZn3XjGmmVhmMRsVAB7DrCvgQGIsZ1pJdaybc61Ns6/ycQPA1ojoAAdyftmqHOxci5S8e7vkfSoJ0XXd1ccBwL2I6AAH4r2XMdOVkGtcR+e8zcdLVAfA1ojoAAcRY5T3Xm3rdpnr0jRWbduOFc4BYAtEdICDqKtK+f2tc9S/OoZJsc6iQPD0cWfFP4fyDrncVVnLrywOCtyLiM4nGdbjyRbX5bn1uBjSOi0VreuDHBExu42I5KnmXdftMiL1DO/9ikym22KU/vzzf/XPf/5zi8O63L9v5E2nzl050qFMRK6FFX0zFOScLjqY1uj5q53Z39DHKG+rcC0x7Mc/3n0A+CpRP4caNZ0bqglbKzN0Rmsflzqt9Mit+5u9dPY1ytGc01+vjnVy7mlTblGK6uxlavwWTjPOjOKTA7wYg/79b7Pxe39YNFCSTDtULr/OXfQrfynGP2ZrWUVv1fj0bzMZ9ETvFUw3FvW8Nr4CljDQ+RQx6IckN/Q06Yw56CIYfONxpu3VO39/FfRbh1d9Z1+3NKVcRTTH7LJtWyfvP/Ty1VC48rldbDgSGKIqUWkA0i+MMsbViZUHKk6u2IcPUlm5vDha/dH3+iM/1Dey3sqbXq1x6rq0wre3TXqAa6tbmRn7QI7Ox0qVfm/Pcln7uI2Mnf3jP5922UNKEZ3zS1bvz7l5rE3vNXJ1HvX1eSzGdWNF8bNLUONA6ceq8hGmfP9Gr2a4PN73vfrOScHKhq///bB/DHQ+VkxnajcHBWsfV5PP6gxDCDLGyJ2dcZeRkji5Xe/2PDWeaeYVME5d36vvO333Q2KwnYkCz4jBqrFe0bTnuTnRj8nJcTJwiSEon1jNHAzRHDyMgc6nME4/JIWhY8mXiYx01vlcfRyqlAc6y+vVLN1f4/Z0+Y2IzqNe8UlNl5j6vldnvPytqEr046UsRS87zJqai8ZEf5pZZYNRm3N7TKsUxBlmXFmv6G4kQQMLyNH5GEZ/dE4/rFUzfIe4rk+dSlz5OJ0nIwfbKFRZNbi243m9UzRn763OkpL3OoPsXeIm6fzLTNvr5trVplXfLyWTF9tMp/7K/17T9lrcDXAHBjqfZKkDmt5/paPaQ+fz6s6+JqmAZ+n9s6eebfNl0k8Z6JxWhQ7Pv2u54gdcYB0dVCKeZng8u6eYZu98wpdkqvwd1XWVjz7v9Glr6vzrX//abF+fNNsQWIOBDqpBZ3+fXMDzfFD3/ojMVq21Kffok9bUAbA9BjrAToUQFEJQ1zkd8VJdXk+HgQ6AZzDrCtipNNtKuj2raY9tyl1h9hWAZxHRAXYoX7bqunbVWkjXIz51bs/V2J07fkVzLtsCr8NAB9Wgs1/vlIScL1u9P6fmFa21XpI5XLJ1KQ/onmcUFdW6VyTiRwVrz6qQzxfYLOpiFceV18cpy0UMO9l2eYoVBYfPj6FYuydvL5bQkGlXreqMujG9/FM8Xbn8egf29OHFqP/7v/97fkcv7ezrktbOefe6N69t29YNg53jDnQys0Etp5dd6otRIRYDFt/I2p9yFxXJk2lxzrSPIO/jaVv0aqyVd9tUJF9VcHhYzDD3a6lo8U+Z4fdI+9iuX0MdGOh8hG0ql0sLHdiGqu7sK5KSkMsv/zoiMFu3xuiDFg/cYnGF16m9IvkjBYfTZd8fCvEPtUoFSE3bMsg5GJKRP8FQkdycVSSPl2uLrXjc+ZLtr1idjBXPbjmVfCjVEYF5RZsGOrwvvlIMk8+5cacv/xUVyU9FPlOfkcvLdF0royhvm3T5yP1+MbQrX3upr7k4vrWMU2vK0hLloCj1dWUft7a2F+rGQOcjPVK5/EoHhi+VI1Z5IJoct02X6AKFPr/QOyuSl689ewzXju/2bybXFftt0+Xf4dRORjptT53c7dpeqB4DnY/0fOVyc/jLCPWKMapt89///RGXV7d5Cv3xBzp1Xy/ZbUXysmjx2f0pZ0huuFRljL5LF9HDT1iZ++gY6HyCDSqX39eBPXWwm+/xSC4vW70/4vL6Ng1yDj/QiWH8PR/9edml3x1UJI/+dCkq2EbNbLg5Xrz+adaX0R9dK5Mviw35itXVLMbdmF7+KZZmUw33T29PH3cxLVTbzkzIU2zTl/hzO40xJa4eMXnVWjuURSh/t1tJrHvfngbf3nsdtbvaZnp5+kv++b//e/jlFYB7MNBBNejsb2uaZrJIYB2zo17dftLigQC2xUAH2IkQgmIMH1v7yVpPkU8AdyNHB9iJlIcx3vqwNi0e+AlrJAHYFhEdYCestXLOfPSlG2v9YfOvALwGKyMDO5AuW0UZk7/g68id+fpWh5x9FWPUf//736f389tvvzEdGpggooNq0Nkv8z7l5xy5uOUaIcSh/EX37kPZTpSst8/vZxgPviziVXvBzBXHt3wMr63lh/ciovMp1hb1lJY7jHv2cffxbTTr6tWd/ZuE4BemlH9em9eMOcpgNhdZ+fPPP/Xbb789NNj/7bffJL2uzlvtBTNXHd+KY3h1LT+8BwOdj7C2qOe1DmP9Ph47wvo7+3cJIX2pn3+xm6KNk9vH3e6cKy7jHfMLKb+Pa1J7wcxVxxdvH8O1YqTYL2ZdfYK1RT01dBjdTCTkjn1s4bfffrv756hivFXbaun+I27XWM38qP773/8+9LOVdxbMfGlBz6vHQC2/I2Og85HWFvV89T6Wvbuzr0mMubCldD3y8QmtxkuSR0xKrsE7C2a+uqDnmmNIr3Gcy95goPOh1hb1fPU+cMvll/m1yMcntOk9d+TaV49EM98W0ay9YOZZLb/lY/i6Wn54B3J0PoFx+qGgHyGqbXMV6KKoZ1nr6pF9vMCRL0XdK0V08myrd0dU3t0mbesON9D597///dwOjF6Wu1Tm7gXbKJwVwxwfpWCLyz0zBTP/slZNzgHcsGDmuuNbPoYYz/NzJGZcHQnTyz/FyqKeZ1Mv0wNPHcYLZ12dahk9GTI2UvDHKeqZinhqmHFVJuZ+duu9V4xS27aHiCqm3+fJgdvw5/nzzz8PWecNeBQDHVSDzv4SqyHPizHKWq+u6w4x0AHwOgx0gEqlL3Orvi8vW9URUXl3myOAxjiKfAK4ioEOUKm0gGJc8UWeBwGftT1fvjrUKskANsesK6BCl6v/XpuNZD5we5pmfuTZVwC2QUQHqFTTNOq6YyTbvkaU90HG7D/x/OfPn/rPf/6zyb6cc7xngALTy1ENOvuTy5V/68iNqa9Nf6s9D3RijPrrr7/k3LTMx/1S8dcXlceorWhmbceDajHQQRV209l/kXz8p9+Bdq51zsn7/ZeDMEabDNZe9Z6vrWhmbceDupGjg2rkzj5/wT/zs3cpSlH+HtdyWD65Tf8+cu2rGizWwCutLZr5UJ2quo8HdWOgA1TmMpojvTtyUmubykEIG3pn0cw1RT2/8nhwDAx0cGbayd26je3lWjzL1cppy4hOunw1rt2PJ72zaOaaop5feTw4BgY6ODPt5G7dxvZC8EPJB2maeDvffvJ2DZf4DNPM36G2opm1HQ+qQDIyUJHLJOp3z2qqv02X+abrDu1LjHmByOeO/71FPb+uaGZtx4O6sY4OqnBa0l/aorPfa1HPEKJC8Oo6yhrcI8+02+sqyf/617+er14+OEpCPrAVIjqogjFGf/755yad/Z47+hjz7KH3R0r21Jp8lr7TqM4///nPQxShBWpERAeoiLVexqypb4WpprFUMwdwgWRkoBKpbtN0ld93z2raS5uSkllPB8AUER2gEiEEhRDIz3nQnvN0Yoz673//+/R+fvvtNyJawAQ5OqjGp3f2Kb9kvKUacl/200rGXE4l3oM842qLd2xUlHPtLhPxgVchovMpoldjT2F9d60Q3lKxvHv2ce/hRcl7+9GdvbVWbTtXjPT0ZT6P7ZIZZ+7t7f99Pu7OGenJAbr3QeZVMw5rK6K54nhisLLjcseXrzd/rDgaIjofIeqnDWMBuxisrLUyM53McrG89ft49Bglqd2os98bqpU/3+YB4h4XDtzsy/VF39K1FdFcdTzRy/o4npClPuunTP9HesfcOFYcB8nInyAG/ZDGL4JcWmDu62CxWN4d+3hU7Z39K+UvZ6qVP9e2bbvLgU7taiuiuep4ps8xRtIPhbjuWHEcDHQ+Ulrq/LkvhC32gSwtcnh2nZD2oTb9m9lX71BZUU/j1Jq0cnI+lnXHiqNhoPOR0of8uYTdLfYBqRwsln/LOiIke2vT+3Gn78mdHvZJfUU9x2Ppe3WtGY/xnmPF/jHQ+QTG6YdOM1LSF+vwgS+L4D26j02Pdesd7kOK6Ejvj4jsvU3r6ewtTytK48rOz/x8eUiitiKaS/1ZDPI+Sm64VHXlWHE8zLr6FEszpob7x4S9chZCeuCpWN5LZ12lmSftBhfMQ4ivm3nyAqmYI6shbyW9l4Latt3NF5f3Po10nhQl/fnnn5uXk1jsFyb9R54JNcYoy8kLZ6OP7Yp6Lh9PVLDF5bFp4c+FY8XxMNBBNWrv7F/FWitjNAx07p9tRFu2SdNYte2+ppkDeA0GOsAbpeiDvRF9OP8SZ/ut7VHWBhljiJIBIEcHeKc8O+h8ReRpaxbuZ/v89vNq5gA+GxEd4I3Iz3mNGKOs9aJ7A8DKyMCbxBhnini+O8flKG2aQRPCtBp8nbaMPO0lARv4KkR0UI1P6+zHmWaz9a3wrBQt20eejrVW0vOrK0S9KBG/mrpSk5lUWpr9eb221sUssOmMLBwKER1UI30xVdzZbywN7OJkkPPuSMhR2hzRqT9HJw/wW3OebXSP/A7yMerf//73pu/9qupKxagQiwGLb2TtT7nhdaZmp4wPa+qM26JXY6282265DNSFgc6nWLsGzuLjXlB9uHzZyjv7V4gxypjpZRVDu0mrUz22OB1M1qc46qcH+lszba/e+UkJhRvPGetK/aFW29aVchd9zl+K8Y/ZWsDRWzV+OKbJoCd6r2A6mRgl/aDm1YEx6+ojnCqP56XQg7W6PNm9/bi8Lf1sW/X3vLO//z+d/dRtXMn2dA/txm2aeTX9O9ep/iO8YYO6UqvqXBl36nOGwpwybmaQc6W2lnHqulZGUd426RKW+30HvQYexUDnE6ytPL7icVtVH549zE33Vr8Yo9o2R3SuRSgi2x/ablL5gR0MdPbv+bpSd9W5Glc1/rEq1+estlb0aoZ8o/F4JiUqcCwMdD7S2srj5ePWVR/GOiGEcSCZXGtvPY7tS9v3EtXZZTThTXWlYrBqrFc0rboyN6c4nvtqa9V3uRDbIkfnI6UojbvZ0Sw/zjgnhW0LJ35SZ3PKG3l3LsuxW+ecrB2SNCp2Gp49OyDbfkBXJiMH2yjMzlC6VlfK6I+u1V/WqslJzW33WOLvkPQ8/ntIwDFtp85MH3rKz5HKfMJWnQuyttHYg7lOPUk6h8X08o8wJBIPnU+aWqn0wdd5Ebylx5lo5dWOoeTNZlHkI8xTrTfYV4hRxtVd56hpmpQnMA4iy8gE7VZtLvBZezmIPL18C3uYcQh8JQY6n2Jl9fKlx21dfXjOp3T2rJ/ztfa0nk6ZbfSVzwWOjIEOqnP0zj6EUKyIXEfk48htCOmn67rV/48AHAcDHeCLUd/qa+XLV9crxAM4KmZdAV8ozwA6z82hfV2r8XbtM68AvAYRHeALparaVn1fXka5dcGN7c9sz8VTa87T+fnzp/7zn//o27dvT+/r999/J3IFFJhejmp8Qmd/vn4O7Ve0adFAKUd1antfxBj1148f+r7Bvv6S9D//8z9v+B0ptol6EdFBFWKM8tZu1tm7ts7p5dZaOWeqPLYjy3k6NSYkR0neWj0bazJKdd7Mpu/9qJ/N3/p9oWjm6WFB1oaxDlVafuLH+YJ+4/6s/lootmnTehZFsc2wXJcPWIkcnU8yrByafxZXNb71uBhkrz3/EcZIxuj3J3/+MPWucnqZnyO9P4flU9r077DxIpc1eU0GktHv7V+yt/oMLRXbnH/stVIy0XuFqCGnimKbeB4DnY+xTWHP6Ju0/PpXH/5KtR6XdLpsdX5VwdB+QZv+7mbxixfLxhpUXatoKbaJ/WGg8yk2Kuxp2qEIHh5U5pCI9gsjOsYYhVB/OYhdo9gmKsRA52M9UtgTz4gxFrkTdUQ6PqctozrHfC+/KvIRw3CZqRiEzFUVp9gmasWsq4/1fGHPGtV6lKf8nDzQWT9riHab9rxafG2iQpS+SfrPA8/+JulvnX7bLY/rb/9dXd9d3y/FNlExZl19jOcLe56uwW8/GyJK8raRebKzl+qcdZXKPviFWT+3vp7YvtV2a32VBT63TJLOkSsACQOdT/JkYc+0i0a27JM3XOfiyJ29tXb4gjV6d2Tjk1vvvWIU5SCAD8JAB3ixXK2c9XPeL61MnSJrDHSAz0AyMvBirJ9TU6th9tVx19MBcI6IDvBi1qZq5V1XV17Ip/I+KMZY5SrJALZHRAd4oRTNCcXCae+OaNA6Z8YoG4DjI6IDvFCuVt51JL/WxHsvqb7ZVwC2R0QHeDFyc2pqAXwaIjrAC6X1c8KN/JyoWtaZ+ZTtuZo508yB4yOiA7xQKuRZ3jMXaTAL97P9dduHW+TpAIdHRAd4kdP6OU6OZeyr472XMY61jYCDI6IDvEie2ZMGOe/OTaGdtqynA3wGIjrAi6SyD2JmT6VS/lQkTwc4OCI6wAuc1mkZK6HSVtY651hPB/gARHSAFwghyHvP+jmV8z5duiLqBhwXER3gBdJsK9bPqb01RkR1gIMjogO8gPd+qKfUKn2p1rWODNtPmsZSzRw4MCI6wAucz7aqcR0Ztksaq8oz+wo4LiI6wMby+jlt64gS7AB5OsCxEdEBNpZzPsjR2UOb8nSI6ADHRUQH2Ji1Vs4ZVtzdiRCiQqDuFXBURHSADV3O4Hl3xIL2VuucYeYVcGBEdIAN5fVz+r5796HgDt6HYZYc/9+AoyGiA2zolJvz/kgF7fo2X7EiqgMcDxEdYEPee0lxMoMnquZ1ZNiesJ4OcExEdIANhRAmScj5S/ZaRIHt792eOOeGgSqAIyGiA2yE9XP2LVczJ08HOBYiOsBG8los5Ojss82DU/J0gGMhogNshPVz9i7K2nTpkf+HwHEQ0QE2kKMAp0tW749Q0N7bsp4OcEREdIANsH7OMZCnAxwPER1gA/OzrWj31hpDVAc4GiI6wJNijLLWqm2XcjvSZZEre2B7Rdut9eTpAAdCRAfYyPJsq3evE8P29dupZg4cDREd4EkhBMUY1LZOa1bgRd1yng7VzIFjIKIDPCnldEjrVuClrbtNKySTowMcBxEd4Ek5P4ez/+NIpSDMpGYZgD0iogM8IV22Ks/+3x2RoN2mBXAURHSAJ8xXK8fepZl0XnSPwP4R0QGeEEKYXLJ6dySCdps2zaJj9hWwf0R0gAel2Tl+xeycqJrWiWH7uu3WehlDng6wd0R0gAfl2Va3q5WzfX/bJecMs6+AAyCiAzzIWjuc8bOC7hHFGOV9YD0dYOeI6AAPOFUrH++hPVibI3VEdYB9I6IDPKhpGvV9K1ZDPi6qmQP7R0QHeID3Yah0ne95fwSC9hWtqGYO7BwRHeAB5Od8BvJ0gP0jogPcKZ/hO8f6Ocdvh1tEdIDdIqID3CnlbQR1Xa5WHlXjOjBs32a7tV7OOTlH9A7YIyI6wB1ijMVqueUg51pkgO173u6cGUp9ANgjIjrAHVINJKuuI2fjc0RZG4jqADtFRAe4w2WuxrtzSGhf20r5shZ5OsA+EdEB7nDKz6H+0SdhPR1gv4joAHegWvmntsMtojrA7hDRAVZKa6p4OWfI1fhA1lq1bUduFrAzRHSAlU7r5zi9P8JA+/WtUQhEdIC9IaIDrJRWQ5badpqfk74El7H9CNvJ0wH2iYgOsEKO5pwuW5yf6d+KBLB979s11Daj7hWwN0R0gBXy+jlUK/9kaT2dVOOMWXfAXhDRAVbI0RyqlX9ya2SMiOoAO0NEB1ghlQCInMl/uBTZ8+o6Zl8Be0FEB1iB2Va0pVO9MwC1I6ID3BBCVAi+qFaOT0Y1c2BfiOgAN8RYVisf76X9yFZyzhDRAXaEiA5wQ9M0N6qVR9Wwzgvbv2Z7WiE7qG2pYA/sAREd4IqUhFyaO9OvYVLisyEAAB6eSURBVJ0Xtn/V9jS4iUR1gJ0gogNc4b1XjJFq5TjDKsnAfhDRAa44Xw1Zen+OCG0NLaskA/tBRAdYQLVyXJNqnznWVgIqR0QHWHBerXy8l5ZWkmSMI08H2AEiOsCCdMZu1LZEc3Ap5+kw+wqoGxEdYEbOvTh9f707gkBbW5tnXwGoGxEdYEYIUd5b9f2aWTVRNa3zwvav226tp5o5UDkiOsCMEPzkjP1aW9c6L2z/uu3MvgLqR0QHmEgVqq3alnpGuK1pLNXMgYoR0QEWsH4O7ZrWOTOzgjaAWhDRASZCCIoxkHeBVbwPipHZV0CtiOgAhRinNYzeHzGgrbt1jjwdoGZEdIBCzs+5Xq0cOMfsK6BeRHSAQghBxhjWz6G9swVQKyI6QGF+NeSoWtdxYXsN23Mk0IvuFKgPER1gkJKQU87FSf6Su3ZGz/bP3p4Yw+wroEZEdICBtV5SVNeRZ4H7kacD1ImIDjCK5ObQPthKzpkxKgigHkR0gEFeDZnZVnhMytNxrmVFbaAiRHQAaVg7pzwTf3eEgHZ/bRogE9AB6kJEB5CGJNJIfgWeEkJacLLr1lS9B/AViOjg4+XVkI2ZTimnpb2vzVc9z1fXBvBORHTw8bz3Q62ipfyc02WJeWxn+2k7s6+AuhDRAQZpkLOUe3ErN4PtbE+38+wrAHUgooOPZ62Vc4aZMtgIs6+AmhDRwUfLa56cLlnVketBu+fWSCKqA9SCiA4+WghhmCVDPgW2E0KU99S+AmpARAcfzXs/U9uKlva51pgUJSSqA7wfER18rBzNYTVkvELK03Hk6QBvRkQHh3Sr3lBeO0e6NtuKlvbRNtW+WlvNnPpY2+LviRIRHRxKHsA4dztK0zSNuq5dEc2JqmmdFrbvY3uMUd4Hte3191g54Cay+LwYI39HnCGi82b5zGPa4jH5clT+8lj6e6aVkNfm5tS1Tgvb97E9v7+8X87TiTEOAyI//huPy4Mca+1ZJXn6189GRKcC+QPJSqrPCyHIez+eRS+d2eUvFmZb4ZViTGvqdF139b2Yo5D0AdtpmkbGGPKkQETnXfIllqZp5L0fO0HOPB4zd+ZmjLka0Tn2bKsg31g1Ntz5vDvbmF7Hh+f2E4NX01g1/t1/t63b5Nrsq/zZL9+v0/ctt9fdLtu2bcdoWdM0sxEefAYiOm+QL63kD1s+kyu/nLnG/Jg1EZ3T2jlO13Mvdix4Nd6o693wG0bZxp9//bpWffvs75/267pO7uldBTU2yHWdnj6sityafVVGdMrPP+3z7fRyIBGez/SPdx/AJ8lfwnNyVKc883t3J7HHtszNcc5dDBpTJC13fDm34mhtWrDOtU4m3x9jGvC0rTpnFIOX9UHBOTnzxOuVZ8jP7EdRMk6tC/I+yHVG5u1/x23aXPtq7su1fH/mKC9eJ0d4vE+XEyWd9Q84JiI6XyB/uAiXfp2liE7KmbArZ1vtVAzyNkhnkZEUeTHDfTFYWW/U9q3c8PjxK9Y49Z0bIywnbogQRQXvVebYtl0nZ6Ki9xqfsrSfcUBT7vN07I2N6bi2/ru8Sfr8h8VIAhGdr4voSDr7/3DYPgBnGOh8kXy2NnfGli9bLckf2untact2jR3bUmdmrZWk4rLV+8/4t2+jbBPlulbO5MhLkLWhuHRl1Jbb8/ODV+OjXNuqNfF0KSkW9yuo8UrP1zCoatO/rdfZ4Cm2rbql/Zgoa8Mw+DodZ95f6979d9yutdYP77tOpfx+TSt0nw+Eavx87Wm7dPq8SxoHkmWkdxrxxUH1+DJd1/V93/fOuV7S+NO27dl22sfbtm3Hv2m+v+Sc650zfd93xU87uT392dn2zvVOpm+7cnvbG6l3bdf3nekl9aZtx+1t8X6UlJ7bpfepa0/Pb7uu75x6ubbvhufO39/1rVGvtu37Nr2eK/aZ9+/OjuN8f9X+fe/e3vVdl96XS+9JSb1zru/75fd3xu11t40Z3ufG9F3XLf49cXwMdF5srtPKP+WAJ38x1zBY2HO79KWR/52+bNIX9/mX1IHazqVBTVfcPxlUtE69ZPq2a9MARSYNUPKgpE37KQcobri/a83p8fm1ivvTIKV4vXI/5f779FzTFv8/xn1U8HfcsO26tjfGjO/L8j2Z37Pl4Jz2uTb/rdf2qzg2Ll29UQ6vluvoEEZ9Tk74zpcByr/n59S2Sjk0waTE43xfmaMjRfnGK8ip6yRrzy+ptl0np3IWVDm7Kio0Xn76+Bs5Oq7r0mUvG8b9j5e3huOMwcqG4XkH4336nHeTy1eso7Otpctc+Fyso/Mm5YevbdvxunGZa4L15v5u5bX6PMgxJufs5McdsU1J2NFHlVk5XZ9zYZK279T3RsY49X2rvu/G1pmYBip9OyY0d/l+Gbm5x8vItMX9nUvHU+7HmLP9t30e5MSUR+Ql17pK/o5btqn21VxybO4HprlmeMz07znN4cHnIaJTAc44tpOTvqeJyDnSc+jZVmeGiI1r1bVG1f/GQxK02lb90wvy1GtuTZ08+DHDLEH6A2BbRHTebG7WEJ6Tw//TiM75l8e7z/BfH0Fo+059q2GQ8+7judE6lyJB4/d/Jce1cWvM+SrJ5QCHQc7zpv0n/SkkIjr4AGXeTtseL/cD+9I09mrtKwDbIqKDQ5o7k3Pu6Lk5tPW36X04XSGdyAPwOkR0cHjWWhmji1lYJ1G6msXCdrZvtz0lxl/OvgLwGkR0cGh56n6M12Zb3Yr0sJ3t220vyxMAeD0iOjg08nNQnziuW0RUB3g9Ijo4rFxDaLhFS1tBK0nLBScBbI+IDg4rD3RykU8iOqhBel+G4n3JasjAKxHRwWGFEBQV0+Ilbz+Tp6VNrTG6KP8C4HWI6OCmGKysj5Kcur6tf5XdgbVWzrlxsUAiOqhDLGqLRTnXnq2UXLu99gf4XER0DiD6Rk1z+vFBaUn9/O/7d5ieGyUpKPgo06b6ReaZ/X6h6TolNZzJ09ImeQXkYcvGER36A+AcEZ29G2oEtX2ndE4Y5INRu1m9oCjfWKnt9ZqASBiqYvfa6pBzbo4xRs65MbKzHNGJqmmdFbYfe3vO0TFGcsbI+qDNumH6A+ACEZ2di4qSUseZuNSpBa+m8QoxPSrYmbO84Uzt9OMVlO+3SieCuW1S0cUwbBtOQkN59uiDYgyy5T7tUD87XL5WlBRsar0tXv/Zv0kukujM8PdJf4Pltq51Vth+7O1jTavhHmPmIpCPeWl/EF/dH8SX9AcAA52dM65NZ25Fx+GjxgRcY6QYvHx0artefd/J5M0D1/Xqu1ZSKCLsRoqSa9OZoWt79a05PdFIMVj5kPfbqzOSMU5dn273nZPi0LkOz2u74X4FhSi5Lh1P2sfwuzwp5+Tk/8YDpqWtos2DHck4I7fhAoIv7Q/06v7AvKQ/ABjo7J5RW3YkkkKI0lgNXZKiZMzQ16UzybJPzX2cO7u/OANVPlPMD0iDoGG54THEbFzqsHxx9jbuvzwecxp+zB3PM/KXRS71EBWvrIhMS/vVrSSlgU0O9DjnNlxTZ6Y/iLk/SIOr/Lld6g9Oe8r3X35+7ukPwqQ/OD3v9f0BIDHQ2b8QxrCxjNO4IkdxpjV2RMU/yzO4OHv/6Qw0dWV5f0Onl08DYxxfP4agELyChrO4oaONxfGUT186nmfkL4w8i8UoJ37WcCZPS6vJ+zFpndvm8tVcfzB+wMrP7emwZj9/5cd9vPx22nBPf+An/UGx45f3B4DEQGf3osJwPbtR01h506przdmZVgpn++FauR9PviY7mpxJ5d5n7gxu2Ow6te70+jZKRukszl47g9Opn5XSGeBW1+RzuYfTy8az9v1n9LSf3uZ1dNLHq/gkDJewnkF/AFxi1tWniUGNDcWsjONIVaHDRZVya63a1u1qrRIcWVpHx5gUycms9XLtF6+pc+D+AMiI6HyEYuaD9WNC4ZHEGBXCkBNkTrOt8srIRHRo62glqZx1dYqMuK0uX910/P4AKBHRwSHEGFPkpmtVpDZKWhPRGcL6y3tnO9s3216uo9M6p5zEqxhlQxxW8ab+FbAVIjo4hDylPBsjOqtydMzC/Wxn+/bbz9bRKQY5eSZUvgQLYBtEdLB740rILq2EfHaVQOTooDbzOTpZY73ar87VAQ6MiA52b5xSbobLACoiOsUZ9PBoWto3ttJ5jk7eHMfWGUNEB9gQER3sXtM0atu2uHSVLxckRHRQk8UcnXJ7iJP3NIBHEdHBrllrz27HYZBzX44OLe3XtRfr6OQcHalYTDBdjt26sjnwiYjoYNestalKeXuZm1M+hogO6pFydJzR+XuyiOzEGGV9UNd1RHWAJxHRwW6dVSmfyc3JLTk6tPW0Us7RKe+Pk8hOqqhArg6wBSI62K0xmnMjUsM6OmyvaXvO0RkjOmMkZ3jccDuEqBDJ1QGeRUQHu5TzF8oq5bPtpKbO/Jl2XeussP3Y23OOTjmoOVUXP912LrVEdYDnENHBLuWBTtu151cFZpCjg7rcztE53ZVydeimgccR0cHu5LpW5eKAixEd5Ryd8dm0tG9spVOOThHpmZl9JZ1ydaazCwGsR0QHu3M7Nyd/iZweT0QHtVjO0RkfcJazE0JQiCJXB3gQER3syrrcnPN1dIjo0NbULufoaDL7KufqpMFQYE0d4CFEdLAbY02rG+vmTBHRQV1W5ujMrKtDdw3cj4gOdmOsaXVj3ZyzlogObVWtNJejM11HZ3pbSjfJ1QHuR0QHu7Gcm5O/NJafxzo6bK9l+9p1dKa3c1SHyubAfYjoYBeu5+YYPRfRqWudFbYfe/vadXSmt40xaU/k6gB3IaKDXWiaRs65u3JzMu+9nLu9gjLwNe7P0TndRQ0s4F5EdLAba9fNmW2vRnRoab+qlVavo1Pm6OR1dYzkjJH3XgDWIaKD6jVNI2OM2rYd7slfEkvOt6ccnTYtqQ+82b3r6Ey3k6sD3IeIDqo2nWVyMydnun3M63n3mTwtbWrvWUdnKbIjnfLWAFxHRAfVCiEohDAOVtq2Pc/rXCnl6DgiOqjEgzk6xewrH4JiFFEdYAUiOqhSrmcl6Tzpcu36OUVEZ3giLW0FrfTIOjqXt9NNojrAbUR0UKUQgrz3attOPngZqcjRmcpfGvNu5+hcfz7b2f6adXRMek+uXEcn344xyoagVkZRUpDUd92V1wc+GxEdVCeXenDOKSqefYXczMmZiejcztFhO9u/bvspR0enQcyKdXTGQU+xW5cW1hmjnwAuEdFBdXICsnHtGJ43RmrdUkTnOnJ0UJeco2PO35N35OhYH9QOz/chDeupbg7MI6KDqpTJx3kVWCONJ8T3r59z7UyblvarW+mUo1Pcv2YdnUntq+EDona4/EW+DjCPiA6qkS9ZSefVyS9XNs6XAxb3dLY95fo4znZRheUcnfEB69bRKZ4fZVLeDrOwgAtEdFCNHM1xzp1VJy9zGh5ZR6ds339GT/vp7fh+HiIyj66jMz5fRkYxrZhMrg5wgYgOqnCaZdUqR2OiTlNo3WzV8nWI6KAu2+bonAI/UT5qsoo4ACI6qIL3XsY5nQY58SxH5zyic0dLRIe2qlbKkRpTJJ/du47OsJuz7cYYOZ1OGgAkRHTwdnmWlRtmVaXLVWb8brhdfXw4pV1wO6Jz/flsZ3tt6+j4EOUkOWfGQU5+nA9RIUYqnAMDIjp4K2vt0FGnQUyK5Bhdz9GZttfX0Snb+TPtutZZYfuxt+dIjrnI0Vm/jk7O8UkRz9NKyzFGtcOMRWZhAQkRHbxNDrE718o4c37iOjTGSMH7FJYnRwcHEBXln8zR8SHI6TxH5zRoSretD5Jzah3vfXw2Ijp4izzIMcYNg5zLXJyz2+To0B6iTXOkNMnRuXcdnVOprFNkp1yfJw7r68ShMC7wyYjo4MuFovN1rh0jN6dITgrHZz5MZ13lXn7J+XYiOqjJFuvo+BBT9XNT5ujodDlruB2UHku+Dj4ZER18qVyVPK2X015GboZBThmZuZx1xTo6tPttl3N0ppGc5XV0ygiomURyyttGaTCUc+GAT0REB18qBC/vw2m9nGkkp5htlSM95OjgSLbJ0TlFdOYiOdPbdhjkdFQ5xwciooMvk/Jywni5SpqJ5JCjQ3vodsjRKSM6mkZy1t1OgaGZSM50NpaR2uG18lIOwCchooMvEYdO1jmXppLn1AMVgxwVt8t1dC5ydC72LtbRYftetuccndaZs/VvxsetXUfnIkcnjhGfudv5ecY5Vk7GRyGig5fLg5w0wDHjfeeDnMntpcjObOSGdXTYvp/ty7Ot7ltH5zJHx1y9bYyRM2aMrAKfgogOXmoc5DgnN0Ryxj5e8zk509vk6OBIco7OGNEZN+TIzfXbSzk603V0pjk7eXsYVk4msoNPQUQHL1NGckwRyZHWRW5uR3JWtOTo0FbVnnJ0zu6/ex2dIkfH6CyCc9p+nrOTtztXRnaoiYXjI6KDlxgXBBxycubWyRlPNC8iO+fr6IQwjejkZy45305EBzWJMSr4IHeRozM+YNU6Oq3RmHszP9vqFAGa2x5ClI9RjsgODo6IDjaV18kZVz0e6u7MrZOznJNzmXMz7n/orVlHh3avbRpzrInkXF9HJ7fL6+hMc3bOtztn1A6RHUtkBwdGRAebyuvklLOrziI108jN1dvk6OB4LiI6pw135ejkiM5lJGfd7en+ZJy6jsgOjoeIDjaRpsz6cZ2ccnaVdCVyszJnZ3ydq5GcmZaIDm1V7XC5qYzoaBrJWXl78vzFdXQWto8RH5MiO4pBTdNo8pEDdo+IDp6WBzkxRrm2Tfk1OUVAxSBG5zk5t7bn74IQvIwzadbW/BGIdXTYvpftyzk6w+Nu3F7O0YlX19G5dTvGKB/Tq3RtSwQUh0FEB0/J+Th5kJOtWSfn1nYNt4d/nN1mHR2273X7co7O+nV0ZiM5Fzk5991OkR3JSbLWjjXpgL0jooOHeW/Hfte5YZBzNSdnuk7O+nV00tkvOTrYv1fl6JwGTbqak7Nme6567pwb8u347GC/iOjgbiGka/khSDJGrm0vIygzkZnZ2VdXt5cRGY3339WSo0NbVTufo3N99tXl9vP78/t7XU7Oze1DVKdzRjEEWWtZbwe7RkQHq4WQlo0/rY9jLtfxUDGI0XzOzSPr6JyfVeZnLjnfTkQHNallHZ3b29NtH2IamBmnlugOdoiIDm6KMappmmFW1WnQccq1mV8HZynn5pF1dM5zdu5fR6f4bWhp394+u47OfI7O9Pb1dXRub0+322FWlolxjO6Qu4M9IaKDq8oZVTJGrSsSjuciMZveLnN0Hj+TJKKDmtSyjs4j6+4EpQhPXtfq0bWtgK9ERAezQgjy1spaO56LlsOEx9bFeXwdneksrHtzdMojp6V9X5vzfS8jM/eso6Pp52Im5+bWOjr3btdwQTl/LoP3zM7CLhDRwZkcwUn/lkw+Y4spP8e17XimN/SJp0GKznNunt2evwsuc3QujlrXcnZYR4ftNW3fYh2dMFQv33Idndu30xHYENKlLElhiPIQ4UHNiOh8uBjj0HGm2RWnCI4r1sU55QqcrbuhcpBy/zo5t7ZLpzPf6xGd2+voFL/xTGsW7mc721+z/dl1dLZYN+f+28XxD59fJ6kb8neC92MuX564ANSAiM4HyyHnEMIw5VVyxqWhRnGNPsaoFNExcq0b++zn18m5Zx0dcnRwDK/K0TkNmrSYY/P0dhk1RUSniDspDj8hD4qGKE+enQm8CxGdD1FGbry3w5lXUAhRxrWScXKuHQcXc2d0ZykC2mKdnHvW0Tk/EyZHh3afbb6VP0hFe/c6Og+uk/PM9uJzmSOw5e9jJLXGyEkyMY4zNXMuD5EevAMRnQMrBzfGmNTJDGdWeZXhMVdmEsGZtoppH8a5Uyeo+ZyaGtfRoSozarGcozM+YCFHJwkxKs7m6GgclGyzjs7l9qjzHJ2svDg3vR1jVBz2E6WzCE/O6SHig1cionMQp2hNOoMq172JSp2jca2McTImfenfWl/j/AxP4+2t1sm5tT3fvmzvX0dnmmNA+1jL33Gjv2O+fTWSM7+Ozimi8uw6OXduN+nITXEcijO/z+S2MUZOw3o8klyMiiGMqy7nn9x/lbO4mM2FLRDR2YHphz1Has4iLjqdiaWzpmsRm1sRnMvtZURn7MN0ax2cZ2+nvvX2rKvrUkTH6XoUCLfk2XhtS3TsGVvk6JSzrvIHZTkys83tPPjKER3lu59o898jnl0WLyI8Q9tOZnMRAcI9/vHuA/g0c4OW3F5cLioeU97OgxGNg5LUGRnXSopyS4MVTQY1mr7e/PZ0vy4HJRcRnpkp489uPzsTLju389vTy115exmROu8br++P29Pb5f01HM+Ob5vy/TqOKuYvV03bvLcY08lMeXmpeN5Lbud+YuhXnCk+t/nzptPnN0dWl7bny9d5P9PfL6Z/SJL8kNtTDpLKy15z/ed0qjuDo89FROeLPTz1cjyDMueRj2lfqHxGtOXtqNwPnUV8dDrRe9VtSYohXK7PUZ4S3rgdQlDbsr7Hc0wR0eFv+Yx04jJ8nm7GPC7bNAhIA4Vx0GAmJwkzkdJntw/dgMIwyEmXpfLn9XzCwta3y89zvnlPL2qMUdd1j/zvwgH8/z9+/Pjx7oP4JD9//tS3b9/07ds3ff/+XZLWtb9+6bsx+vUrpjZGGfNNv2LU97L99cjtX/oVf13ZbiT9Kjqfb6n99u3lt3/FqO/fvyvGqG/D9m/fvin+vf729+/f9fffUdK32TbGb0Pkh+3L2//Wr1+/JEnfvpkKj28/2799M/r161f6O8ao+G2IlAy3p+10+zdj9OuX9M0Y/f3rl36Z74rx13j7m/muv+MvaePtMkbx16/0efz1S9++f9ffvzS0r70dcyvJDO3a/vPbt2+SxGKGH4yIDgAAOCxmXWGVpml2+9rvPHZgzjPvyXe/n9/9+sC9GOgAAIDDYqADAAAOi4EOAAA4LAY6AADgsBjoAACAw2KgAwAADouBDgAAOCwGOgAA4LAY6AAAgMNioAMAAA6LgQ4AADgsinoCAIDDIqIDAAAOi4EOAAA4LAY6AADgsBjoAACAw/rHuw8A22ma5uz2tTzzNY9tmubqPl55DNNtt/YFvNI97+vyOdPHPbKfR577qs9WDX3Mnhz999sLBjoHsdSpru1cpvfNdYZffQxbdBA1fEFh3+55X5fbt9jPI8991Werhj4GeAQDHVzIHdLeO6IavqDweY7y+Xkl/kb4SuTo4MK7v8DfNYhg8IIt1PwequU9XsMxZHmw1TTN1YHXdFt5Oz/30eff2sea/WMZER1U6R2XimrqfIFX4TLspXIAeO9gcO6S3CO5jUv72GL/n46BDqrEpSLgNfhsXVrz++dLbWW79rlb+vT/V49goIPq8EEGXoPP1npl5OvW322LS0pL+5jmMvH/8H4MdAAAmLhnyv0Ws8muvR6Xrp5DMjKqQ8Id8Bp8tuat/btML1s9up97jof/Z88jonMQc1M1l84Cbj323cfwquMDHnHP+/qZ/Wx1DK/6bNXQx7xKebz3Huf0uWsvQV3bNl3ziEtXz2l6/mo4sEe+oFgwEPgcXAo6PgY6AICPxUDn+MjRAQAAh8VABwDwsYjmHB8DHQAAcFgMdAAAwGExvXzH7pkJNDetsaylsnY/9xzbvauJXlt0q8Zj2uq4sB81vIfe+dmquc8BljDQ2amlKdBrV9d8Zj9rjm3NY5Zet8ZjyuiQP1cN76F3frZq7nOAa7h0tVO1dgqv6rCe/XJ49Pm1/p3xtWp4D737s8VnAXtFROcDfOXZUo2d4Vdd9sJx1fAe2tP7by+fF2vtxX1d1616/PRxj2yz1qrrurF95jWwjAUDD+TaSr9T786HWSqEV4bXt172fO0xzb0u+TmQ6ngP1fTZqqnPeVY52FizfTo4eXSbpKf3g+uI6BzEvdfKX5kPs8ZcZzstZLemXMPWrr0ueQVY493voa/6bO2tz9natUHGPQOQRwcrDHLWY6CzE9fOwB5JCHz1Ma3ximN+1THtrRPG+9TwHnp1f/CuPudV5qIlWb4/X2Ka3v+KY5nzVa9/RAx0dmKp43jnmVCNnVmNxwQcyR6jL9fMXQJaGkR8xaWjtZEiLl2tx6yrHbtnWmhtpsdUe+dZ498Q+/JV76FXfrb23Oc8aynS8uxj1+5nq31+IpKRd2qpIykTH9cm/31VMvK1Y5p77LuPafq6NSZQ4mvV8B5612er9j7nEbXMutriNbCMgQ4AADgsLl0BAIDDYqADAAAOi4EOAAA4LAY6AADgsBjoAACAw2KgAwAADouBDgAAOCwGOgAA4LAY6AAAgMNioAMAAA6LgQ4AADgsBjoAAOCwGOgAAIDDYqADAAAOi4EOAAA4LAY6AADgsBjoAACAw2KgAwAADouBDgAAOCwGOgAA4LAY6AAAgMNioAMAAA6LgQ4AADis/wejk0w7P+XVkwAAAABJRU5ErkJggg==)

### Reminder
- **p-value** : smallest significance level
	- [[___INBOX___/__à trier/p-value|p-value]]

### Example
- 

### TODO
- [ ] https://towardsdatascience.com/hypothesis-testing-z-scores-337fb06e26ab #todo 

### Resources
- https://www.omnicalculator.com/statistics/z-test
- https://pro.arcgis.com/fr/pro-app/2.8/tool-reference/spatial-statistics/what-is-a-z-score-what-is-a-p-value.htm

---
https://en.wikipedia.org/wiki/Test_statistic