---
title: "Transitivity"
author: Laplace
tags:
  - economics
  - JCER
date: 2026-09-26
status: Editing
type: Subconcept
logical_role: assumption
---
> [!definition] Axiom 2 — Transitivity
> Let $\succeq$ be a binary relation on the consumption set $X$. It is **transitive** if, for every $x,y,z\in X$,
>
> $$
> x\succeq y\ \text{and}\ y\succeq z
> \quad\Longrightarrow\quad
> x\succeq z.
> $$

## Interpretation

Transitivity makes comparisons consistent along a chain: if $x$ is at least as good as $y$, and $y$ is at least as good as $z$, then $x$ must be at least as good as $z$. The condition applies to **every** triple of bundles, including cases in which two bundles are indifferent.

It differs from **completeness**. Completeness asks whether every pair can be compared; transitivity asks whether comparisons already made fit together. Neither condition implies the other.

## Example

On $X=\mathbb R_+^2$, define coordinatewise dominance by

$$
x\succeq y
\quad\Longleftrightarrow\quad
x_1\geq y_1\ \text{and}\ x_2\geq y_2.
$$

If $x\succeq y$ and $y\succeq z$, then $x_j\geq y_j\geq z_j$ for $j=1,2$; hence $x\succeq z$. The relation is transitive, but it is **not complete**: $(1,0)$ and $(0,1)$ are incomparable. This shows that transitivity alone does not guarantee rationality in the usual consumer-theory sense.

## Non-example

Let $X=\{a,b,c\}$. Suppose each bundle is at least as good as itself, and the only comparisons between distinct bundles are

$$
a\succeq b,\qquad b\succeq c,\qquad c\succeq a.
$$

Every pair can be compared, so this relation is complete. But $a\succeq b$ and $b\succeq c$ while $a\not\succeq c$; it is **not transitive**. The three comparisons form a cycle.

## Related definitions

In consumer theory, a relation is usually called **rational** when it is both complete and transitive. The two assumptions serve different purposes and must be checked separately.

Transitivity is necessary for representation by a real-valued utility function. If $x\succeq y$ exactly when $u(x)\geq u(y)$, then

$$
x\succeq y,\ y\succeq z
\quad\Longrightarrow\quad
u(x)\geq u(y)\geq u(z)
\quad\Longrightarrow\quad
x\succeq z.
$$

Transitivity alone does not ensure that a utility representation exists. It also implies that the derived indifference relation is transitive. If $x\sim y$ and $y\sim z$, transitivity in both directions gives $x\succeq z$ and $z\succeq x$, hence $x\sim z$.

## Used in

- [[PREFERENCE RELATION]]: transitivity, together with completeness, is the rationality assumption used to derive properties of strict preference and indifference.
