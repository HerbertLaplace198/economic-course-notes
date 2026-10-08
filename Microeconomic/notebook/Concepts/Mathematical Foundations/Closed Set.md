---
title: "Closed Set"
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
> Let $(M,d)$ be a metric space. A set $F\subseteq M$ is **closed in $M$** if its complement $M\setminus F$ is [[Open Set|open in $M$]]. Equivalently, every point outside $F$ has an open ball that avoids $F$:
>
> $$
> \forall y\in M\setminus F,\quad
> \exists r>0\quad\text{such that}\quad
> B_r(y)\cap F=\varnothing.
> $$

## Interpretation

The condition concerns **every point outside** $F$. For each such point, the radius may be different. Finding a ball that avoids $F$ around only some exterior points is insufficient.

Closedness is relative to the ambient metric space $M$: both the complement $M\setminus F$ and the balls $B_r(y)$ are taken in $M$.

## Example

The interval $F=[0,1]$ is closed in $\mathbb R$. If $y<0$, choose $r=-y/2$; if $y>1$, choose $r=(y-1)/2$. In either case, $B_r(y)\cap[0,1]=\varnothing$.

## Non-example

The interval $U=(0,1)$ is not closed in $\mathbb R$. The point $0$ lies outside $U$, yet every $B_r(0)$ intersects $U$. An exterior point such as $2$ does have a ball avoiding $U$, but that does not satisfy the condition at $0$.

## Related definitions

$$
F\text{ is closed in }M
\quad\Longleftrightarrow\quad
M\setminus F\text{ is open in }M.
$$

A closed ball is a closed set, but a closed set need not be a ball. Closedness gives the corresponding sequential criterion in $\mathbb R^L$.

## Used in

- Compactness: in finite-dimensional Euclidean space, a set is compact exactly when it is closed and bounded.
- The consumption set: closedness ensures that limits of admissible bundles remain admissible.
