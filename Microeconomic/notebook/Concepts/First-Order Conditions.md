---
title: "First-Order Conditions"
author: Laplace
tags:
  - economics
  - JCER
date: 2026-09-30
status: Editing
type: Concept
logical_role: derived_result
---
> [!definition]
> **First-order conditions (FOCs)** state what a differentiable local optimum must satisfy to first order. At an interior optimum, a feasible change in either direction cannot raise the objective, so its directional derivative is zero. At a boundary, only one-sided changes are feasible and the condition becomes an inequality.
>
> In the consumer problem with $p\gg0$ and $m>0$,
>
> $$
> \max_{x\in\mathbb R_+^n}u(x)
> \qquad\text{subject to}\qquad p\cdot x\leq m,
> $$
>
> if $u$ is continuously differentiable near an **interior** optimum $x^*\gg0$ and the budget binds, then there is a multiplier $\lambda\geq0$ such that
>
> $$
> \frac{\partial u(x^*)}{\partial x_i}=\lambda p_i
> \quad(i=1,\ldots,n),
> \qquad p\cdot x^*=m.
> $$

## Interpretation

The utility-maximizing choice is the object of interest; FOCs are a way to **characterize a candidate** for that choice. The interior equations equate marginal utility per unit of expenditure across goods:

$$
\frac{\partial u(x^*)/\partial x_i}{p_i}=\lambda
\qquad(i=1,\ldots,n).
$$

If spending one unit of money on good $i$ raised utility more than spending it on good $j$, a small reallocation from $j$ to $i$ would improve the bundle. The common $\lambda$ is the budget multiplier. When the optimized value is differentiable in income, it equals that derivative in the chosen utility units; its numerical value changes under an increasing transformation of $u$.

These conditions are **necessary under their stated assumptions, not automatically sufficient**. A stationary point may be a minimum, and an interior candidate may violate non-negativity or fail to be globally best. A corner optimum requires the inequality conditions below. No derivative-based FOC applies at a point where the relevant derivative does not exist.

## Derivation

For the standard budget set $B(p,m)$, [[Walras' Law]] gives $p\cdot x^*=m$ when preferences are locally non-satiated and an optimum exists. Suppose $x^*\gg0$, so small reallocations between any two goods are feasible in both directions. For distinct $i,j$, let

$$
d=\frac{e_i}{p_i}-\frac{e_j}{p_j},
\qquad p\cdot d=0.
$$

Because $x^*+td$ remains on the budget plane for sufficiently small positive and negative $t$, the function $t\mapsto u(x^*+td)$ has an interior local maximum at $t=0$. Differentiating yields

$$
\begin{aligned}
0
&=\left.\frac{d}{dt}u(x^*+td)\right|_{t=0}\\[0.8em]
&=\frac{1}{p_i}\frac{\partial u(x^*)}{\partial x_i}
-\frac{1}{p_j}\frac{\partial u(x^*)}{\partial x_j}.
\end{aligned}
$$

Thus every marginal-utility-to-price ratio has a common value $\lambda$. A small decrease in any good is feasible, so optimality requires each marginal utility to be nonnegative; since $p_i>0$, this gives $\lambda\geq0$. The Lagrangian collects the same conditions:

$$
\mathcal L(x,\lambda)=u(x)+\lambda(m-p\cdot x),
$$

$$
\frac{\partial\mathcal L}{\partial x_i}
=\frac{\partial u}{\partial x_i}-\lambda p_i=0,
\qquad
\frac{\partial\mathcal L}{\partial\lambda}=m-p\cdot x=0.
$$

When $\lambda>0$, the marginal utilities are positive, and dividing the equations for goods $i$ and $j$ gives the **tangency condition**

$$
\operatorname{MRS}_{ij}(x^*)
:=\frac{\partial u(x^*)/\partial x_i}
{\partial u(x^*)/\partial x_j}
=\frac{p_i}{p_j}.
$$

Budget exhaustion or local non-satiation alone does **not** imply $\lambda>0$; without a nonzero denominator this ratio is undefined even though the original FOCs still make sense.

### Boundary solutions

For $x_i\geq0$ and $p\cdot x\leq m$, the Kuhn–Tucker Lagrangian is

$$
\mathcal L(x,\lambda,\mu)
=u(x)+\lambda(m-p\cdot x)+\sum_{i=1}^n\mu_i x_i.
$$

Under differentiability and a constraint qualification, a local optimum satisfies

$$
\begin{aligned}
\frac{\partial u(x^*)}{\partial x_i}-\lambda p_i+\mu_i&=0\quad(i=1,\ldots,n),\\[0.8em]
p\cdot x^*&\leq m,\quad x_i^*\geq0,\\[0.8em]
\lambda&\geq0,\quad \mu_i\geq0,\\[0.8em]
\lambda(m-p\cdot x^*)&=0,\quad \mu_i x_i^*=0.
\end{aligned}
$$

Consequently,

$$
x_i^*>0\ \Longrightarrow\ \frac{\partial u(x^*)}{\partial x_i}=\lambda p_i,
\qquad
x_i^*=0\ \Longrightarrow\ \frac{\partial u(x^*)}{\partial x_i}\leq\lambda p_i.
$$

The zero-consumption good need not satisfy tangency equality: its first unit is not valuable enough, relative to its price, to displace goods already purchased.

### When the interior conditions are sufficient

Suppose $u$ is continuous and quasi-concave on $\mathbb R_+^n$, differentiable at an interior $x^*$, and $\lambda>0$ satisfies $\nabla u(x^*)=\lambda p$ and $p\cdot x^*=m$. Then $x^*$ is a **global maximum** on the budget set.

To see why, suppose a feasible $x'$ gave $u(x')>u(x^*)$. By continuity, choose $t<1$ close enough to $1$ that $y=tx'$ still gives $u(y)>u(x^*)$; it also has $p\cdot y<m$. Quasi-concavity implies

$$
u\bigl(x^*+s(y-x^*)\bigr)\geq u(x^*)
\qquad(0\leq s\leq1).
$$

Differentiating at $s=0$ from the right gives $\nabla u(x^*)\cdot(y-x^*)\geq0$. Yet the FOC gives

$$
\nabla u(x^*)\cdot(y-x^*)
=\lambda(p\cdot y-m)<0,
$$

a contradiction. Concavity is a stronger, easier-to-use sufficient condition; quasi-concavity is enough here. Strict quasi-concavity additionally makes the maximizer unique on the convex budget set.

## Example

Following the lecture, take $u(x_1,x_2)=x_1+2\sqrt{x_2}$, $p=(1,1)$, and first set $m=3$. The interior FOCs give

$$
1=\lambda,
\qquad
\frac{1}{\sqrt{x_2}}=\lambda,
\qquad
x_1+x_2=3.
$$

Hence $\lambda=1$, $x_2^*=1$, and $x_1^*=2$. The candidate is feasible and interior; because $u$ is concave, it is a global maximum.

Now set $m=\tfrac12$. The same interior equations would give $x_2=1$ and $x_1=-\tfrac12$, which is infeasible. At the corner $x_1^*=0$, $x_2^*=\tfrac12$,

$$
\lambda=\frac{1}{\sqrt{1/2}}=\sqrt2,
\qquad
\mu_1=\lambda-1=\sqrt2-1>0,
\qquad
\mu_2=0.
$$

The consumed good satisfies equality, while the unconsumed good satisfies $1\leq\lambda p_1=\sqrt2$. This is why the interior tangency equations cannot be applied to every optimum.

## Connections

- Behavioural Assumption poses the maximization problem; FOCs characterize differentiable candidates within its feasible set.
- [[Envelope Theorem]] uses the stationarity of an optimal choice when differentiating the optimized value.

