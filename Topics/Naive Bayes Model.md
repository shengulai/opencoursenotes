---
tags:
  - machineLearning
  - bayes
---
**Naive Bayes setup**:
- $Y$: label; $P(Y)$: probability of each label occuring
- $F_1,...,F_n$ : features; $P(F_i|Y)$: probability over a feature given the label
- Training: estimate $P(Y)$ and $P(F_i|Y)$
- Classification: query for $P(Y|f_1,...f_n)$
**General Naive Bayes**:
$$
P(Y,F_1,...F_n) = P(Y)\prod_{i}P(F_i|Y)
$$
![[Screenshot 2024-12-16 at 3.38.32 PM.png]]

**Parameter estimation**: estimate the distribution of a random variable
- [[Maximum Likelihood]]
**For unseen events**:
- [[Laplace Smoothing]]

