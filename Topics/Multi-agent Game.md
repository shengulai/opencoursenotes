---
tags:
  - multiAgent
  - search
---
**Deterministic Game**:  the outcome of each action is fully predictable and determined
**Stochastic Game**: the outcome of an action depends on a probabilistic process

**Zero-sum Game**: agents has opposite utility: one max, the other min
**General-sum Game**: independent utilities
___
**Adversarial Search (Minimax)**
![[Pasted image 20241029112230.png|500]]
- ==deterministic== and ==zero-sum== games
**Alpha-beta Pruning**
- store an $\alpha$ value which is the max from the min node
- store an $\beta$ value which is the min from the max node
- cut the branch if $\beta < \alpha$
**Depth-limited Search**
- replace terminal value with a evaluation function
**Expectimax Search**
- chance node instead of the min node in the figure above: expectation of the children
- need to know all children values to compute the $\mathbb{E}$
[[Monte Carlo Tree Search (MCTS)]]

---
**References**
