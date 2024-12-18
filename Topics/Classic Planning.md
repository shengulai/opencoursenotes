---
tags:
  - planning
---
**Definition**: the task of finding a sequence of actions to accomplish a goal in a discrete, deterministic, static, fully observable environment.
**PDDL**: planning domain definition language
- Symbols in First-order [[Logic]]
	- constant symbols (objects): Box1, Truck1, City1
	- predicate symbols (relations): On(x, y), TruckIn(x, y)
	- function symbols: CityDepot(c1) => Depot1
- Domain spec.
	- predicates/functions (symbols): On( ), TruckIn( )
	- object variables (symbols): x
	- fluents (atoms): BoxOn(x,y), things can change over time
	- operators/action schema: Unload(x, y, c)
		- preconditions: BoxOn(x, y), TruckIn(y, c)
		- effect: BoxIn(x, c), $\neg$BoxOn(x, y)
- Problem spec.
	- constants (symbols): Truck1, Paris
	- initial state (set of ground fluents)
	- goal (set of ground fluents)
**STRIPS planning graph**: initial facts -> potential actions -> resulted facts
- Action mutexes (mutual exclusions)
	- inconsistent effects: action1 and action2 lead to conflict outcomes
	- interference: action1 deletes the precondition of action2
	- competing needs: mutually exclusive preconditions
- Literal mutex (inconsistent support): one negates the other (handEmpty and $\neg$handEmpty), or all ways of achieving them via actions are are pairwise mutex
**Relaxed planning graph (RPG)**: remove the mutexes and settle for a suboptimal plan
- Do not delete, do all applicable actions, add all effects, repeat
**Heuristic for RPG**:
- $H_{add}$ add up the levels at which each goal fluent appears; not admissible
- $H_{max}$ max level at which goal fluent appear; admissible but weak
- $H_{ff}$ fast forward (approximate using the RPG), # of actions in a plan from the RPG


---
**References**
[[Artificial Intelligence A Modern Approach (Russell)]] Chapter 11
[Classic STRIP planning notes](https://web.engr.oregonstate.edu/~afern/classes/cs533/notes/strips-intro.pdf)
[GraphPlan notes](https://web.engr.oregonstate.edu/~afern/classes/cs533/notes/graphplan.pdf)
