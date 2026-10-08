---
title: "Continuity"
author: Laplace
tags:
  - economics
  - JCER
date: 2026-09-26
status: Editing
type: Subconcept
logical_role: assumption
---
> [!definition] Axiom 3 — Continuity
> A [[PREFERENCE RELATION|preference relation]] $\succeq$ on a consumption set $X\subseteq\mathbb R^L$ is **continuous** if, for every fixed $z\in X$, both its upper and lower contour sets are [[Closed Set|closed in $X$]]:
>
> $$
> U(z)=\{x\in X:x\succeq z\},
> \qquad
> L(z)=\{x\in X:z\succeq x\}.
> $$

## Interpretation

The sets must be closed **relative to $X$**. If a sequence of bundles weakly preferred to $z$ converges to a bundle in $X$, the limit must still be weakly preferred to $z$. The same applies to bundles to which $z$ is weakly preferred. For every fixed $z\in X$,

$$
\begin{aligned}
x^k\succeq z,\quad x^k\to x\in X
&\Longrightarrow x\succeq z,\\[0.8em]
z\succeq x^k,\quad x^k\to x\in X
&\Longrightarrow z\succeq x.
\end{aligned}
$$

The reference bundle $z$ is held fixed in these tests. Continuity rules out a preference comparison disappearing at the limit of a convergent sequence. It is an additional regularity assumption; completeness and transitivity alone do not imply it.

## Example

On $X=\mathbb R_+^2$, let $u(x)=x_1+x_2$ and define $x\succeq y$ exactly when $u(x)\geq u(y)$. For each $z$,

$$
U(z)=\{x\in X:u(x)\geq u(z)\},
\qquad
L(z)=\{x\in X:u(x)\leq u(z)\}.
$$

Both sets are closed in $X$: the continuous function $u$ maps convergent sequences to convergent utility values, and a weak inequality remains true at the limit. Hence these preferences are continuous.

## Non-example

Lexicographic preferences on $X=\mathbb R_+^2$ rank $x$ above $y$ if $x_1>y_1$, or if $x_1=y_1$ and $x_2\geq y_2$. They are complete and transitive, but not continuous. Fix $z=(1,1)$ and let

$$
x^k=(1+1/k,0).
$$

Every $x^k\succeq z$ because its first coordinate exceeds $1$. Yet $x^k\to(1,0)$ and $(1,0)\not\succeq(1,1)$. Thus $U(z)$ is not closed.

## Related definitions

When $\succeq$ is complete, its strict contour sets are the complements of the opposite weak contour sets:

$$
\{x\in X:x\succ z\}=X\setminus L(z),
\qquad
\{x\in X:z\succ x\}=X\setminus U(z).
$$

Thus continuity is also equivalent to both strict contour sets being open in $X$ for every $z$. A continuous utility representation implies continuous preferences because the weak contour sets are inverse images of closed intervals under $u$.

Jehle and Reny state continuity in this contour-set form (Axiom 3).

## Used in

- A preference relation: continuity is separate from rationality, which requires completeness and transitivity.
- Ordinal utility theory: continuity is important when asking for a **continuous** function representing preferences.
