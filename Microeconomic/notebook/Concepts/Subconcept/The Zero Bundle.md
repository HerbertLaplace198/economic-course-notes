---
title: "The Zero Bundle"
author: Laplace
tags:
  - economics
  - JCER
date: 2026-09-23
status: Editing
type: Subconcept
logical_role: definition
---
> [!definition]
> For $L$ commodities, the **zero bundle** is the vector
>
> $$
> 0=(0,\ldots,0)\in\mathbb R_+^L.
> $$
>
> The assumption $0\in X$ says that this bundle belongs to the [[The Consumption Set|consumption set]] $X$.

## Interpretation

The zero bundle contains none of the commodities represented in the model. Assuming $0\in X$ means that consuming none of those commodities is an allowed plan. It does **not** mean the consumer prefers that plan or will choose it.

The zero vector exists mathematically whether or not it belongs to a particular consumption set. Therefore, defining the zero bundle and assuming $0\in X$ are different statements.

## Example

If $X=\mathbb R_+^2$, then $(0,0)\in X$. With a budget set $B(p,m)=\{x\in X:p\cdot x\leq m\}$ and $m\geq0$, the zero bundle is also affordable because $p\cdot0=0\leq m$.

## Non-example

Consider

$$
X=\{x\in\mathbb R_+^2:x_1+x_2\geq1\}.
$$

This set contains only nonnegative bundles and is closed and convex, but $(0,0)\notin X$. Thus, nonnegativity, closedness, and convexity do not themselves imply $0\in X$.

## Related definitions

- Non-negative consumption requires $X\subseteq\mathbb R_+^L$; it does not require every nonnegative bundle, including $0$, to be in $X$.
- Closedness and convexity describe different properties of $X$. The example above satisfies both while excluding the zero bundle.

## Used in

- The consumption set includes $0\in X$ among the standard assumptions used in this course.
- A feasible set may impose further constraints. Even when $0\in X$, an arbitrary feasible set need not contain the zero bundle.
