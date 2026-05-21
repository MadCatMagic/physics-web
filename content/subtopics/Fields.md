---
tags:
  - linalg/field
date-created: 2026-03-29
template-version: m.0
---
[[Maths bits]]

A field $\mathbb{F}$ is a three-tuple $(S,+,\cdot)$ which contains a set of objects (called *scalars*) $S$, a scalar addition $+$, and a scalar multiplication $\cdot$. They must satisfy the following properties to be a field:
- The sum $a+b\in S$ for $a,b\in S$ is 
	- *commutative* $a+b=b+a$, 
	- *associative* $(a+b)+c=a+(b+c)$,
	- exists a unique scalar $0$ s.t. $a+0=a,\,\forall a\in S$ (identity), 
	- exists for every non-zero scalar a $-a$ s.t. $a+(-a)=0$ (inverse).
- The product $ab\in S$ for $a,b\in S$ is:
	- *commutative*,
	- *associative*,
	- exists a unique scalar $1$ s.t. $1\cdot a=a$ (identity),
	- exists for every non-zero scalar a $a^{-1}$ s.t. $a\cdot a^{-1}=1$ (inverse).
- Multiplication is distributive over addition, $a(b+c)=ab+ac$.

Any set of objects that satisfies these conditions for a given addition and multiplication operator is a **field**.