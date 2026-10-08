---
title: "Open Set"
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
> Let $(M,d)$ be a metric space. A set $U\subseteq M$ is **open in $M$** if every point $a\in U$ has an [[Open Ball|open ball]] contained entirely in $U$:
>
> $$
> \forall a\in U,\quad\exists r>0
> \quad\text{such that}\quad
> B_r(a)\subseteq U.
> $$

## Interpretation

The radius may depend on the point $a$. The condition must hold for **every** point in $U$: finding one point with a suitable ball is not enough.

"Open" always refers to an ambient metric space. The ball $B_r(a)$ contains points of $M$, so changing $M$ can change whether $U$ is open.

## Example

The interval $(0,1)$ is open in $\mathbb R$. For any $a\in(0,1)$, choose

$$
0<r<\min\{a,1-a\}.
$$

Then $B_r(a)=(a-r,a+r)\subseteq(0,1)$.

## Non-example

The interval $[0,1)$ is not open in $\mathbb R$. It contains $0$, but every $B_r(0)=(-r,r)$ contains $-r/2\notin[0,1)$. Thus no positive radius works at $0$.

## Related definitions

A set is closed in $M$ exactly when its complement in $M$ is open. Equivalently,

$$
U\text{ is open in }M
\quad\Longleftrightarrow\quad
M\setminus U\text{ is closed in }M.
$$

Ambient space matters: $[0,1)$ **is** open relative to $M=[0,1]$, even though it is not open in $\mathbb R$. An open ball is one example of an open set; an open set need not be a single ball.

## Used in

- A closed set uses this open-complement relationship in a specified ambient space.
- The limit definition describes convergence through open balls around the limit.
- Closedness defines a closed set by requiring its complement to be open, or equivalently by placing an open ball around each exterior point.
