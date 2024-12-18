---
tags:
  - reinforcementLearning
  - AI
---
## Overview
![[Pasted image 20241013094807.png|600]]

- RL fits in the framework of [[Markov Decision Process (MDP)]]
- Similar to [[Dynamic Programming]] as optimal sequential decision making under uncertainty, with model-free approach approximated by neural networks. RL becomes like a “Sampled approximate DP”
---
**Key attributes for RL:**
- **online vs. offline**: compute policy as experience come vs. as ahead of time
- **passive vs. active**:  use past experience vs. interact with new experience (explore)
- **model-based vs. model-free**: learn the models (T, R, ..) vs. learn V, Q
- **on-policy vs. off policy**: explore and learn using same policy vs. different policy
---
- [[Value and Policy Iteration]]
- [[Imitation Learning]]

## Policy Evaluation / Value estimation / Prediction
From policy $\pi$ to $V$
- Model-based policy evaluation
	- [[Dynamic Programming]] uses the system dynamics to iterate until $V$ or $Q$ converge
		![[Screenshot 2024-10-13 at 10.53.05 AM.png|200]]
- Model-free policy evaluation
	- [[Monte Carlo Learning]] sample for the next state till ht goal state, then update backwards
		![[Screenshot 2024-10-13 at 10.53.35 AM.png|200]]
	- [[Temporal Difference Learning]] sample until next state, update immediately
		![[Screenshot 2024-10-13 at 10.54.21 AM.png|200]]
- 
## Policy Improvement / Learning / Control
from $V$ to policy $\pi$
- [[Q-Learning]]
- [[Approximate Q-Learning]]
- [[Proximal Policy Optimization (PPO)]]
- 
## Exploration
**Epsilon-greedy method**
- with probability $\epsilon$, choose random actions; otherwise act on current policy $0<\epsilon<1$
**Exploration function**
- explore areas whose badness is not yet established
**Regret**: measure of total mistake cost


___
## Literature
An overview of RL algorithms provided by[[AlMahamid2021_RL_Algo]]

Model-based RL review
[[Moerland_2022_model_based_rl_survey]]

Physics informed RL
[[Banerjee_2023_RL]]

RL in building control
[[Han_2022_RL_RadiantFloorHeating]]

___
## Textbook for RL
[[Reinforcement Learning An Introduction (Richard)]]
[[Dynamic Programming and Optimal Control (Dimitri)]]
[[Neural Dynamic Programming (Dimitri)]]

___
## RL Class
- [[MIT_6.7920_RL_F&M]]
- [[Algorithms for Reinforcement Learning (Lecture Notes)]]

___
## Resources
[OpenAI Spinning Up in Deep RL](https://spinningup.openai.com/en/latest/index.html)

![[Screenshot 2024-07-06 at 9.36.56 AM.png|300]]
![[Screenshot 2024-09-30 at 10.15.30 PM.png|350]]

---
## Implementing RL
- For research and prototype: [CleanRL]([https://docs.cleanrl.dev](https://docs.cleanrl.dev/))
- For scaling up: [RLlib](https://docs.ray.io/en/latest/rllib/index.html)
- 