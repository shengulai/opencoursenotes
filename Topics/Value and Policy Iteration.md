---
tags:
  - reinforcementLearning
  - dynamicProgramming
---
From [[Value Functions]] to [[Bellman Equation]], now we can do value or policy iteration to solve for [[Markov Decision Process (MDP)]] under the big idea of [[Dynamic Programming]].
___
**Value Iteration** 
$$
\begin{align}
V_{k+1}(s) &= \mathcal{T}V_k = \max_a \sum_{s'} P(s' | s, a) \left( R(s', s, a) + \gamma V_k(s') \right) \\
\pi^*(s) &= \arg\max_a \sum_{s'} P(s' | s, a) \left( R(s', s, a) + \gamma V^*(s') \right)
\end{align}
$$
Guarantee: $V_t \to ^*V$, $V^{\pi_t}\to V^*$ with greedy policy $\pi_t$
1. Update the value function $V$ till converge
2. Compute the policy from $V^*$
Note: We can also extract from the $Q(s,a)$ function, this enables model-free RL; if doing approximation, no guarantee to optimality anymore

For a **greedy policy $\pi$**, we can prove that
$$
||V^*-V^{\pi}||_{\infty} \leq \frac{2\gamma}{1-\gamma}||V^*-V||_{\infty}
$$
___
**Policy Iteration**

$$
\begin{align}
V_{t+1}^{\pi}(s) &= \mathcal{T}^{\pi_t}V_t^{\pi_t} = \mathbb{E} \left( R(s', s, \pi(s)) + \gamma V_t^{\pi}(s') \right) \\
&= \sum_{s'} P(s' | s, \pi_t(s)) \left( R(s', s, \pi_t(s)) + \gamma V^{\pi}(s') \right) \\
\pi_{t+1}(s) &= \arg\max_a \mathbb{E} \left( R(s', s, a) + \gamma V^{\pi_t}(s') \right)
\end{align}
$$
Guarantee: $V^{\pi_t+1} \geq V^{\pi_t}$, $V^{\pi_t}\to V^*$ with greedy policy $\pi_{t+1}$
1. Evaluate the policy
2. Update the policy
Note: Policy typically converges before value converges

