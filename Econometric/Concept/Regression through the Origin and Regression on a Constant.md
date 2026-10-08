> [!definition]
> **Regression through the origin** fixes the intercept at zero. **Regression on a constant** fixes the slope at zero. Both are restricted forms of the [[Sample Regression Function (SRF)]].

## Regression through the origin 

### Estimator 

Suppose the true model contains an intercept,

$$  
y_i=\beta_0+\beta_1x_i+u_i,  
$$

but we estimate a regression through the origin. Since the slope estimator is $\tilde\beta_1=\dfrac{\sum_{i=1}^{n}x_iy_i}{\sum_{i=1}^{n}x_i^2}$, substituting the true model gives

$$  
\begin{aligned}  
\tilde\beta_1  
&=\frac{\sum_{i=1}^{n}x_i(\beta_0+\beta_1x_i+u_i)}  
{\sum_{i=1}^{n}x_i^2}\\[0.8em]  
&=\beta_0\frac{\sum_{i=1}^{n}x_i}{\sum_{i=1}^{n}x_i^2}  
+\beta_1\frac{\sum_{i=1}^{n}x_i^2}{\sum_{i=1}^{n}x_i^2}  
+\frac{\sum_{i=1}^{n}x_iu_i}{\sum_{i=1}^{n}x_i^2}\\[0.8em]  
&=\beta_1  
+\beta_0\frac{\sum_{i=1}^{n}x_i}{\sum_{i=1}^{n}x_i^2}  
+\frac{\sum_{i=1}^{n}x_iu_i}{\sum_{i=1}^{n}x_i^2}.  
\end{aligned}  
$$

Conditional on $\mathbf{x}=(x_1,\ldots,x_n)$, the observed $x_i$ values are fixed. If [[Zero Conditional Mean]] holds, $E(u_i\mid\mathbf{x})=0$, so

$$  
\begin{aligned}  
E(\tilde\beta_1\mid\mathbf{x})  
&=\beta_1  
+\beta_0\frac{\sum_{i=1}^{n}x_i}{\sum_{i=1}^{n}x_i^2}  
+\frac{\sum_{i=1}^{n}x_iE(u_i\mid\mathbf{x})}  
{\sum_{i=1}^{n}x_i^2}\\[0.8em]  
&=\beta_1  
+\beta_0\frac{\sum_{i=1}^{n}x_i}{\sum_{i=1}^{n}x_i^2}.  
\end{aligned}  
$$

Therefore, the conditional bias is

$$  
E(\tilde\beta_1\mid\mathbf{x})-\beta_1  
=\beta_0\frac{\sum_{i=1}^{n}x_i}{\sum_{i=1}^{n}x_i^2}  
=\beta_0\frac{n\bar x}{\sum_{i=1}^{n}x_i^2}.  
$$

When the intercept is omitted, the slope absorbs part of its effect if $\beta_0\ne0$ and $\bar x\ne0$. If $\sum_{i=1}^{n}x_i=0$, this conditional bias is zero even when $\beta_0\ne0$.

### Conditional variance

From the expression above, conditional on $\mathbf{x}$, both $\beta_1$ and $\beta_0\dfrac{\sum_i x_i}{\sum_i x_i^2}$ are constants. Only the term containing $u_i$ varies across samples. Therefore,

$$  
\begin{aligned}  
\operatorname{Var}(\tilde\beta_1\mid\mathbf{x})  
&=\operatorname{Var}\left(  
\frac{\sum_{i=1}^{n}x_iu_i}{\sum_{i=1}^{n}x_i^2}  
\middle|\mathbf{x}\right)\\[0.8em]  
&=\frac{1}{\left(\sum_{i=1}^{n}x_i^2\right)^2}  
\operatorname{Var}\left(\sum_{i=1}^{n}x_iu_i  
\middle|\mathbf{x}\right).  
\end{aligned}  
$$

If the errors are conditionally uncorrelated across observations and [[Homoskedasticity]] gives $\operatorname{Var}(u_i\mid\mathbf{x})=\sigma^2$, then

$$  
\begin{aligned}  
\operatorname{Var}(\tilde\beta_1\mid\mathbf{x})  
&=\frac{\sum_{i=1}^{n}x_i^2\operatorname{Var}(u_i\mid\mathbf{x})}  
{\left(\sum_{i=1}^{n}x_i^2\right)^2}\\[0.8em]  
&=\boxed{\frac{\sigma^2}{\sum_{i=1}^{n}x_i^2}}.  
\end{aligned}  
$$

Omitting the intercept shifts the conditional mean of $\tilde\beta_1$, but the omitted constant does not itself add conditional variance. The estimator can therefore have a small variance while still being biased. Its conditional [[Mean Squared Error (MSE)|mean squared error]] includes both:
$$
\frac{\sigma^2}{\sum_i x_i^2}  
+  
\left(  
\beta_0\frac{\sum_i x_i}{\sum_i x_i^2}  
\right)^2.  
$$

## Regression on a constant

>[!definition]
> A **regression through a fixed point** constrains its fitted line to pass through a specified point $(x_0,y_0)$. For a candidate slope $\beta_1$, write the predicted value as
> $$
> \hat y_i(\beta_1)=y_0+\beta_1(x_i-x_0).
> $$
> At $x_i=x_0$, the predicted value is $y_0$ for every choice of slope. The point $(x_0,y_0)$ is specified in advance.

#### Estimator

OLS chooses the slope that minimizes the residual sum of squares:

$$
SSR=\sum_{i=1}^{n}\left[y_i-y_0-\beta_1(x_i-x_0)\right]^2.
$$

Differentiate with respect to $\beta_1$ and set the derivative to zero at the minimizing value $\tilde\beta_1$:

$$
\begin{aligned}
&=\sum_{i=1}^{n}(x_i-x_0)
  \left[y_i-y_0-\tilde\beta_1(x_i-x_0)\right]\\[0.8em]
&=\sum_{i=1}^{n}(x_i-x_0)(y_i-y_0)
  -\tilde\beta_1\sum_{i=1}^{n}(x_i-x_0)^2=0.
\end{aligned}
$$

Solving for the slope gives

$$
\boxed{
\tilde\beta_1
=\frac{\sum_{i=1}^{n}(x_i-x_0)(y_i-y_0)}
       {\sum_{i=1}^{n}(x_i-x_0)^2}
}.
$$

The denominator must be positive: at least one observed $x_i$ must differ from $x_0$. The estimator uses each observation's coordinates relative to the fixed point.

## Conditional variance

Suppose the [[Population Regression Function (PRF)|population regression]] line passes through the specified point:

$$
y_i=y_0+\beta_1(x_i-x_0)+u_i.
$$

Substituting this model into the estimator gives

$$
\begin{aligned}
\tilde\beta_1
&=\frac{\sum_{i=1}^{n}(x_i-x_0)
  [\beta_1(x_i-x_0)+u_i]}
  {\sum_{i=1}^{n}(x_i-x_0)^2}\\[0.8em]
&=\beta_1+
  \frac{\sum_{i=1}^{n}(x_i-x_0)u_i}
       {\sum_{i=1}^{n}(x_i-x_0)^2}.
\end{aligned}
$$

Conditional on $\mathbf{x}=(x_1,\ldots,x_n)$, the $x_i$, $x_0$, and $y_0$ are fixed. If Zero Conditional Mean gives $E(u_i\mid\mathbf{x})=0$, then $E(\tilde\beta_1\mid\mathbf{x})=\beta_1$. If the errors are also conditionally uncorrelated across observations and Homoskedasticity gives $\operatorname{Var}(u_i\mid\mathbf{x})=\sigma^2$, then

$$
\begin{aligned}
\operatorname{Var}(\tilde\beta_1\mid\mathbf{x})
&=\frac{\sum_{i=1}^{n}(x_i-x_0)^2\sigma^2}
       {\left[\sum_{i=1}^{n}(x_i-x_0)^2\right]^2}\\[0.8em]
&=\boxed{\frac{\sigma^2}{\sum_{i=1}^{n}(x_i-x_0)^2}}.
\end{aligned}
$$
