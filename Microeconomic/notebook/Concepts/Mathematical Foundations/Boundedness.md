---
title: "Boundedness"
author: Laplace
tags:
  - economics
  - JCER
date: 2026-09-26
status: Editing
type: Subconcept
logical_role: definition
---
> [!definition]
> A subset $S$ of a metric space $(M,d)$ is **bounded** if one ball of finite radius contains **every** point of $S$. Formally,
>
> $$
> \exists c\in M,\ \exists R>0
> \quad\text{such that}\quad
> d(x,c)<R\quad\text{for every }x\in S.
> $$

## Interpretation

The centre $c$ and radius $R$ may be chosen to fit the set, but **the same ball must work for all points**. Giving each point its own ball would say nothing about whether $S$ is bounded.

Boundedness limits how far points can spread; it does not say how many points the set contains. For example, the interval $(0,1)$ contains infinitely many points but is bounded. Boundedness also does not imply closedness.

## Example

Consider the budget set from The Feasible Set:

$$
B=\{(x_1,x_2)\in\mathbb R_+^2:2x_1+x_2\leq6\}.
$$

Every $x\in B$ satisfies $0\leq x_1\leq3$ and $0\leq x_2\leq6$. Therefore

$$
\|x\|_2\leq\sqrt{3^2+6^2}=\sqrt{45}<7,
$$

so the **single** ball $B_7(0)$ contains all of $B$.

## Non-example

The set $\mathbb R_+^2$ is unbounded: it contains $(k,0)$ for every $k>0$. For any proposed centre $c$ and finite radius $R$, choose $k>R+\|c\|_2$. Then

$$
\|(k,0)-c\|_2
\geq k-\|c\|_2
>R,
$$

so that proposed ball cannot contain the whole set.

## Related definitions

For a nonempty set $S$, boundedness is equivalent to having **finite diameter**:

$$
\operatorname{diam}(S)
=\sup_{x,y\in S}d(x,y)<\infty.
$$

If $S\subseteq B_R(c)$, the triangle inequality gives $d(x,y)<2R$. Conversely, if its diameter is finite, choose any $x_0\in S$; every point of $S$ lies in a sufficiently large ball centred at $x_0$.

Boundedness depends on the metric. In $\mathbb R^L$ with Euclidean distance, it is one of the two conditions in the Heine–Borel criterion; the other is closedness.

## Used in

- Compactness: a subset of finite-dimensional $\mathbb R^L$ is compact exactly when it is closed and bounded.
- Budget sets: with $X=\mathbb R_+^L$, finite nonnegative income $m$, and strictly positive prices $p_\ell$, every bundle in the budget set satisfies $0\leq x_\ell\leq m/p_\ell$.
