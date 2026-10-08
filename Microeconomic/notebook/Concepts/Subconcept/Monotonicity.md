---
title: "Monotonicity"
author: Laplace
tags:
  - economics
  - JCER
date: 2026-09-26
status: Editing
type: Subconcept
logical_role: assumption
---
> [!definition] Axiom 4 — Strict Monotonicity (lecture)
> On $X=\mathbb R_+^n$, the lecture requires, for all $x^0,x^1\in X$,
>
> $$
> x^0\geq x^1\quad\Longrightarrow\quad x^0\succeq x^1,
> \qquad
> x^0\gg x^1\quad\Longrightarrow\quad x^0\succ x^1.
> $$
>
> Here $x^0\geq x^1$ means $x^0_j\geq x^1_j$ for every good $j$; $x^0\gg x^1$ means $x^0_j>x^1_j$ for **every** good $j$.

## Interpretation

The first implication is weak monotonicity: more of some goods, with no decrease in the others, cannot make the consumer worse off. The second implication says that increasing **every** good makes the bundle strictly better. Axiom 4 does not demand strict preference when only one good increases.

A stronger convention, also sometimes called *strict monotonicity*, requires

$$
x^0\geq x^1,\quad x^0\ne x^1
\quad\Longrightarrow\quad x^0\succ x^1.
$$

The distinction matters: the stronger version requires strict improvement when **at least one** good increases and the others do not fall. The lecture calls the weaker pair of implications above Axiom 4, “Strict Monotonicity.” Both conditions concern goods rather than possible bads.

## Example

On $X=\mathbb R_+^2$, $u(x_1,x_2)=x_1+x_2$ satisfies both Axiom 4 and the stronger convention. If $x^0\geq x^1$ and $x^0\ne x^1$, at least one coordinate rises, so $u(x^0)>u(x^1)$.

The utility function $u(x_1,x_2)=\min\{x_1,x_2\}$ satisfies **Axiom 4 but not the stronger convention**. If both coordinates rise strictly, their minimum rises strictly. Yet $(2,1)\geq(1,1)$ while both bundles give utility $1$.

## Non-example

The utility function $u(x_1,x_2)=x_1-x_2$ violates even the weak part of Axiom 4: $(0,1)\geq(0,0)$, but $u(0,1)=-1<0=u(0,0)$.

## Related definitions

On $X=\mathbb R_+^n$, Axiom 4 implies [[Local Non-satiation]]. Given any $x\in X$ and $\varepsilon>0$, choose $\delta>0$ small enough that $\|\delta\mathbf 1\|<\varepsilon$ and set $y=x+\delta\mathbf 1$. Then $y\gg x$ and hence $y\succ x$. On a domain with a top boundary, this argument can fail because the required $y$ may lie outside $X$.

Local non-satiation need not imply weak monotonicity: on $\mathbb R_+^2$, $u(x_1,x_2)=x_1-x_2$ is locally non-satiated because $x_1$ can always be increased slightly.

## Used in

- [[PREFERENCE RELATION]]: Axiom 4 rules out the upward-bending indifference curve shown in lecture Fig. 1.4.
- [[Local Non-satiation]]: on $\mathbb R_+^n$, Axiom 4 is sufficient for local non-satiation.
