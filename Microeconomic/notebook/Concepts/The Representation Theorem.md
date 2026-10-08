---
title: "The Representation Theorem"
author: Laplace
tags:
  - economics
  - JCER
date: 2026-09-26
status: Editing
type: Concept
logical_role: derived_result
---
> [!definition]
> **The Representation Theorem (Jehle and Reny, Theorem 1.1).** Let $\succeq$ be a Preference Relation|preference relation on the consumption set $X=\mathbb R_+^n$. If $\succeq$ is [[Rational Preferences|rational]], [[Continuity|continuous]], and [[Monotonicity|strictly monotonic]], then there exists a continuous function
>
> $$
> u:\mathbb R_+^n\to\mathbb R
> $$
>
> that represents $\succeq$:
>
> $$
> \boxed{
> x\succeq y
> \iff
> u(x)\geq u(y)
> }
> \qquad
> \forall x,y\in\mathbb R_+^n.
> $$

## Interpretation

The theorem allows the consumer's ranking of bundles to be replaced by a continuous numerical representation. Statements about preferences can therefore be translated into inequalities between utility values.

This is an **existence theorem**. It guarantees that at least one representing function exists, but it does not provide a particular functional form. It also does not make utility cardinal: the numbers matter only through their ordering. The exact sense in which the representation is non-unique is given by Jehle and Reny's Theorem 1.2 in [[Monotonic Transformation]].

> [!important] What is not required
> Convexity is not required for representability. Convexity restricts the shape of preferences; the representation theorem only asks whether a coherent and sufficiently regular ranking can be encoded by real numbers.

> [!note] Role of strict monotonicity
> Strict monotonicity is stronger than necessary for the general existence result. On $\mathbb R_+^n$, **rationality and continuity are already sufficient** under the standard Debreu representation theorem. Jehle and Reny impose strict monotonicity because it gives a direct constructive proof: every indifference class crosses the diagonal exactly once.

## Derivation

Let

$$
e=(1,\ldots,1)\in\mathbb R_+^n.
$$

For each bundle $x\in\mathbb R_+^n$, define $u(x)$ by the indifference condition

$$
\boxed{u(x)e\sim x}.
$$

Thus, $u(x)$ is the amount of **every** good in a diagonal bundle that makes the consumer indifferent to $x$.

### 1. Existence

Fix $x$ and define

$$
A=\{t\geq0:te\succeq x\},
\qquad
B=\{t\geq0:x\succeq te\}.
$$

Monotonicity ensures that both sets are nonempty: a sufficiently large diagonal bundle lies in $A$, while $0e$ lies in $B$. Continuity makes $A$ and $B$ closed. Completeness ensures that every $t\geq0$ belongs to at least one of them.

Because the nonnegative real line is connected, the two closed sets cannot partition it without meeting. Hence there exists some $t$ such that

$$
t\in A\cap B.
$$

Therefore $te\succeq x$ and $x\succeq te$, so

$$
te\sim x.
$$

### 2. Uniqueness

Suppose both $te\sim x$ and $se\sim x$. If $t>s$, then strict monotonicity gives

$$
te\succ se,
$$

contradicting their indifference through $x$. The same argument rules out $s>t$. Therefore $t=s$, so $u(x)$ is well defined.

### 3. Representation

For any $x,y\in\mathbb R_+^n$,

$$
\begin{aligned}
x\succeq y
&\iff u(x)e\succeq u(y)e\\
&\iff u(x)\geq u(y).
\end{aligned}
$$

The first equivalence follows from $x\sim u(x)e$, $y\sim u(y)e$, and transitivity. The second follows from strict monotonicity along the diagonal. Hence $u$ represents $\succeq$.

### 4. Continuity of the representation

For any $a<b$,

$$
\begin{aligned}
u^{-1}((a,b))
&=\{x\in\mathbb R_+^n:a<u(x)<b\}\\
&=\{x\in\mathbb R_+^n:ae\prec x\prec be\}.
\end{aligned}
$$

Continuity of preferences makes the strict upper and lower contour sets open. Their intersection is therefore open, so $u^{-1}((a,b))$ is open. Hence $u$ is continuous.

## Uniqueness up to Increasing Transformations

A utility representation is unique only up to a [[Monotonic Transformation|strictly increasing transformation]]: $u$ and $v$ represent the same preferences if and only if $v=f\circ u$ for some $f$ strictly increasing on $u(X)$. Jehle and Reny's Theorem 1.2 and its proof are given in the linked concept.

## Example

On $\mathbb R_+^2$, consider preferences represented by

$$
v(x_1,x_2)=x_1+x_2.
$$

They are rational, continuous, and strictly monotonic. The diagonal bundle $(t,t)$ is indifferent to $x=(x_1,x_2)$ when

$$
2t=x_1+x_2.
$$

The construction in the proof therefore gives

$$
u(x)=\frac{x_1+x_2}{2}.
$$

The functions $u$ and $v$ represent the same preferences because

$$
v(x)=2u(x),
$$

and $f(t)=2t$ is strictly increasing on the range of $u$. They assign different numbers to the same bundles but produce exactly the same ordering.

## Limits and common mistakes

- The theorem guarantees **existence**, not a unique functional form.
- Utility levels and utility differences have no intrinsic meaning under an ordinal representation.
- Convex preferences are not required for representation.
- Rationality alone is sufficient on a finite set, but it is not sufficient on every infinite domain.
- Lexicographic preferences on $\mathbb R_+^2$ are rational and strictly monotonic but not continuous, so they do not admit a continuous real-valued utility representation.

## Connections

- The Consumption Set supplies the domain $\mathbb R_+^n$.
- Rationality supplies a coherent ranking; continuity supplies the topological regularity needed for a continuous representation.
- The theorem justifies replacing preference comparisons with utility inequalities in utility maximization.
