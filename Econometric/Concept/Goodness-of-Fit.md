>[!definition]
> **Goodness-of-fit** describes how closely a statistical model's fitted values match the observed values of the [[Dependent Variable]].

For the regression model

$$
y_i
=
\beta_0+\beta_1x_{i1}+\cdots+\beta_kx_{ik}+u_i,
$$

the fitted value is

$$
\hat y_i
=
\hat\beta_0+\hat\beta_1x_{i1}+\cdots+\hat\beta_kx_{ik},
$$

and the Residual is

$$
\hat u_i=y_i-\hat y_i.
$$

A model fits the sample more closely when its residuals are small relative to the total sample variation in $y$.

That is,

$$
SST=SSE+SSR,
$$

where:

- $SST$ is the [[Total Sum of Squares (SST)]].
- $SSE$ is the [[Explained Sum of Squares (SSE)]].
- $SSR$ is the [[Residual Sum of Squares (SSR)]].

The goodness-of-fit is measured by the coefficient of determination:

$$
R^2=\frac{SSE}{SST}
=1-\frac{SSR}{SST}.
$$

A model fits the sample more closely when $SSR$ is small relative to $SST$, or equivalently when $R^2$ is close to one.

