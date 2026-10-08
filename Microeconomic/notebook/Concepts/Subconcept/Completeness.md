---
title: "Completeness"
author: Laplace
tags:
  - economics
  - JCER
date: 2026-09-26
status: Editing
type: Subconcept
logical_role: assumption
---
> [!definition] Axiom 1 — Completeness
> Let $\succeq$ be a binary relation on the consumption set $X$. It is **complete** if, for every $x,y\in X$,
>
> $$
> x\succeq y\quad\text{or}\quad y\succeq x.
> $$

## Interpretation

Every pair of bundles must be comparable. The **or** is inclusive: both comparisons may hold, in which case $x\sim y$. Completeness therefore allows indifference; it does not demand a strict ranking or a unique best bundle.

The definition includes the case $x=y$. Setting $y=x$ gives $x\succeq x$ for every $x\in X$. Thus completeness **implies reflexivity**. Reflexivity alone does not imply completeness, because it says nothing about two distinct bundles.

Completeness differs from **transitivity**. Completeness asks whether a comparison is available for each pair; transitivity asks whether comparisons are consistent across triples. Neither condition implies the other.

## Example

On $X=\mathbb R_+^2$, let $u(x)=x_1+x_2$ and define

$$
x\succeq y\quad\Longleftrightarrow\quad u(x)\geq u(y).
$$

For every $x,y\in X$, the real numbers $u(x)$ and $u(y)$ can be compared, so either $x\succeq y$ or $y\succeq x$. If $u(x)=u(y)$, both comparisons hold and the bundles are indifferent. This relation is also transitive, because $\geq$ on the real numbers is transitive.

## Non-example

On $X=\mathbb R_+^2$, suppose $x\succeq y$ only when $x$ has at least as much of **each** good as $y$:

$$
x\succeq y
\quad\Longleftrightarrow\quad
x_1\geq y_1\ \text{and}\ x_2\geq y_2.
$$

Take $x=(1,0)$ and $y=(0,1)$. The first bundle has more of good 1, while the second has more of good 2. Neither $x\succeq y$ nor $y\succeq x$ holds, so the relation is **not complete**. It is nevertheless transitive: if $x_j\geq y_j\geq z_j$ for each good $j$, then $x_j\geq z_j$.

## Related definitions

A preference relation is **rational** in the usual consumer-theory sense when it is both complete and transitive. Completeness alone does not rule out a cycle such as $a\succeq b$, $b\succeq c$, and $c\succeq a$ without $a\succeq c$.

Completeness is necessary for representation by a real-valued utility function. If $x\succeq y$ exactly when $u(x)\geq u(y)$, then for any $x,y$ either $u(x)\geq u(y)$ or $u(y)\geq u(x)$, so the preference relation is complete. Completeness by itself is not sufficient for a utility representation; the relation must also be transitive.

## Used in

- [[PREFERENCE RELATION]]: completeness, together with transitivity, is the rationality assumption used to derive properties of strict preference and indifference.
