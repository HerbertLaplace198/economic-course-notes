---
title: "Quasi-concave"
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
> Let $C\subseteq\mathbb R^L$ be [[Convexity|convex]], and let $f:C\to\mathbb R$. The function $f$ is **quasi-concave** if, for every $x,y\in C$ and $\lambda\in[0,1]$,
>
> $$
> f\bigl(\lambda x+(1-\lambda)y\bigr)
> \geq\min\{f(x),f(y)\}.
> $$

## Interpretation

The value at a mixture cannot fall below the **smaller** endpoint value. Quasi-concavity does not require the mixture's value to exceed the weighted average of endpoint values; that stronger inequality defines concavity.

For a utility function, the condition says that mixing two bundles cannot produce a bundle worse than the less preferred endpoint. It does not by itself make the best feasible bundle unique.

## Example

On $C=\mathbb R_+^2$, let $f(x_1,x_2)=(x_1+x_2)^2$. Write $s(x)=x_1+x_2\geq0$. Since

$$
s\bigl(\lambda x+(1-\lambda)y\bigr)
=\lambda s(x)+(1-\lambda)s(y)
\geq\min\{s(x),s(y)\},
$$

and squaring preserves order on $[0,\infty)$, $f$ is quasi-concave.

It is **not concave**: for $x=(0,0)$ and $y=(2,0)$, the midpoint $(1,0)$ has $f(1,0)=1$, while $\tfrac12f(0,0)+\tfrac12f(2,0)=2$.

## Non-example

On $\mathbb R_+^2$, the function $g(x_1,x_2)=x_1^2+x_2^2$ is not quasi-concave. At $x=(2,0)$ and $y=(0,2)$, both endpoint values are $4$, but the midpoint gives

$$
g(1,1)=2<\min\{g(2,0),g(0,2)\}=4.
$$

## Related definitions

For each level $\alpha\in\mathbb R$, define the **upper level set**

$$
U_\alpha=\{x\in C:f(x)\geq\alpha\}.
$$

The function $f$ is quasi-concave **if and only if** every $U_\alpha$ is convex. In one direction, if $x,y\in U_\alpha$, the defining inequality gives $f(\lambda x+(1-\lambda)y)\geq\min\{f(x),f(y)\}\geq\alpha$. In the other direction, choose $\alpha=\min\{f(x),f(y)\}$; convexity of $U_\alpha$ gives the defining inequality.

Concavity implies quasi-concavity because

$$
f\bigl(\lambda x+(1-\lambda)y\bigr)
\geq\lambda f(x)+(1-\lambda)f(y)
\geq\min\{f(x),f(y)\}.
$$

The converse fails, as the example above shows. A strictly increasing transformation of $f$ preserves quasi-concavity because it preserves the ordering of function values.

## Used in

- Convex Preferences are represented by a quasi-concave utility function on a convex consumption set.
- Ordinal Utility Theory explains why quasi-concavity, unlike concavity, is preserved by strictly increasing changes of utility scale.
- A consumption set supplies the convex domain on which mixtures of bundles are evaluated in the standard consumer model.
