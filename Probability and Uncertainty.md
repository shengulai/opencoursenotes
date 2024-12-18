---
tags:
  - probability
  - math
---
**Probability Density Functions**
- Cumulative distribution function (CDF)
	- monotonically increasing
	- $F_x(t)=p(x\leq t)$
- Probability density function (PDF)
	- continuous RV
	- $f_x(t)=\frac{d}{dt}F_x(t) \geq 0$, it can be $>1$ as it's not the probability
	- $\int_{-\infty}^{\infty}f_x(t)dt=1$ 
- Probability mass function (PMF)
	- discrete RV

**Marginal Distributions**
$$
P(X=x) = \sum_yP(X=x, Y=y)
$$
marginalization means summing out the other RV
**Product Rule**
$$
P(a|b) = \frac{P(a,b)}{P(b)}; \quad P(a|b)P(b)=P(a,b)
$$
**Chain Rule**
$$
P(x_1,x_2,x_3) = P(x_3|x_2,x_1)P(x_1,x_2) = P(x_3|x_1,x_2)P(x_2|x_1)P(x_1)
$$
**Independence**
$$
\begin{align}
P(x,y) &= P(x)P(y) \quad \forall x,y \\
P(x|y) &= P(x) \\
P(y|x) &= P(y)
\end{align}
$$
**Conditional Independence**
$x$ is conditionally independent of $y$ given $z$ if 
$$
\begin{align}
P(x|y,z) &= P(x,z) \quad \forall x,y,z\\
P(x,y|z) &= p(x|z)p(y|z) 
\end{align}
$$
**Bayes' Rule**
$$
\begin{align}
P(a|b)P(b) &= P(a,b) = P(b|a)P(a) \\
P(a|b) &= \frac{P(b|a)P(a)}{P(b)}
\end{align}
$$
