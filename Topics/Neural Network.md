---
tags:
  - AI
  - algorithm
---
![[Screenshot 2024-12-16 at 7.40.27 PM.png]]
**In matrix form**:
$$
\phi(x\times W_1) = h, \quad \phi(h\times W_2)=y
$$
Note the shape of the matrices $x(1,3), W_1(3,2), h(1,2), W_2(2,1), y(1,1)$ 
3 is dimension of input; 2 is dimension of hidden layer (hidden neurons); 1 is dimension of output

**Activation functions**:
sigmoid, hyperbolic tangent, rectified linear unit (RuLU), ...
![[Screenshot 2024-12-16 at 7.45.55 PM.png]]

**Learning**: same basic idea as [[Maximum Likelihood]]
$$
\max_w ll(w)=\max_w\sum_i\log P(y_i|x_i;w)
$$
$w$ here are set of all parameters, many times written as $\theta$
**Binary classification**:  using the binary cross-entropy, [[Entropy of Information]]
$$
\log\text{loss} = - \sum_i y_i\log(p_i)+(1-y_i)\log(1-p_i)
$$
where $y_i$ is the true binary label, $p_i$ is the prob. of positive class by classifier
use methods like [[Gradient Descent (Ascent)]] to optimize the weights $w$ with learning rate $\alpha$
$$
w \leftarrow w - \alpha \Delta\log\text{loss}(w)
$$
**Backpropagation**: autodiff done using tools PyTorch Tensorflow

**Neural Networks Properties**: Theorem (Universal function approximators)
A two-layer NN with sufficient number of neurons can approximate any continuous function to any desired accuracy.

**Consistency**: predicts better;  can risk overfit
**Simplicity:** fewer layers, neurons; reduce computation cost; prevent overfittting
- early stopping
- weight regularization (add penalty to weight magnitude)
- dropout (neurons)


---
**Types of layer**
- Dense (fully connected)
- Convolutional
- Pooling
- Recurrent
- Normalization
- ...