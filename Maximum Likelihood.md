---
tags:
---
**Why log probability (*likelihood)***:
$p_1*p_2*..$ can become very small, $\log(p_1*p_2)=\log(p_1)+\log(p_2)$
**Maximum likelihood estimate**:
$$
\hat{\theta} = \arg \max_{\theta}P(D|\theta) = \arg \max_{\theta}\log P(D|\theta)
$$
set $\frac{\partial}{\partial\theta}\log P(D|\theta) = 0$ to solve