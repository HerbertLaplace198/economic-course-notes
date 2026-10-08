---
title: "Monotonic Transformation"
aliases:
  - 单调变换
  - Strictly Increasing Transformation
author: Laplace
tags:
  - economics
  - JCER
date: 2026-10-07
status: Editing
type: Concept
logical_role: definition
---
> [!definition]
> Let $u:X\to\mathbb R$ be a utility function. A **monotonic transformation** of $u$, in the ordinal utility sense, is a function
>
> $$
> v(x)=f(u(x)),
> $$
>
> where $f:u(X)\to\mathbb R$ is **strictly increasing**:
>
> $$
> t_1>t_2\quad\Longrightarrow\quad f(t_1)>f(t_2)
> \qquad\forall t_1,t_2\in u(X).
> $$

## Interpretation

The transformation changes the numerical labels assigned to consumption bundles while preserving their order. It acts on utility values; the consumer's preferences and the consumption bundles themselves are unchanged.

Here, **monotonic transformation** means a **strictly increasing transformation**. A strictly decreasing transformation reverses the ranking, while a merely nondecreasing transformation can turn a strict preference into indifference.

## Invariance of Utility Representation

> [!theorem]
> **Invariance to increasing transformations (Jehle and Reny, Theorem 1.2).** Let $u:X\to\mathbb R$ represent $\succeq$. A function $v:X\to\mathbb R$ also represents $\succeq$ **if and only if** there exists a function
>
> $$
> f:u(X)\to\mathbb R
> $$
>
> that is strictly increasing on the range of $u$ and satisfies
>
> $$
> \boxed{v(x)=f(u(x))\quad\forall x\in X.}
> $$

Equivalently,

$$
\boxed{
v\text{ represents }\succeq
\iff
v=f\circ u
\text{ for some strictly increasing }f\text{ on }u(X).
}
$$

This is what **uniqueness up to increasing transformations** means. A utility representation is not unique as a numerical function; it is unique only up to a relabelling that preserves the order of all utility levels.

> [!important] Why the range matters
> The transformation needs to be strictly increasing only on
> $$
> u(X)=\{u(x):x\in X\},
> $$
> because utility values outside this set are never assigned to any bundle. For example, $f(t)=t^2$ is strictly increasing on $[0,\infty)$ even though it is not strictly increasing on all of $\mathbb R$.

### Proof: increasing transformations preserve representation

Suppose

$$
v=f\circ u
$$

and $f$ is strictly increasing on $u(X)$. Since $u$ represents $\succeq$,

$$
\begin{aligned}
x\succeq y
&\iff u(x)\geq u(y)\\
&\iff f(u(x))\geq f(u(y))\\
&\iff v(x)\geq v(y).
\end{aligned}
$$

Therefore $v$ also represents $\succeq$.

### Proof: every equivalent representation is an increasing transformation

Now suppose both $u$ and $v$ represent the same preference relation. For each $t\in u(X)$, choose any $x\in X$ satisfying $u(x)=t$ and define

$$
f(t)=v(x).
$$

This definition is well defined. If $u(x)=u(y)$, then

$$
x\sim y,
$$

so any other representation of the same preferences must satisfy

$$
v(x)=v(y).
$$

To show that $f$ is strictly increasing, take $t_1,t_2\in u(X)$ with $t_1>t_2$, and choose $x_1,x_2\in X$ such that $u(x_1)=t_1$ and $u(x_2)=t_2$. Then

$$
u(x_1)>u(x_2)
\Longrightarrow
x_1\succ x_2
\Longrightarrow
v(x_1)>v(x_2).
$$

Hence

$$
f(t_1)>f(t_2).
$$

Thus $f$ is strictly increasing on $u(X)$ and, by construction,

$$
v=f\circ u.
$$

> [!summary] Ordinal meaning
> No significance attaches to the particular numbers assigned by a utility function. Only their ordering matters. A strictly increasing transformation may change utility levels, differences, ratios, and marginal utilities, but it cannot change preference rankings or the set of utility-maximizing bundles.

## Example

On $X=\mathbb R_+^2$, let

$$
u(x_1,x_2)=x_1+x_2.
$$

Since $u(X)=[0,\infty)$, the function $f(t)=t^2$ is strictly increasing on the relevant range. Therefore

$$
v(x_1,x_2)=(x_1+x_2)^2
$$

represents exactly the same preferences as $u$. The numbers and utility differences change, but the ranking of bundles does not.

## Limits and common mistakes

- Strict increase is required on the actual utility range $u(X)$, not necessarily on all of $\mathbb R$.
- A nondecreasing transformation can collapse distinct utility levels. For example, a constant transformation makes all bundles indifferent and cannot preserve a ranking with strict preferences.
- No differentiability assumption is needed for the representation result.
