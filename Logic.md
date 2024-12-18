---
tags:
  - logic
---
**Syntax**: what sentences are allowed; how it should be formed
- ex: “x +y=4” is a well-formed sentence, whereas “x4y+=” is not
- $\neg$ not (negation); 
- $\land$ and (conjunction); $\lor$ or (disjunction)
- $\implies$ implies (implication)
- $\iff$ iff (biconditinoal)
**Semantic**: truth of each sentence w.r.t. each possible world
	ex: the semantics for arithmetic specifies that the sentence “x +y=4” is true in a world where x is 2 and y is 2
**Entailment**: a sentence follows logically from another sentence 
	$\alpha \models \beta$ -> $\alpha$ entails $\beta$ iff. in every model in which $\alpha$ is true, $\beta$ is also true
![[Screenshot 2024-12-16 at 9.17.51 AM.png]]
**Propositional logic**:  
![[Screenshot 2024-12-16 at 9.22.13 AM.png]]
**First-order logic**: adds universal quantifier  $\forall$ and existential quantifier $\exists$. More expressive.
![[Screenshot 2024-12-17 at 8.59.08 AM.png]]

**Proof**: a demonstration of entailment
- sound: the conclusion logically follows the premises
- complete: the premises are also proved
**Satisfiability**: if a sentence is true in at least one world
**Conjunctive normal form (CNF)**: in the form shown in step 4 below
![[Pasted image 20241216094443.png]]
**DPLL solver**: solves like a recursive depth first tree search, in addition:
![[Screenshot 2024-12-16 at 10.13.16 AM.png]]
