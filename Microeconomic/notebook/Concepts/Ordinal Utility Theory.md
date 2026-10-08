---
title: Ordinal Utility Theory
author: Laplace
tags:
  - economics
  - JCER
date: 2026-09-23
status: Editing
type: Concept
logical_role: definition
---
> [!definition]
> An **ordinal utility function** $u:X\to\mathbb R$ represents the preference relation $\succeq$ on The Consumption Set $X$ if, for every $x,y\in X$,
>
> $$
> x\succeq y\iff u(x)\geq u(y).
> $$
>
> Only the ranking represented by these numbers matters.

## Interpretation

The value $u(x)$ labels the position of bundle $x$ in the preference ranking. Its level, differences from other utility values, and ratios of utility values do not measure how much more the consumer likes one bundle. Changing the labels without changing their order leaves the represented preferences unchanged.

## Derivation

Let $\phi$ be a [[Monotonic Transformation|strictly increasing transformation]] on the range of $u$, and define $\tilde u=\phi\circ u$. Then

$$
x\succeq y
\iff u(x)\geq u(y)
\iff \phi(u(x))\geq\phi(u(y))
\iff \tilde u(x)\geq\tilde u(y).
$$

Thus, $u$ and $\tilde u$ represent the same preferences and select the same most preferred bundles from any given feasible set.

If $u$ and $\phi$ are differentiable, $\phi'(u(x))>0$, and the denominator below is nonzero, the chain rule also gives

$$
\frac{\partial\tilde u/\partial x_1}
     {\partial\tilde u/\partial x_2}
=
\frac{\phi'(u)\,\partial u/\partial x_1}
     {\phi'(u)\,\partial u/\partial x_2}
=
\frac{\partial u/\partial x_1}
     {\partial u/\partial x_2}.
$$

The individual marginal utility numbers may change, while their ratio—and therefore the marginal rate of substitution—does not.

## Connections

- A preference relation is the ranking represented by an ordinal utility function.
- [[The Representation Theorem]] gives sufficient conditions for a continuous ordinal utility representation to exist.
- Cardinal Utility theory gives additional meaning to utility differences; ordinal utility uses only their ordering.
- Quasi-concave utility remains quasi-concave under a strictly increasing transformation, consistent with its link to Convex Preferences.
