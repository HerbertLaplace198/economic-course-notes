---
title: "Non-negative Consumption"
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
> For $L$ goods, **non-negative consumption** means that every bundle in the [[The Consumption Set|consumption set]] $X$ has a non-negative quantity of each good:
>
> $$
> X\subseteq\mathbb R_+^L,
> \qquad
> \mathbb R_+^L
> =\{x\in\mathbb R^L:x_\ell\geq0
> \text{ for every }\ell=1,\ldots,L\}.
> $$

## Interpretation

The condition restricts **which bundles are allowed**; it does not rank them. A quantity of zero is permitted for an individual good. The inclusion $X\subseteq\mathbb R_+^L$ does **not** say that every non-negative bundle belongs to $X$.

Non-negativity is a modeling assumption, not a property of every possible consumption set. Models with net trades or short positions may allow negative components.

## Example

Let $X=\{x\in\mathbb R_+^2:x_1+x_2\geq1\}$. Every bundle in $X$ has non-negative components, so $X\subseteq\mathbb R_+^2$. Yet $(0,0)\notin X$: non-negativity does not imply that the zero bundle is available.

## Non-example

If $X=\{(-1,2),(0,0)\}$, then $X\not\subseteq\mathbb R_+^2$ because the first bundle contains a negative quantity of good 1.

## Related definitions

- The stronger condition $x_\ell>0$ for every $\ell$ places a bundle in $\mathbb R_{++}^L$ and excludes zero consumption of any good.
- Taking $X=\mathbb R_+^L$ is one possible choice of consumption set. It is stronger than merely requiring $X\subseteq\mathbb R_+^L$.
- Non-negativity alone does not imply closedness or convexity.

## Used in

- The Consumption Set includes non-negativity among the standard assumptions used in this course.
- A feasible set selects bundles from $X$, so its bundles are also non-negative whenever $X\subseteq\mathbb R_+^L$.
