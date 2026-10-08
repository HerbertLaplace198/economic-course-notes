---
title: "Convex Preferences"
author: Laplace
tags:
  - economics
  - JCER
date: 2026-09-24
status: Editing
type: Concept
logical_role: assumption
---
> [!definition] Axiom 5′ and Axiom 5 — Convex Preferences
> On a convex consumption set $X$, **Axiom 5′ (weak convexity)** requires, for $x^0,x^1\in X$ and $t\in[0,1]$,
>
> $$
> x^1\succeq x^0
> \quad\Longrightarrow\quad
> tx^1+(1-t)x^0\succeq x^0.
> $$
>
> **Axiom 5 (strict convexity)** strengthens the conclusion when $x^1\ne x^0$ and $t\in(0,1)$:
>
> $$
> x^1\succeq x^0,\quad x^1\ne x^0
> \quad\Longrightarrow\quad
> tx^1+(1-t)x^0\succ x^0.
> $$

## Interpretation

Both axioms say that mixing two bundles cannot be worse than the less preferred endpoint. Axiom 5′ allows indifference; Axiom 5 requires every nontrivial mixture of distinct bundles to be **strictly** preferred to that endpoint. If $x^0\sim x^1$, Axiom 5′ makes the mixture weakly preferred to both; Axiom 5 makes it strictly preferred to both.

[[Convexity]] of $X$ ensures that the mixture is in the consumption set. Convexity of preferences is a separate condition on how the consumer ranks that mixture.

## Derivation

For each $z\in X$, define its **upper contour set** as

$$
U(z)=\{x\in X:x\succeq z\}.
$$

When preferences are complete and transitive, Axiom 5′ is equivalent to every $U(z)$ being convex. To see one direction, take $x,y\in U(z)$. By completeness, suppose without loss of generality that $x\succeq y$. Convexity of preferences gives $\lambda x+(1-\lambda)y\succeq y$; transitivity with $y\succeq z$ then gives $\lambda x+(1-\lambda)y\succeq z$. Thus the mixture remains in $U(z)$.

Conversely, if each $U(z)$ is convex and $x_1\succeq x_0$, then both $x_1$ and $x_0$ lie in $U(x_0)$. Hence their mixture also lies in $U(x_0)$, giving Axiom 5′.

If an ordinal utility function $u$ represents the preferences, this is equivalent to

$$
u\bigl(\lambda x+(1-\lambda)y\bigr)
\geq\min\{u(x),u(y)\}
\qquad(x,y\in X,\ \lambda\in[0,1]).
$$

This is [[Quasi-concave|quasi-concavity]] of $u$. The utility function itself need not be convex or concave.

## Example

On $X=\mathbb R_+^2$, the utility function $u(x_1,x_2)=x_1+x_2$ represents convex preferences: the utility of a mixture is the same weighted average of endpoint utilities, so it cannot fall below the smaller endpoint value. For $x=(2,0)$ and $y=(0,2)$, the midpoint $(1,1)$ gives the same utility $2$ as both endpoints. This illustrates Axiom 5′ and shows why strict convexity is a separate condition.

For a strict example, $u(x_1,x_2)=\sqrt{x_1}+\sqrt{x_2}$ is strictly concave on $\mathbb R_+^2$ and therefore represents preferences satisfying Axiom 5.

By contrast, $u(x_1,x_2)=x_1^2+x_2^2$ does not represent convex preferences on $\mathbb R_+^2$: $(2,0)$ and $(0,2)$ each give utility $4$, but their midpoint $(1,1)$ gives only $2$.

## Connections

- A preference relation defines how bundles are compared; convex preferences add a restriction on those comparisons.
- The consumption set must contain the mixtures being compared; convexity defines this property of a set.
- Quasi-concavity is the corresponding condition on any utility function representing convex preferences.
- Ordinal utility theory explains why a strictly increasing transformation of the representing utility function preserves the same convex preferences.
