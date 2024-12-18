---
tags:
  - tdLearning
  - reinforcementLearning
---
[[Q-Learning]] is just the TD Learning on the Q function
- Q learning needs some exploration policy
- Q learning is off-policy learning

[[Approximate Temporal Difference]] methods are used also

---
**TD(0)**
Looking one time step into the future
$$
V(s_k) = \mathbb{E} \left( r_k + \gamma V(s_{k+1}) \right)
$$
Update the value with TD error at each step
$$
V^{\text{new}}(s_k) = V^{\text{old}}(s_k) + \alpha \left( r_k + \gamma V^{\text{old}}(s_{k+1}) - V^{\text{old}}(s_k) \right)
$$
where $r_k+\gamma V^{\text{old}}(s_{k+1})$ is called the **TD target estimate** of $R_\sum$ and $\left( r_k + \gamma V^{\text{old}}(s_{k+1}) - V^{\text{old}}(s_k) \right)$ is called the **TD error**. $0<\alpha<1$ is the learning rate.

There's analog of this behavior in neural science around biological learning with dopamine!
> [!info] Bootstrapping
> Update involves an estimate of the value function

---
**TD(1)**
Same as Incremental [[Monte Carlo Learning]]

> [!info] Sampling
> Updates does not involved an expected value.
> - Both [[Temporal Difference Learning]] and [[Monte Carlo Learning]] sample
> - Classical [[Dynamic Programming]] does not sample
___

___
**TD($\lambda$)**
$$
\begin{align}
V(s_t) &\leftarrow V(s_t) + \alpha \delta_t e_t \\
\delta_t &= r_{t+1} + \gamma V(s_{t+1}) - V(s_t) \\
e_t &: \text{eligibility trace that assigns credit to states visited recently}
\end{align}
$$
The eligibility trace  e_t(s)  for a state  s  at time  t  can be updated as follows:
1. When a state  s  is visited: $e_t(s) \leftarrow 1$ (or  $e_t(s) \leftarrow e_t(s) + 1$ if we’re using accumulating traces)
2. For all other states  $s'$: $e_{t+1}(s') \leftarrow \lambda \gamma e_t(s')$  (if not visited, stays 0, otherwise decay by $\lambda$)

---

| Algorithm     | Update Type        | Bias and Variance                 | $\lambda$         |
| ------------- | ------------------ | --------------------------------- | ----------------- |
| TD(0)         | one step           | low variance, high bias           | $\lambda=0$       |
| TD(1)         | full return (MC)   | high variance, low bias           | $\lambda=1$       |
| TD($\lambda$) | weighed multi-step | adjustable bias-variance tradeoff | $\lambda\in[0,1]$ |
*bias: some wrong will accumulate into the future

---
**TD(N)**
$$
V(s_k) = \mathbb{E} \left( r_k + \gamma V(s_{k+1}) \right) \quad \Longrightarrow \quad V(s_k) = \mathbb{E} \left( r_k + \gamma r_{k+1} + \gamma^2 V(s_{k+2}) \right)
$$
$$
V^{\text{new}}(s_k) = V^{\text{old}}(s_k) + \alpha \left( r_k + \gamma r_{k+1} + \gamma^2 V^{\text{old}}(s_{k+2}) - V^{\text{old}}(s_k) \right)
$$
Note for N=the full length of the game, it is same to [[Monte Carlo Learning]]