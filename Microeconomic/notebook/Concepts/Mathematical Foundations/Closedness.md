---
title: "Closedness"
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
> A set $C\subseteq\mathbb R^L$ is **closed** if every point outside $C$ has an open ball that does not meet $C$:
>
> $$
> \forall y\in\mathbb R^L\setminus C,\quad
> \exists r>0\quad\text{such that}\quad
> B_r(y)\cap C=\varnothing.
> $$

## Interpretation

Every exterior point must have some room around it that stays outside $C$. Equivalently, the complement $\mathbb R^L\setminus C$ is open. The ambient space matters: here closedness means closed **in $\mathbb R^L$**.

A closed ball is an example of a closed set, but the definition of closedness does not require a set to be a ball.

## Example

The nonnegative orthant $\mathbb R_+^L$ is closed. If $y\notin\mathbb R_+^L$, some coordinate $y_j<0$. Choose $0<r<-y_j$. Every $z\in B_r(y)$ satisfies $z_j<y_j+r<0$, so $B_r(y)\cap\mathbb R_+^L=\varnothing$.

## Non-example

The strictly positive orthant $\mathbb R_{++}^L$ is not closed. The point $y=(0,1,\ldots,1)$ lies outside it. Yet every $B_r(y)$ contains $(r/2,1,\ldots,1)\in\mathbb R_{++}^L$, so no open ball around $y$ avoids the set.

## Related definitions

In $\mathbb R^L$, the open-ball condition is equivalent to the sequential criterion:

$$
x^k\in C,\quad x^k\to x
\quad\Longrightarrow\quad x\in C.
$$

See [[Closed Set]] for the complement formulation in a specified ambient space. **Closed** does not mean **bounded**; $\mathbb R_+^L$ is closed and unbounded.

## Used in

- The Consumption Set assumes closedness so that limits of admissible bundles remain in $X$.
- Convexity is a separate property: a set may be closed without being convex.
