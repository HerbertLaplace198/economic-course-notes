---
title: "Compactness"
author: Laplace
tags:
  - economics
  - JCER
date: 2026-09-24
status: Editing
type: Subconcept
logical_role: definition
---
> [!definition]
> A subset $K$ of a metric space $M$ is **compact** if every cover of $K$ by [[Open Set|open sets]] has a finite subcover. Formally, whenever open sets $\{U_\alpha\}_{\alpha\in A}$ satisfy
>
> $$
> K\subseteq\bigcup_{\alpha\in A}U_\alpha,
> $$
>
> there are finitely many indices $\alpha_1,\ldots,\alpha_m$ such that
>
> $$
> K\subseteq\bigcup_{j=1}^{m}U_{\alpha_j}.
> $$

## Interpretation

However many open sets are used to cover $K$, a finite selection always suffices.

In finite-dimensional Euclidean space $\mathbb R^L$, a set is **compact if and only if it is closed and bounded**. This is the Heine–Borel theorem.

$$
K\subseteq\mathbb R^L\text{ is compact}
\quad\Longleftrightarrow\quad
K\text{ is closed and bounded}.
$$

Here **[[Boundedness|bounded]]** means that $K$ fits inside some ball of finite radius. The equivalence with closedness and boundedness depends on the ambient space; it is not the general definition of compactness in every metric space.

## Example

Use the budget set from The Feasible Set with $X=\mathbb R_+^2$, $p=(2,1)$, and $m=6$:

$$
B(p,m)=\{(x_1,x_2)\in\mathbb R_+^2:2x_1+x_2\leq6\}.
$$

It is nonempty and [[Closedness|closed]]. It is also bounded, because $0\leq x_1\leq3$ and $0\leq x_2\leq6$. Hence it is compact in $\mathbb R^2$.

## Non-example

The consumption set $\mathbb R_+^2$ is closed but unbounded, so it is not compact. The interval $(0,1)\subset\mathbb R$ is bounded but not closed, so it is not compact either. In $\mathbb R^L$, neither property alone is sufficient.

## Related definitions

In a metric space, compactness is also equivalent to **sequential compactness**: every sequence in $K$ has a subsequence converging to a point of $K$. Closedness requires limits of convergent sequences already in $K$ to remain in $K$; it does not ensure that every sequence has a convergent subsequence.

A closed ball in $\mathbb R^L$ is compact because it is closed and bounded. A closed ball in an arbitrary metric space need not be compact.

## Used in

- A feasible set: a budget set with finite income and strictly positive prices is compact when $X=\mathbb R_+^L$.
- Behavioural Assumption: if $B$ is nonempty and compact and a utility function $u$ is continuous on $B$, the Weierstrass theorem guarantees an $x^*\in B$ maximizing $u$. Compactness helps establish **existence**, not uniqueness, of an optimal choice.
