---
tags:
  - bayes
---
**Bayes nets encode joint distribution as product on conditional on each node**
$$
P(X_1,...X_n) = \prod_{i=1}^nP(X_i | \text{Parent}(X_i))
$$
**Operations for the Conditional Probability Tables (CPT)**
- Pointwise product 
	- $P(A)P(J|A) \to P(A,J)$
	- $P(A,J)P(A,M) \to P(A,J,M)$
- Summing out (variable elimination)
	- $P(A,J) \to P(A)$

**Approximate Inference for Bayesian Network**
Introduced in Chapter 13.4 [[Artificial Intelligence A Modern Approach (Russell)]]
- Direct sampling
	- ==Prior sampling==
		- the sampling procedure is consistent (more samples get to true distribution)
	- ==Rejection sampling==
		- stop if unwanted evidence is seen (if unlikely evidence, a lot of sample rejections)
		- can't answer all query
	- Importance sampling (weight )
		- ==likelihood weighting==
			- weight each sample by probability of evidence given parents
			- it is consistent
- Markov Chain Monte Carlo (MCMC)
	- ==Gibbs sampling==
		- it is consistent
		- fix the evidence, pick a variable and sample a value conditioned on all other variables in the Markov Blanket (its parents, children, and it's children's parents)
		- can be complied and run fast, can run asynchronously in parallel

**Conditional Independence for Nodes**
![[Screenshot 2024-10-29 at 8.09.39 PM.png|500]]

if $X$ and $Y$ are conditionally independent given $Z$, then $P(X|Z)=P(X|Y,Z)$



---
**References**
[Notes from CMU](https://www.cs.cmu.edu/~./15281/coursenotes/bayesnets/index.html)
[Bayes Net Independ. and Infer. Note](https://www.cs.cmu.edu/~awm/15781/slides/bayesinf05a.pdf)
