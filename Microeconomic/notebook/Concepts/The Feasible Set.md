---
title: "The Feasible Set"
author: Laplace
tags:
  - economics
  - JCER
date: 2026-09-24
status: Editing
type: Concept
logical_role: definition
---
> [!definition]
> A **feasible set** $B$ contains the consumption bundles that satisfy the constraints faced by the consumer. It is a subset of the The Consumption Set $X$:
>
> $$
> B\subseteq X.
> $$

## Interpretation

$X$ specifies which bundles the model allows us to consider. $B$ specifies which of those bundles the consumer can actually choose under the relevant economic, physical, or institutional constraints. A bundle may belong to $X$ without belonging to $B$.

The definition does not require every feasible set to be a budget set. Affordability is one common constraint; availability or other restrictions can narrow the set further.

## Derivation

Let $C$ be the set of bundles satisfying the constraints in a particular choice problem. Only bundles that are both in $X$ and satisfy those constraints are feasible:

$$
B=X\cap C\subseteq X.
$$

With prices $p=(p_1,\ldots,p_L)$ and income $m$, the ordinary budget constraint is $p\cdot x\leq m$. If this is the only additional constraint, the feasible set is the **budget set**

$$
B(p,m)=\{x\in X:p\cdot x\leq m\}.
$$

If $0\in X$ and $m\geq0$, then $0\in B(p,m)$ because $p\cdot0=0\leq m$. If $X$ is closed and convex, this budget set is also closed and convex: the linear budget inequality defines a closed, convex half-space. These conclusions need not hold for a feasible set defined by different constraints.

## Example

Let $X=\mathbb R_+^2$, $p=(2,1)$, and $m=6$. Then

$$
B(p,m)=\{(x_1,x_2)\in\mathbb R_+^2:2x_1+x_2\leq6\}.
$$

The bundle $(2,2)$ is feasible because it costs $6$. The bundle $(2,3)$ belongs to $X$ but is infeasible because it costs $7$. The bundle $(-1,0)$ is excluded already by $X$.

## Connections

- The consumption set supplies the bundles from which the feasible set is selected.
- A preference relation compares bundles; the consumer's choice problem restricts attention to bundles in $B$.
- Behavioural Assumption specifies how the consumer selects among feasible bundles.
- The zero bundle explains why the ordinary budget set is nonempty when $0\in X$ and $m\geq0$.
