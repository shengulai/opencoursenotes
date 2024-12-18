---
tags:
  - optimization
  - LP
---
**Simplex process**
Step 0: standard LP form
Step 1: add slack variables to transfer inequality to equality constraints
- max $4x_1+x2$ becomes max $z$, s.t. $z-4x_1-x_2=0$
- $x_1+x_2\leq 3$ becomes $x_1+x_2+s_1 = 3$, all variables $\geq 0$
Step 2: setup simplex tableau
	![[Screenshot 2024-12-16 at 2.07.55 PM.png|250]]
Step 3: pivoting non-basic variable (improving)
- pick the smallest non-basic variable (column) in the last row
- pick the row that has the smallest ratio (1st row 2/2=1; 2nd, 3rd row = 4)
- stop until no negative values in the objective (last) row
- the value of b for the row where the variable is 1, is the optimal value for the variable


---
**Reference**:
[Simplex algorithm Computational Optimization Open Textbook](https://optimization.cbe.cornell.edu/index.php?title=Simplex_algorithm)
