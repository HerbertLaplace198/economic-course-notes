---
title: "The Consumption Set"
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
> The **consumption set** $X$ is the set of consumption bundles allowed in a consumer model. It specifies which bundles can be considered before prices and income restrict the consumer's choices.

## Interpretation

A bundle $x\in X$ belongs to the model's domain of choice; it need not be affordable. The preference relation compares bundles in $X$, and a utility function, when one exists, is defined on $X$.

In the standard model used here, $X$ is assumed to satisfy four conditions:

$$
X\subseteq\mathbb R_+^L,\qquad
X\text{ is closed},\qquad
X\text{ is convex},\qquad
0\in X.
$$

- **[[Non-negative consumption|Non-negative quantities]]:** No bundle in $X$ contains a negative amount of a good.
- **[[Closedness]]:** If bundles in $X$ converge to a limit, that limit remains in $X$.
- **[[Convexity]]:** Every mixture $\lambda x+(1-\lambda)y$ of bundles $x,y\in X$, for $\lambda\in[0,1]$, also belongs to $X$.
- **[[The Zero Bundle|Zero bundle]]:** Consuming nothing is included as a possible bundle; it need not be preferred.

These are assumptions of this model, not properties that every consumption set must have. For example, $X=\mathbb Z_+^2$ describes indivisible goods but is not convex.

## Derivation

Suppose there are $L$ infinitely divisible goods, each consumed in a nonnegative quantity. A bundle is a vector

$$
x=(x_1,\ldots,x_L),\qquad x_\ell\geq 0
\quad\text{for every }\ell.
$$

If there are no other restrictions, the model takes

$$
X=\mathbb R_+^L
=\{x\in\mathbb R^L:x_\ell\geq 0\text{ for every }\ell\}.
$$

Given prices $p$ and income $m$, the **budget set** is

$$
B(p,m)=\{x\in X:p\cdot x\leq m\}.
$$

Thus $B(p,m)\subseteq X$: the budget condition selects affordable bundles **from** the consumption set. The choice $X=\mathbb R_+^L$ is a modeling assumption, not a result proved from the definition of a consumption set.

## Example

With two divisible goods, let $X=\mathbb R_+^2$. The bundle $(2,3)$ belongs to $X$, while $(-1,3)$ does not. If $p=(2,1)$ and $m=6$, then $(2,3)$ costs $7$: it belongs to $X$ but not to $B(p,m)$.

## Connections

- A preference relation compares bundles drawn from $X$.
- Ordinal Utility Theory represents preferences with a function defined on $X$.
- Convex Preferences uses mixtures of bundles, so its usual definition requires a convex consumption set.
- The Feasible Set contains the bundles available under the model's constraints and is a subset of $X$.
