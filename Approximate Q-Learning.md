---
tags:
  - reinforcementLearning
  - QLearning
---
Feature-based representations
$$
\begin{align}
V(s) &= w_1f_1(s)+w_2f_2(s)+\dots+w_nf_n(s) \\
Q(s,a) &= w_1f_1(s,a)+w_2f_2(s,a)+\dots+w_nf_n(s,a) \\
\end{align}
$$
For Q-learning with linear **Q-functions approximation**
$$
\begin{align}
\text{diff} &= (r+\gamma\max_{a'}Q(s',a')) - Q(s,a) \\
Q(s,a) &\leftarrow Q(s,a) + \alpha[\text{diff}] \\
w_i &\leftarrow w_i + \alpha[\text{diff}]f_i(s,a)
\end{align}
$$
---
**Loss using bootstrapped target**
$$
\tilde{L}(s_{1:n}, a_{1:n}, y_{1:n}; \theta) = \sum_{t} \left( Q_\theta(s_t, a_t) - y_t \right)^2 = \sum_{t} \left( Q_\theta(s_t, a_t) - \left( r_t + \gamma \max_{a{\prime}} Q_{\theta}(s_{t+1}, a{\prime}) \right) \right)^2
$$
**Online update**
$$
\begin{align}
\hat{\theta}{i+1} &= \hat{\theta}i - \alpha_i \nabla\theta \tilde{L}(s{1:n}, a_{1:n}, y_{1:n}; \theta) \\
&= \hat{\theta}i - \alpha_i \left( Q\theta(s_t, a_t) - \left( r_t + \gamma \max_{a'} Q_{\theta}(s_{t+1}, a') \right) \right) \nabla_\theta Q_\theta(s_t, a_t)
\end{align}
$$
Note: a pseudo-gradient method; may diverge even with linear function approx.

