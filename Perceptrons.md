---
tags:
  - machineLearning
  - perceptron
  - neuralNetwork
  - classification
---
A **linear binary classifier** that separates data into two classes using a **linear decision boundary**.
**Setup**:
- Inputs: feature values
- Weight: for each feature
- Activation: weighted sum, check if $>0$, output (0 or 1)
$$
\text{activation}_w(x)=\sum_i w_i \cdot f_i(x) = w \cdot f(x)
$$
**Review on dot product**:
$$
a \cdot b = \sum_i a_i b_i = |a||b|\cos(\theta)
$$
$\theta < 90^{\circ}$: positive dot prod; $=$: 0; $>$: negative; $\cos(0)=1$, exact same
- positive means positive class
**Binary perception**:
- if $w \cdot f > 0$, predict $+1$
	- if correct, no change
	- else, $w'=w-f$
- elif $w \cdot f < 0$, predict $-1$
	- if correct, no change
	- else, $w'=w+f$
**Multiclass perceptron**: $y=\arg \max_y w_y \cdot f(x)$
- initialize with 0 weights
- if correct, no change
- if wrong, lower wrong class answer by $w_y=w_y-f(x)$, raise correct class by $w_{y^*}=w_{y^*}+f(x)$
**Probabilistic decision instead of Deterministic**:
for $z=w\cdot f(x)$, add sigmoid function $\phi(z)  = 1 / (1+\exp^{-z})$, instead of the binary activation, becomes [[Logistic Regression]]


---
