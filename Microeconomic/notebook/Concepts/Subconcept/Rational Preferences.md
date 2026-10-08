---
title: Rational Preferences
author: Laplace
tags:
  - economics
  - JCER
date: 2026-09-26
status: Editing
type: Subconcept
logical_role: assumption
---
> [!definition]
> A preference relation $\succeq$ on a consumption set $X$ is **rational** if it is both [[Completeness|complete]] and [[Transitivity|transitive]]:
>
> $$
> \begin{aligned}
> \text{Completeness:}\quad
> &\forall x,y\in X,\quad x\succeq y\ \text{or}\ y\succeq x;\\[0.8em]
> \text{Transitivity:}\quad
> &\forall x,y,z\in X,\quad
> (x\succeq y\ \text{and}\ y\succeq z)
> \Longrightarrow x\succeq z.
> \end{aligned}
> $$

## Interpretation

Rationality is a property of the **ranking relation**. Completeness ensures that every pair of bundles can be compared, while transitivity ensures that comparisons fit together across triples. Both comparisons may hold for a pair, so rationality permits indifference.

This definition does not assert that the consumer has perfect information, performs calculations, or actually chooses a best feasible bundle. The rule that choice selects a most-preferred feasible bundle is a separate behavioural assumption. Rationality also does not by itself imply continuity, convexity, or the existence of an optimal bundle.

Because completeness applies even when $x=y$, a rational preference relation is reflexive: $x\succeq x$ for every $x\in X$.

## Example

On $X=\mathbb R_+^2$, let $u(x)=x_1+x_2$ and define

$$
x\succeq y\quad\Longleftrightarrow\quad u(x)\geq u(y).
$$

Any two real utility values can be compared, so the relation is complete. If $x\succeq y$ and $y\succeq z$, then $u(x)\geq u(y)\geq u(z)$, giving $x\succeq z$; it is transitive. Bundles with equal utility are indifferent.

## Non-example

**Transitive but incomplete.** On $\mathbb R_+^2$, coordinatewise dominance is defined by $x\succeq y$ when $x_j\geq y_j$ for both goods $j=1,2$. It is transitive, but $(1,0)$ and $(0,1)$ cannot be compared, so it is not rational.

**Complete but intransitive.** On $X=\{a,b,c\}$, let every bundle be related to itself, and let the only comparisons between distinct bundles be $a\succeq b$, $b\succeq c$, and $c\succeq a$. Every pair can be compared, but $a\succeq b$ and $b\succeq c$ do not imply $a\succeq c$. This relation is not rational either.

## Related definitions

A complete and transitive weak preference relation is also called a **total preorder**. Its derived indifference relation $\sim$ is an equivalence relation, and its strict part $\succ$ is irreflexive and transitive. The proofs follow from the definitions of $\sim$ and $\succ$ in the Preference Relation note.

Any real-valued utility representation $x\succeq y\iff u(x)\geq u(y)$ implies rationality, since the order $\geq$ on $\mathbb R$ is complete and transitive. On a finite $X$, the converse holds: rank the finitely many indifference classes and assign each class a number. On a general infinite domain, rationality alone need not guarantee a real-valued utility representation.

Even when a rational relation has a utility representation, a best feasible bundle need not exist. For example, with $X=[0,1]$, $B=(0,1)$, and $u(x)=x$, the preference relation is rational but no $x\in B$ maximizes $u$ over $B$.

## Used in

- Preference Relation: rationality names the joint completeness-and-transitivity assumption used to derive properties of strict preference and indifference.
