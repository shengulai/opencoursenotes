---
tags:
  - bellmanEquation
  - reinforcementLearning
  - dynamicProgramming
  - markov
  - math
---
**Bellman equation** can vary from system to system (deterministic vs. stochastic, finite vs. infinite). Overall, the idea is to have a recursion that connects a value (utility) $V$ from one state to another! It enables optimal solution!!!!

> [!NOTE] Bellman Equation (one version)
> $$
> \begin{align}
> V(s) &= \max_a \left(r(s,a) + \gamma\sum_{s'}P(s'|s,a)V(s')\right) \\
> \end{align}
> $$

To use the Bellman equation for finite (state and action spaces) discounted problems through [[Dynamic Programming]] using [[Value and Policy Iteration]]. Going into the ==Quality Function== (==Action-value function== $Q(S,A)$) we can start to do model-free reinforcement learning [[Q-Learning]]! Cool!

In addition, [[Bellman Operator]] is used to represent the $\max$ operation.
___

For fixed-policy Bellman Equation consider a finite [[Markov Decision Process (MDP)]]: 
$$
V_t^\pi(s) = c_t(s, \mu_t(s)) + \sum_{s{\prime}} p_t(s{\prime}; s, \mu_t(s)) V_{t+1}^\pi(s{\prime}), \quad \forall s \in \mathcal{S}
$$
where it is formulated as the cost minimization problem. Thus, at end time $T$:
$$
V_T^\pi(s)=c_T(s), \quad \forall s \in \mathcal{S}
$$
For an optimal policy: $V_t^\pi=V_t^*$,  we have: 
$$
V_t^*(s) = \min_{a \in \mathcal{A}_t(s)} \left\{ c_t(s, a) + \sum_{s'} p_t(s'; s, a) V_{t+1}^*(s') \right\}, \quad \forall s \in \mathcal{S}
$$
___
For discounted [[Markov Decision Process (MDP)]] #mdp
$$
\begin{align}
V_{\pi}(s) &= \mathbb{E}\left(\sum_t\gamma^tr_t|s_0=s\right) \\
V(s) &= \max_\pi \mathbb{E}\left(\sum_t^{\infty}\gamma^tr_t|s_0=s\right) \\
&= \max_\pi \mathbb{E}\left(r_o+\sum_{t=1}^{\infty}\gamma^tr_t|s_1=s'\right) \\
V(s)&= \max_\pi \mathbb{E}(r_0+\gamma V(s')) \\
\pi &= \arg \max_\pi \mathbb{E}(r_0+\gamma V(s'))
\end{align}
$$
From the value function $V(s)$, we can always extract the policy $\pi$ as the policy that maximizes the value function.
___
Another version of summary from [[MIT_16.410_AutoSys_DecsMaking]]
![[Pasted image 20241029170230.png]]
