---
tags:
  - reinforcementLearning
  - tdLearning
  - "#SARSA"
---
**Overview**
- Model-free algo for learning the optimal policy
- Take action according to a suitable exploration policy
	- Use $\epsilon-greedy$ policy to collect data
		- With prob $1-\epsilon$ choose the best predicted action that maximizes $Q$
		- With prob $\epsilon$ choose an action uniformly at random
	- soft-max policy
		- …
	- Exploration function
		- Takes into account how many times the $(s,a)$ pair has been tried
- 
---
**Q-learning** is essentially [[Temporal Difference Learning]] TD(0) on the Q function
$$
Q^{\text{new}}(s_k, a_k) = Q^{\text{old}}(s_k, a_k) + \alpha \left( r_k + \gamma \max_a Q^{\text{old}}(s_{k+1}, a) - Q^{\text{old}}(s_k, a_k) \right)
$$
- Off-policy TD(0) learning of the Q function
- Better/faster learning, lower variance
- Can learn from imitation and experience replay
- Need exploration policy (such as $\varepsilon$-greedy for convergence)
---
**SARSA: State-Action-Reward-State-Action**
a variation from the Q-Learning
$$
Q^{\text{new}}(s_k, a_k) = Q^{\text{old}}(s_k, a_k) + \alpha \left( r_k + \gamma Q^{\text{old}}(s_{k+1}, a_{k+1}) - Q^{\text{old}}(s_k, a_k) \right)
$$
- On-policy TD learning of the Q function
---
**Exploration**
- $\varepsilon$-greedy with random actions
- With Exploration Function

---
**Approximate Q-Learning**
[[Approximate Q-Learning]]

---
**Proof for convergence of Q-Learning** (stochastic approximation of a fixed point)
Overall, we show
- deterministic part converge to optimal. ([[Bellman Operator]])
- stochastic part (noise) converge to 0. (Supermartingale Convergence Theorem)
Thus, Q-learning goes to optimal