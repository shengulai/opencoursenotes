---
tags:
  - machineLearning
  - optimization
  - gradient
---
**Gradient algorithm**:
- consider $g(w_1,w_2)$
- update (sign depends on Descent or Ascent)
	$$
	\begin{align}
	w_1 & \leftarrow w_1 \pm \alpha *\frac{\partial g}{\partial w_1}(w_1, w_2) \\
	w_2 & \leftarrow w_2 \pm \alpha *\frac{\partial g}{\partial w_2}(w_1, w_2) \\
	\end{align}
	$$
**Variations**:
- Batch gradient descent: single precise step, but slow, could stuck in local minima
- Stochastic gradient descent: fast and noisy, can help escape local minima, less soomth
- Mini-batch gradient descent: balance between two, good for GPU, require tuning
