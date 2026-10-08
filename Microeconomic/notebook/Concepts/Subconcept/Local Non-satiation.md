---
title: Local Non-satiation
author: Laplace
tags:
  - economics
  - JCER
date: 2026-09-26
status: Editing
type: Subconcept
logical_role: assumption
---
> [!definition]
> A [[PREFERENCE RELATION|preference relation]] $\succeq$ on $X\subseteq\mathbb R^L$ is **locally non-satiated** if, for every $x\in X$ and every $\varepsilon>0$, there is a bundle $y\in X$ such that
>
> $$
> \|y-x\|<\varepsilon
> \qquad\text{and}\qquad
> y\succ x.
> $$

## Interpretation

No bundle is a **local** point of satiation: however small a neighbourhood of $x$ we choose, it contains a strictly preferred bundle that is still in $X$. The quantifier “for every $\varepsilon>0$” matters. Finding a better bundle somewhere far away is not enough.

The neighbourhood is taken **relative to $X$**. At a boundary point, the better bundle must lie in $B_\varepsilon(x)\cap X$; the definition does not require a bundle outside $X$. If $x$ is isolated in $X$, local non-satiation fails at $x$ because sufficiently small neighbourhoods contain no other bundle in $X$.

Local non-satiation is a property of preferences on $X$. It does not say that every nearby bundle is better, or that every good is desirable.

## Example

On $X=\mathbb R_+^2$, let $u(x_1,x_2)=x_1+x_2$. For any $x\in X$ and $\varepsilon>0$, choose

$$
y=x+(\varepsilon/2,0).
$$

Then $y\in X$, $\|y-x\|=\varepsilon/2<\varepsilon$, and $u(y)>u(x)$. Thus the represented preferences are locally non-satiated, including at boundary points such as $x=(0,0)$.

## Non-example

On $X=\mathbb R_+$, let $u(x)=-(x-1)^2$. At the bliss point $x=1$, $u(1)=0$ and $u(y)<0$ for every $y\ne1$. There is no strictly preferred bundle in **any** neighbourhood of $1$, so these preferences are not locally non-satiated.

## Related definitions

On $X=\mathbb R_+^L$, **strict monotonicity** (more of at least one good, with none reduced, is strictly better) implies local non-satiation: increase one coordinate by an arbitrarily small amount. The converse fails. For example, $u(x_1,x_2)=x_1-x_2$ is locally non-satiated on $\mathbb R_+^2$ because $x_1$ can always be increased slightly, although increasing $x_2$ makes the consumer worse off. Weak monotonicity alone does not imply local non-satiation; a constant utility function is a counterexample.

## Used in

[[Walras' Law]] uses local non-satiation to show that an **existing optimum** for the ordinary budget set exhausts the budget. Let

$$
B(p,m)=\{x\in X:p\cdot x\leq m\},
$$

and suppose $x^*\in B(p,m)$ is most preferred among its bundles. If $p\cdot x^*<m$, write $\delta=m-p\cdot x^*>0$. Since the cost function $x\mapsto p\cdot x$ is continuous, some $\varepsilon>0$ satisfies

$$
\|y-x^*\|<\varepsilon
\quad\Longrightarrow\quad
p\cdot y<p\cdot x^*+\delta=m.
$$

Local non-satiation supplies $y\in X$ inside that neighbourhood with $y\succ x^*$. The inequality makes $y\in B(p,m)$, contradicting the optimality of $x^*$. Hence

$$
\boxed{p\cdot x^*=m}.
$$

This argument requires the nearby better bundle to remain affordable. It applies to the ordinary budget set; an additional constraint could block all nearby improvements. Local non-satiation alone does not guarantee that an optimum exists.
