---
title: "Preference Relation"
author: Laplace
tags:
  - economics
  - JCER
date: 2026-09-23
status: Editing
type: Concept
logical_role: definition
---
> [!definition]
> A **preference relation** $\succeq$ compares bundles in the consumption set $X$. 
> For $x,y\in X$, writing $x\succeq y$ means that the consumer considers $x$ **at least as good as** $y$.

## Interpretation

This is a *weak* preference: $x\succeq y$ allows the consumer to regard $x$ and $y$ as equally good. The statement describes a comparison, not how large the difference in satisfaction is.

Defining $\succeq$ does not by itself impose completeness or transitivity. **Completeness** requires that, for every $x,y\in X$, either $x\succeq y$ or $y\succeq x$. **Transitivity** requires that, for every $x,y,z\in X$,

$$
x\succeq y,\quad y\succeq z
\quad\Longrightarrow\quad
x\succeq z.
$$

In much of microeconomic theory, preferences are assumed to be **rational**: $\succeq$ is both complete and transitive. This is an additional assumption about the relation, not a consequence of merely writing $x\succeq y$. Rationality in this sense does not require continuity, convexity, or monotonicity.

**Terminology.** Jehle and Reny (Definition 1.1) call a relation a *preference relation* only when it satisfies both completeness and transitivity. In these notes, *preference relation* names the comparison relation itself; completeness and transitivity are separate properties. This lets us discuss relations that fail either property without changing their name.

## Assumptions on the Preference Relation

The lecture's five axioms progressively restrict admissible preference shapes; they do not change a fixed consumer's tastes. Figures 1.1–1.6 are schematic redrawings of the lecture figures. Axioms 4 and 5 are stated on $X=\mathbb R_+^n$.

[[Geoffrey A. Jehle, Philip J. Reny - Advanced Microeconomic Theory, 3rd Edition  -Prentice Hall (2011).pdf#page=23&annotation=4328R|Axiom 1]] — [[Completeness]].** Every pair of bundles can be compared:

$$
\forall x^1,x^2\in X,\qquad x^1\succeq x^2\quad\text{or}\quad x^2\succeq x^1.
$$

**Axiom 2 — [[Transitivity]].** Pairwise comparisons must be consistent:

$$
\forall x^1,x^2,x^3\in X,\qquad
x^1\succeq x^2\ \text{and}\ x^2\succeq x^3
\quad\Longrightarrow\quad x^1\succeq x^3.
$$

Together, Axioms 1 and 2 define **Rational Preferences**. They establish a coherent ranking, but thick indifference regions, missing boundary points, and upward bends may remain.

![[Preference Fig 1.1 - Rationality.png|700]]

[[Geoffrey A. Jehle, Philip J. Reny - Advanced Microeconomic Theory, 3rd Edition  -Prentice Hall (2011).pdf#page=26&annotation=4331R|Axiom 3]] — [[Continuity]].** For every $x\in X$, both the upper contour set $\{y\in X:y\succeq x\}$ and the lower contour set $\{y\in X:x\succeq y\}$ are closed in $X$. This closes missing boundary points but can leave a thick indifference region.

![[Preference Fig 1.2 - Continuity.png|700]]

**Alternative Axiom 4′ — [[Local Non-satiation]].** Every neighbourhood contains a strictly preferred bundle. This rules out a thick indifference region, but upward bends may remain.

![[Preference Fig 1.3 - Local Non-satiation.png|700]]

**Axiom 4 — Strict [[Monotonicity]].** For all $x^0,x^1\in\mathbb R_+^n$,

$$
x^0\geq x^1\quad\Longrightarrow\quad x^0\succeq x^1,
\qquad
x^0\gg x^1\quad\Longrightarrow\quad x^0\succ x^1.
$$

Here $\geq$ means at least as much of every good, while $\gg$ means strictly more of **every** good. Figure 1.4 shows an indifference curve this axiom rules out. Requiring strict preference when only one good increases is a stronger condition.

![[Preference Fig 1.4 - Monotonicity.png|700]]

Axioms 1–4 still permit non-convex preferences: the mixture of two indifferent bundles can be worse (Fig. 1.5).

![[Preference Fig 1.5 - Non-convexity.png|700]]

**Axiom 5 — Strict [[Convex Preferences|Convexity]]** For $x^0,x^1\in X$ and $t\in(0,1)$,

$$
x^1\succeq x^0,\quad x^1\ne x^0
\quad\Longrightarrow\quad
tx^1+(1-t)x^0\succ x^0.
$$

Thus a nontrivial mixture is strictly better than the less preferred endpoint. This rules out Fig. 1.5 and yields the pattern in Fig. 1.6.

![[Preference Fig 1.6 - Strict Convexity.png|700]]

> [!note] Alternative strength
> Axiom 5′ (weak convexity) replaces $\succ$ above by $\succeq$ and also permits $t=0,1$. Axiom 4′ is an alternative weaker restriction to compare with Axiom 4, not an additional step required before it.

## Derivation

Strict preference and indifference are defined from the weak preference relation:

$$
\begin{aligned}
x\succ y
&\iff x\succeq y\ \text{and}\ \neg(y\succeq x),\\[0.8em]
x\sim y
&\iff x\succeq y\ \text{and}\ y\succeq x.
\end{aligned}
$$

Thus, $x\succ y$ rules out $y\succeq x$, whereas $x\sim y$ requires comparison in both directions.

## Properties under rationality

**Proposition (MWG, Proposition 1.B.1).** If $\succeq$ is rational (complete and transitive), then:

1. The strict preference relation $\succ$ is irreflexive and transitive.
2. The indifference relation $\sim$ is reflexive, symmetric, and transitive.
3. If $x\succ y$ and $y\succeq z$, then $x\succ z$.

### Proof

**1. Strict preference.** By definition, $x\succ x$ would require both $x\succeq x$ and $\neg(x\succeq x)$, which is impossible. Hence $\succ$ is irreflexive.

Suppose $x\succ y$ and $y\succ z$. Since $x\succeq y\succeq z$, transitivity of $\succeq$ gives $x\succeq z$. If $z\succeq x$, then $z\succeq x\succeq y$ implies $z\succeq y$, contradicting $y\succ z$. Thus $\neg(z\succeq x)$, so $x\succ z$.

**2. Indifference.** Completeness applied to the pair $(x,x)$ implies $x\succeq x$, hence $x\sim x$. Symmetry follows directly from the definition: $x\sim y$ requires both $x\succeq y$ and $y\succeq x$, so also $y\sim x$.

If $x\sim y$ and $y\sim z$, transitivity of $\succeq$ gives $x\succeq y\succeq z$, hence $x\succeq z$, and $z\succeq y\succeq x$, hence $z\succeq x$. Therefore $x\sim z$. Thus $\sim$ is an equivalence relation.

**3. Strict followed by weak preference.** If $x\succ y$ and $y\succeq z$, then $x\succeq y\succeq z$ gives $x\succeq z$. If $z\succeq x$, then $y\succeq z\succeq x$ would imply $y\succeq x$, contradicting $x\succ y$. Therefore $\neg(z\succeq x)$ and $x\succ z$.

**Completeness caveat.** On a nonempty $X$, $\succ$ is not complete because $x\succ x$ never holds. Indifference $\sim$ is generally incomplete, but it **is** complete in the special case where every pair of bundles is indifferent. Neither derived relation must inherit completeness from $\succeq$.


## Connections

- The consumption set supplies the bundles that the relation compares.
- Ordinal Utility Theory represents a preference relation by numbers when such a representation exists: $x\succeq y\iff u(x)\geq u(y)$.
- Convex Preferences places an additional condition on the preference relation; it is not part of the definition of $\succeq$.
