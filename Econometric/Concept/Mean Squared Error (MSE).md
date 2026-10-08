> [!definition]
> The **mean squared error (MSE)** of an estimator $\hat\theta$ for a target parameter $\theta$ is the expected squared distance between them:
> $$
> \operatorname{MSE}(\hat\theta)=E\!\left[(\hat\theta-\theta)^2\right].
> $$
> A smaller MSE means that, across repeated samples, estimates tend to be closer to the target.

## Variance and bias

Let $\mu=E(\hat\theta)$. Write the estimation error as

$$
\hat\theta-\theta
=
\underbrace{(\hat\theta-\mu)}_{\text{variation around its mean}}
+
\underbrace{(\mu-\theta)}_{\text{bias}}.
$$

Squaring and taking expectations gives

$$
\boxed{
\operatorname{MSE}(\hat\theta)
=
\operatorname{Var}(\hat\theta)
+
\left[E(\hat\theta)-\theta\right]^2
}.
$$

The cross term disappears because $E(\hat\theta-\mu)=0$. Thus, variance measures how much the estimator fluctuates around **its own mean**, while squared bias measures how far that mean is from the target. If an estimator is unbiased, its MSE equals its variance. For OLS, see [[Unbiasedness of OLS]] and [[Variances of the OLS Estimators]].

## Conditional MSE

When an estimator depends on observed explanatory variables $\mathbf{x}$, the same identity holds conditional on $\mathbf{x}$:

$$
\operatorname{MSE}(\hat\theta\mid\mathbf{x})
=
E\!\left[(\hat\theta-\theta)^2\mid\mathbf{x}\right]
=
\operatorname{Var}(\hat\theta\mid\mathbf{x})
+
\left[E(\hat\theta\mid\mathbf{x})-\theta\right]^2.
$$

For the slope estimated by [[Regression through the Origin and Regression on a Constant|regression through the origin]] when the true model contains an intercept,

$$
\operatorname{MSE}(\tilde\beta_1\mid\mathbf{x})
=
\underbrace{\frac{\sigma^2}{\sum_i x_i^2}}_{\text{conditional variance}}
+
\underbrace{\left(
\beta_0\frac{\sum_i x_i}{\sum_i x_i^2}
\right)^2}_{\text{conditional bias squared}}.
$$

Omitting the intercept can reduce the estimator's variance while increasing its bias. MSE accounts for both when evaluating its distance from $\beta_1$.

## Terminology in regression output

**MSE of an estimator** must be distinguished from the **residual mean square** sometimes labeled “MSE” in regression output. In simple OLS with an intercept, the latter is $\hat\sigma^2=SSR/(n-2)$, and *Root MSE* is $\hat\sigma$. These describe residual variation; they are not the MSE of $\hat\beta_1$.
