---
tags:
  - markov
  - reinforcementLearning
  - dynamicProgramming
  - math
---
**MDP** continuing from the [[Markov Process]] with added feature of decision making
___
**MDP** (controlled markov process) has the state transition is affected by the action $a$: 
$$
S_{t+1}=f_t(S_t,a,W_t)
$$
with a **policy** $\pi_t: s_t \to a_t$ and transition kernel representation: 
$$
p_t(s';s,a)=\mathbb{P}(f_t(s,a,W)=s')
$$
___
For a **cost function**: $C_t = c_t(s_t,a_t)$, the cost-to-go (value function / state-value function) of policy $\pi$ is: 
$$
V_t^\pi(s)=\mathbb{E}_{t,s}^\pi[C_t+C_{t+1}+...+C_T]
$$
and there exists an **optimal value function**: 
$$
V_t^*(s)=min_\pi V_t^\pi(s)
$$
**Discounting for infinite horizon** can make sure the reward is bounded
$$
V = \sum_{t=0}^{\infty}\gamma^tC_t
$$
Inversely, it can be a **reward** $R_t=r_t(s_t,a_t)$ maximization. More detail on [[Value Functions]]
___
Goal: Given initial state distribution $\mu$, fin a policy $\pi(s)$ that maximizes $\mathbb{E_{\tau}}[R(\tau)|\pi,\mu]$, where the **trajectory** $\tau=(s1,a1,s2,a4,...)$
___
**Additionally**
- Further representing the state-action pair by the $Q(s,a)$ where $Q^*$ is the optimal.
- To solve , we get to [[Value and Policy Iteration]]
- History-based vs. memoryless policies
