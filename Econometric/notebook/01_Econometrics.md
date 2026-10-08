---
title: 01_Econometric
author: Laplace
tags:
  - economics
  - JCER
  - econometrics
date: 2026-09-15
status: Finished
type: Course
---
Just Introduction !  ！！ 

### Model 

#### 1. Mathematical Model

$$
Y = \beta X
$$

- $Y$: dependent variable
- $X$: independent variable
- $\beta$: parameter

----

####  2. Economic Model

$$
Q = f(K,L)
$$

- $Q$: output
- $K$: capital
- $L$: labor
- $f(\cdot)$: production function

----

#### 3. Econometric Model

$$
Q_i = \alpha + \beta_1 K_i + \beta_2 L_i + \varepsilon_i
$$


- $Q_i$: output
- $K_i$: capital
- $L_i$: labor
- $\alpha$: intercept
- $\beta_1$: coefficient of capital
- $\beta_2$: coefficient of labor
- $\varepsilon_i$: error term

---

### Data Types

#### 1. Cross-sectional Data

Cross-sectional data observe **multiple individuals at a single point in time**.

$$
\{Y_i, X_i\}_{i=1}^{N}
$$

- $i$: individual
- $N$: number of individuals
- One time period
- Example: GDP, population, and unemployment rates of 100 countries in 2025

---

#### 2. Time Series Data

Time series data observe **a single individual over multiple time periods**.

$$
\{Y_t, X_t\}_{t=1}^{T}
$$

- $t$: time
- $T$: number of time periods
- One individual
- Example: China's GDP from 2000 to 2025

---

#### 3. Panel Data

Panel data combine **individual and time dimensions**.

$$
\{Y_{it}, X_{it}\}_{i=1,\ldots,N;\ t=1,\ldots,T}
$$

- $i$: individual
- $t$: time
- $N$: number of individuals
- $T$: number of time periods
- Multiple individuals observed over multiple time periods
- Example: GDP of 100 countries from 2000 to 2025

---

#### 4. Pooled Cross-sectional Data

Pooled cross-sectional data combine **cross-sectional samples from different time periods**.

$$
\{Y_{it}, X_{it}\}
$$

The individuals **do not have to be the same** across different periods.

Example:

- Survey 1,000 households in 2020
- Survey another 1,000 households in 2021
- The households in 2020 and 2021 are not necessarily the same
- Combine the two samples → Pooled Cross-sectional Data

---

#### 5. Basic Structure

##### Cross-sectional

$$
i
$$

##### Time Series

$$
t
$$

##### Panel

$$
(i,t)
$$

##### Pooled Cross-sectional

$$
(i,t), \quad \text{but } i \text{ may differ across } t
$$