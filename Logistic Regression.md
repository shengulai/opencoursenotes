---
tags:
  - machineLearning
  - classification
---
For $z = w_1x_1 + w_2x_2 + \dots + w_nx_n + b = w \cdot x + f(x)$,
Apply sigmoid function $\sigma(z) = 1/(1 + e^{-z})$
Choose the $w$ that:
$$
\max_w \sum_i \log P(y_i|x_i;w)
$$
Hypothesis functions:
$$
\begin{align}
P(y_i = 1 | x_i) &= 1/(1 + e^{-w \cdot f(x_i)}) \\
P(y_i = -1 | x_i) &= 1 - P(y_i = 1 | x)
\end{align}
$$

**Multi-class LR, Softmax and sigmoid**:
$$
\text{softmax}(z_i) = \frac{e^{z_i}}{\sum_{j=1}^n e^{z_j}}
$$
Use [[Gradient Descent (Ascent)]] to solve numerically