---
tags:
  - maths/equivalence-class
date-created: 2026-03-28
template-version: m.0
---
[[Maths bits]]
### Relations
#maths/relation
A (binary) *relation* $R$ from $A$ to $B$ is a subset of $A\times B$ where if a pair $(a,b)\in R$ we say that $a$ is related to $b$, and if $(a,b)\not\in R$ $a$ is not related to $b$. Hence
$$
R=\{ (a,b)\,|\,aRb \}
$$
where the notation $aRb$ represents $a$ being related to $b$ ($a\bar{R}b$ is the converse). A relation from $A$ to itself is called a relation *on* $A$.
#### Equivalence relations
A relation $R$ on non-empty set $S$ is called an **equivalence relation** if $R$ is:
- *reflexive*, so for every $a\in A$, $aRa$.
- *symmetric*, so $aRb\iff bRa$.
- *transitive*, so if $aRb$ and $bRc$ then $aRc$.
This could be thought of as classifying objects that are somehow 'alike'. For example, equality is an equivalence relation, as is e.g. similarity of triangles.

If we partition a set $S$ into *cells* $A_{j}$ so that every $a\in S$ is in exactly one cell $A_{j}$, then any element $b\in A_{j}$ is a *representative* of the cell, and any subset $B$ of $S$ that contains exactly one element from each of the cells is a *system of representatives*.

Supposing $R$ is an equivalence relation on $S$, then $\forall a\in S$, the **equivalence class** of $a$, $[a]$ is the set of elements of $S$ to which $a$ is related:
$$
[a]=\{ x\,|\,aRx \}
$$
the collection of all the equivalence classes is the **quotient** of $S$ by $R$:
$$
S /R=\{ [a]\mid a\in S \} 
$$
The most important thing here is that *the quotient set $S /R$ is a partition of $S$*. When we are working with vector spaces we can similarly define the [[Quotient space]].

This means that if we define an equivalence relation on the set then we can partition the set according to which groups of elements are equivalent to each other.