**CSP definition**:
- $\mathcal{X}$ a set of variables, $\{X_1,...X_n\}$
- $\mathcal{D}$ a set of domain, $\{D_1,...D_n\}$ for each variable
- $\mathcal{C}$ a set of constraints
**Backtracking search**: DFS + variable-ordering + fail-on-violation
**Constraint propagation**: use constraint to reduce number of legal values for a variable
- node consistency (unary): reduce the domain for a variable
- arc consistency (binary): reduce the domain for a variable because of another variable
- path consistency (triple)
- k-consistency: for each k node, assignment to k-1 extend to the k th node
**Ordering**: which unassigned variable to select next
- minimum remaining values
- least constraining value (one that rules out fewest values in the remaining variables)


