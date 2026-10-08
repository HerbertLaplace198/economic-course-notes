---
title: "Closed Ball"
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
> Let $(M,d)$ be a metric space, let $a\in M$, and let $r>0$. The **closed ball** with centre $a$ and radius $r$ is
>
> $$
> \overline B_r(a)=\{y\in M:d(a,y)\leq r\}.
> $$

## Interpretation

A closed ball contains all points at distance **at most** $r$ from its centre, including any points at distance exactly $r$. Every closed ball is a [[Closed Set|closed set]] in its metric space.

## Example

In $\mathbb R$ with the usual distance,

$$
\overline B_r(a)=[a-r,a+r].
$$

In particular, $\overline B_1(0)=[-1,1]$ includes both endpoints.

## Non-example

The interval $(-1,1)$ is not $\overline B_1(0)$ in $\mathbb R$, because it omits the points $-1$ and $1$, whose distance from the centre is exactly $1$.

## Related definitions

The open ball $B_r(a)$ uses the strict condition $d(a,y)<r$, so $B_r(a)\subseteq\overline B_r(a)$. In Euclidean space, the closure of $B_r(a)$ is $\overline B_r(a)$; in a general metric space this equality need not hold.

## Used in

- The closed-set definition gives the general definition of a closed subset of an ambient space.
- Closedness concerns all closed sets; a closed ball is one example, but a closed set need not have the shape of a ball.
