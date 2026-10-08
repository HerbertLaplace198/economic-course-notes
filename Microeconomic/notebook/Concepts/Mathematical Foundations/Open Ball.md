---
title: "Open Ball"
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
> Let $(M,d)$ be a metric space, let $a\in M$, and let $r>0$. The **open ball** with centre $a$ and radius $r$ is
>
> $$
> B_r(a)=\{y\in M:d(a,y)<r\}.
> $$

## Interpretation

An open ball contains exactly the points whose distance from $a$ is **strictly less than** $r$. Points at distance exactly $r$ are excluded. Every open ball is an open set in its metric space.

## Example

In $\mathbb R$ with $d(a,y)=|a-y|$,

$$
B_r(a)=(a-r,a+r).
$$

In particular, $B_1(0)=(-1,1)$: both $-1$ and $1$ are excluded.

## Non-example

The interval $[-1,1]$ is not $B_1(0)$ in $\mathbb R$, because it contains the points $-1$ and $1$, each at distance exactly $1$ from the centre.

## Related definitions

The closed ball with the same centre and radius uses $d(a,y)\leq r$ instead. The distinction is the **strict** versus **weak** distance inequality.

## Used in

- An open set requires an open ball around every point of the set that remains inside it.
- Closedness can be tested by finding an open ball around each exterior point that avoids the set.
- Limit Definition describes convergence using every sufficiently small open ball around a limit.
