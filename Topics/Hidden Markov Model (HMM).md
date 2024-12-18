---
tags:
  - HMM
  - markov
---
From the [[Markov Process]] (Markov Model), observe evidence not the true state
![[Pasted image 20241029193236.png|300]]
**Joint distribution adjustment**
$$
\begin{align}
\text{Markov model:} \quad P(X_0,\dots X_T) &= P(X_0)\prod_{t=1:T}P(X_t|X_{t-1}) \\
\text{HMM:} \quad P(X_0,\dots X_T) &= P(X_0)\prod_{t=1:T}P(X_t|X_{t-1})P(E_t|X_t)
\end{align}
$$

**Inference tasks**
![[Pasted image 20241029193711.png|400]]

**Filtering** 
$$
P(X_{t+1}|e_{1:t+1}) =\alpha P(e_{t+1}|X_{t+1})\sum_{X_t}P(X_t|e_{1:t})P(X_{t+1}|X_t) 
$$
where $\alpha$ is the normalization, next Update (add in evidence), next Predict (state transition)
without the new evidence coming, it just becomes **Prediction**
**Smoothing**
**Mostly likely explanation**
	- Forward Algorithmn
	- Viterbi Algorithm



---
**References**
