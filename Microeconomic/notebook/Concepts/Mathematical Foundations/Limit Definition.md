---
title: "Limit Definition"
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
> Let $(x_k)$ be a sequence in a metric space $(M,d)$, and let $x\in M$. The sequence **converges** to $x$ if
>
> $$
> \forall\varepsilon>0,\quad\exists N\in\mathbb N
> \quad\text{such that}\quad
> k\geq N\Longrightarrow d(x_k,x)<\varepsilon.
> $$

## Interpretation

No matter how small an [[Open Ball]] around $x$ is chosen, every term after some index $N$ lies inside it. The index $N$ may depend on the chosen radius $\varepsilon$.

## Example

In $\mathbb R$ with the usual distance, $x_k=1/k$ converges to $0$. Given any $\varepsilon>0$, choose $N>1/\varepsilon$. Then $k\geq N$ implies $|x_k-0|=1/k<\varepsilon$.

## Non-example

The sequence $x_k=(-1)^k$ does not converge in $\mathbb R$. Its even terms are always $1$ and its odd terms are always $-1$, so the terms cannot eventually lie in every sufficiently small ball around one point.

## Related definitions

Using an open ball $B_\varepsilon(x)=\{y\in M:d(y,x)<\varepsilon\}$, the definition is equivalently

$$
\forall\varepsilon>0,\quad\exists N\in\mathbb N
\quad\text{such that}\quad
k\geq N\Longrightarrow x_k\in B_\varepsilon(x).
$$

## Used in

- Closedness uses limits of sequences to test whether a set contains its boundary limits.
- The closed-set definition gives the equivalent open-complement characterization in a specified ambient space.
