---
tags:
  - optmization
  - LP
---
**LP standard form**
$$
\begin{align}
\max \quad & z=c^{\top}x \\
\text{s.t} \quad & Ax \leq b \\
&x \geq 0
\end{align}
$$
equivalent of
$$
\begin{align}
\min \quad & -c^{\top}x \\
\text{s.t} \quad & Ax = b \\
&x \geq 0
\end{align}
$$
**Geometric representation**: 
- optimal solution always on the corners of the feasible region, no interior solution
- Computational complexity of generating corner points in a LP is O(n³)
**Ill-formed LP**: 
- empty feasible region (no solution)
- unbounded feasible region (infinite utility)
- non-convex feasible region
**Corner-point optimality**:
- ==If a feasible corner-point has no better neighbor, it is optimal==
**Algorithm for LP**:
- [[Simplex Algorithm]]

---
