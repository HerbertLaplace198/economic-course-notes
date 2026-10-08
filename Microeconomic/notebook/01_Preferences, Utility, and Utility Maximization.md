---
title: 01_Econometrics
author: Laplace
tags:
  - Microeconomic
  - JCER
  - economics
date: 2026-10-07
status: Editing
type: Course
---
# ***A.[[PRIMITIVE NOTIONS]]***
## *The Consumption Set*

***the consumption set***, $X$, represent the set of all alternatives, or complete consumption plans, that the consumer can conceive – whether some of them will be achievable in practice or no.

## *The Feasible Set*

 ***the feasible set***, $B$, represent all those alternative consumption plans that are both conceivable and, more important, realistically obtainable given the consumer’s circumstances.
 
## *Preference Relation*

***preference relation***, typically specifies the limits, if any, on the consumer’s ability to perceive in situations involving choice the form of consistency or inconsistency in the consumer’s choices, and information about the consumer’s tastes for the different objects of choice. 

## *Behavioural assumption*

***behavioural assumption***, expresses the guiding principle the consumer uses to make final choices and so identifies the ultimate objectives in choice.

# ***B.[[PREFERENCE RELATION|PREFERENCE RELATION]]***

## *Definition 1.B.1 — Preference Relation*

The binary relation $\succsim$ on the consumption set $X$ is called a **preference relation** if it satisfies Axioms 1 and 2.

There are two additional relations that we will use in our discussion of consumer preferences. Each is determined by the preference relation, $\succsim$, and they formalise the notions of **strict preference** and **indifference**.
## *Definition 1.B.2 — Strict Preference Relation*

The binary relation $\succ$ on the consumption set $X$ is defined as follows:

$$  
\mathbf{x}^{1}\succ\mathbf{x}^{2}  
\quad\text{if and only if}\quad  
\mathbf{x}^{1}\succsim\mathbf{x}^{2}  
\quad\text{and}\quad  
\mathbf{x}^{2}\not\succsim\mathbf{x}^{1}.  
$$

The relation $\succ$ is called the **strict preference relation induced by $\succsim$**, or simply the strict preference relation when $\succsim$ is clear. The phrase $\mathbf{x}^{1}\succ\mathbf{x}^{2}$ is read, “$\mathbf{x}^{1}$ is strictly preferred to $\mathbf{x}^{2}$”.

## *Definition 1.B.3 — Indifference Relation*

The binary relation $\sim$ on the consumption set $X$ is defined as follows:

$$  
\mathbf{x}^{1}\sim\mathbf{x}^{2}  
\quad\text{if and only if}\quad  
\mathbf{x}^{1}\succsim\mathbf{x}^{2}  
\quad\text{and}\quad  
\mathbf{x}^{2}\succsim\mathbf{x}^{1}.  
$$

The relation $\sim$ is called the **indifference relation induced by $\succsim$**, or simply the indifference relation when $\succsim$ is clear. The phrase $\mathbf{x}^{1}\sim\mathbf{x}^{2}$ is read, “$\mathbf{x}^{1}$ is indifferent to $\mathbf{x}^{2}$”.

## *Definition 1.B.4 — Sets in $X$ Derived from the Preference Relation*

Let $\mathbf{x}^{0}$ be any point in the consumption set, $X$. Relative to any such point, we can define the following subsets of $X$:

1. $\succsim(\mathbf{x}^{0})\equiv{\mathbf{x}\mid\mathbf{x}\in X,\ \mathbf{x}\succsim\mathbf{x}^{0}}$, called the **“at least as good as” set**.

2. $\precsim(\mathbf{x}^{0})\equiv{\mathbf{x}\mid\mathbf{x}\in X,\ \mathbf{x}^{0}\succsim\mathbf{x}}$, called the **“no better than” set**.

3. $\prec(\mathbf{x}^{0})\equiv{\mathbf{x}\mid\mathbf{x}\in X,\ \mathbf{x}^{0}\succ\mathbf{x}}$, called the **“worse than” set**.

4. $\succ(\mathbf{x}^{0})\equiv{\mathbf{x}\mid\mathbf{x}\in X,\ \mathbf{x}\succ\mathbf{x}^{0}}$, called the **“preferred to” set**.

5. $\sim(\mathbf{x}^{0})\equiv{\mathbf{x}\mid\mathbf{x}\in X,\ \mathbf{x}\sim\mathbf{x}^{0}}$, called the **“indifference” set**.

##  *Proposition 1.B.1:* 

if $\succcurlyeq$ is rational then:

(i) $\succ$ is both **irreflexive** ($x\succ x$ never holds) and **transitive** (if $x\succ y$ and $y\succ z$, then $x\succ z$).

(ii) $\sim$ is **reflexive** ($x\sim x$ for all $x$), **transitive** (if $x\sim y$ and $y\sim z$, then $x\sim z$), and **symmetric** (if $x\sim y$, then $y\sim x$).

(iii) If $x\succ y\succcurlyeq z$, then $x\succ z$.

# ***C.[[UTILITY FUNCTIONS]]***

## *Definition 1.C.1*

A function $u\to\mathbb{R}$ is a **utility function representing preference relation** $\succcurlyeq$ if, for all $x,y\in X$,

$$  
x\succcurlyeq y  
\quad\Longleftrightarrow\quad  
u(x)\geq u(y).  
$$
## **

A strictly increasing transformation of a utility function preserves the preference relation it represents:

$$
v=f\circ u,\qquad f\text{ strictly increasing on }u(X).
$$

**Proposition 1.C.2:** A preference relation $\succcurlyeq$ can be represented by a utility function only if it is rational.