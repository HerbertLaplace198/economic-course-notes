---
title: "Convexity"
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
> A set $C\subseteq\mathbb R^L$ is **convex** if, for every $x,y\in C$ and every $\lambda\in[0,1]$,
>
> $$
> \lambda x+(1-\lambda)y\in C.
> $$

## Interpretation

The entire line segment joining any two points in $C$ must remain in $C$. The cases $\lambda=0$ and $\lambda=1$ give the endpoints; values strictly between $0$ and $1$ test the points between them.

This definition concerns the **shape of a set**. It says nothing by itself about which bundle a consumer prefers.

## Example

The nonnegative orthant $\mathbb R_+^L$ is convex. If $x,y\in\mathbb R_+^L$ and $\lambda\in[0,1]$, then, for every coordinate $\ell$,

$$
\lambda x_\ell+(1-\lambda)y_\ell\geq 0.
$$

Hence $\lambda x+(1-\lambda)y\in\mathbb R_+^L$.

## Non-example

The set $\mathbb Z_+^2$ of nonnegative integer bundles is not convex. Both $x=(1,0)$ and $y=(0,1)$ belong to it, but their midpoint does not:

$$
\frac12x+\frac12y
=\left(\frac12,\frac12\right)
\notin\mathbb Z_+^2.
$$

## Related definitions

Equivalently, $C$ is convex if the line segment

$$
[x,y]=\{\lambda x+(1-\lambda)y:\lambda\in[0,1]\}
$$

is contained in $C$ for every $x,y\in C$. Convexity of a **set** is distinct from convexity of a function or of a preference relation.

## Used in

- The Consumption Set assumes that $X$ is convex in the standard model, so mixtures of its bundles remain in $X$.
- Convex Preferences requires certain sets of equally good or better bundles to be convex; a convex $X$ alone does not establish this preference property.
- Quasi-concave describes the corresponding condition on a utility function representing convex preferences.
