---
tags:
  - optimization
  - MILP
---
**MILP standard form**:
$$
\begin{align}
\max \quad & z=c^{\top}x+d^{\top}y \\
\text{s.t} \quad & Ax+By = b \\
& x,y \geq 0 \\
& x \in \mathbb{Z}
\end{align}
$$
**Properties**:
- Fewer feasible solutions than LP
- Can't be solved in polynomial time
- Solving associated LP generates the best possible solution
**Modeling disjunctive constraints**:
- using a binary activation variable $f_1(y)$, $f_2(1-y)$; $y=0$, $f2$ active, $y=1$, $f1$ active
**Algorithms**:
- [[Branch and Bound]]



---
**References**
