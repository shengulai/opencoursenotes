---
tags:
  - search
  - algorithm
  - AI
  - autonomousSystem
---
## Search Overview

**A search problem consists of**
- State space
- Actions (with associated cost)
- Successor function (transition model)
- Start state & Goal test / Goal state
**Solution for a search problem is**
- a sequence of Actions (a plan)
**Reflex agent (What the world is)**
- Choose action based on current percept and/or memory
- Do not consider future consequences
**Planning Agent (What the world would be)**
- Decisions based on (hypothesized consequences of actions)
- Has a goal test
---
## Informed and Uninformed Search
 - **Informed Search (heuristic)**: can estimate how far from goal; hint comes in the form of a heuristic function $h(n)$
	 - Greedy best-first search: which next state is closer to goal based on $h(n)$
		 - Complete for finite spaces; Not Optimal
	 - A* search: backward cost from initial node to $n$ ($g(n)$) + estimated cost from $n$ to goal ($h(n)$), $f(n)=g(n)+h(n)$; extended to Bidirectional A*
		 - Complete; Optimal with admissible/consistent heuristic
	 - Iterative deepening A* (IDA*), Recursive best-first search (RBFS), Simplified memory-bounded A*(SMA*), Beam search, Weighted A*, and more...
 - **Uninformed Search: no such estimate**
	- Breadth-first search (BFS, FIFO Queue) list.pop(0)
		- complete; optimal if costs are identical
	- Dijkstra's algorithm
		- Uniform-cost search(AI community calls this), or Best-first search
	- Depth-first search (DFS, LIFO Stack)
		- Complete if finite; Not Optimal
	- Depth-limited and iterative deepening search
		- limit on the depth
		- iteratively increase the limit on the depth
	- Bidirectional search
		- search from both initial and goal state
**Notes on Heuristics**
- Admissibility
	- Admissible (Optimistic) : never overestimate the cost
	- Inadmissible (Pessimistic)
- Consistency of heuristic (estimated heuristic cost $\leq$ actual costs)
	- consistency implies admissibility
- Best heuristic is the actual cost; Worst is 0
Mentioned in [[Artificial Intelligence A Modern Approach (Russell)]] Chapter 3
___
## Search for Motion Planning

Detail algorithms in [[Motion Planning]]

___
## Multi-agent Game

[[Minimax Search]]
[[Expectimax Search]]

---
## References


