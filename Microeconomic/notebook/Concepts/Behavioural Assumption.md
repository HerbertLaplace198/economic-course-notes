---
title: "Behavioural Assumption"
author: Laplace
tags:
  - economics
  - JCER
date: 2026-09-24
status: Editing
type: Concept
logical_role: assumption
---
> [!definition]
> In the standard consumer-choice model, the **behavioural assumption** is that the consumer selects a most-preferred bundle from the feasible set $B$. A chosen bundle $x^*$ must satisfy
>
> $$
> x^*\in B
> \quad\text{and}\quad
> x^*\succeq x\quad\text{for every }x\in B.
> $$

## Interpretation

The feasible set determines what the consumer **can** choose; the Preference Relation determines how those options are ranked. This assumption says the consumer chooses an available option that is at least as good as every other available option.

The assumption does not require a unique choice: several feasible bundles may tie for best. It also does not guarantee that a best bundle exists. Existence depends on the feasible set and the properties of preferences; it must be checked or assumed separately.

## Derivation

Given $B\subseteq X$ and a preference relation $\succeq$ on $X$, the set of choices satisfying the behavioural assumption is

$$
C(B,\succeq)
=\{x^*\in B:x^*\succeq x\text{ for every }x\in B\}.
$$

If an ordinal utility function $u$ represents the preference relation, then $x^*\succeq x$ is equivalent to $u(x^*)\geq u(x)$. Therefore the same choice set can be written as

$$
C(B,\succeq)=\operatorname*{arg\,max}_{x\in B}u(x).
$$

This is the **utility maximization** formulation of the behavioural assumption. It describes the same ranking-based choice whenever the utility representation exists; the numerical utility values themselves need not measure satisfaction.

## Example

Suppose $B=\{a,b,c\}$ and $a\sim b\succ c$. Both $a$ and $b$ satisfy the assumption, so $C(B,\succeq)=\{a,b\}$. A representation such as $u(a)=u(b)=2$ and $u(c)=1$ gives the same maximizing set.

If $a$ is removed from $B$, the consumer can no longer choose it even though it remains in the consumption set and may still be preferred to other bundles.

## Connections

- The consumption set defines the domain of possible bundles.
- The feasible set restricts choice to bundles the consumer can obtain.
- The preference relation ranks those bundles; the behavioural assumption selects the highest-ranked feasible ones.
- Ordinal utility theory permits the equivalent utility-maximization expression when a representing utility function exists.
