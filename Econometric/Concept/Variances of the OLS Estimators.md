> [!definition]
> The **sampling variance** of an estimator measures how much the estimator varies across repeated samples. The OLS variance formulas below are **conditional on the observed values** of the explanatory variable.

Consider the simple regression model

$$
y_i=\beta_0+\beta_1x_i+u_i.
$$

The model is linear in parameters. Define $SST_x=\sum_{i=1}^{n}(x_i-\bar x)^2.$By [[Sample Variation in the Explanatory Variable|sample variation]], $SST_x>0$, so the OLS slope is defined. $SST_x$ is the total sum of squares of $x$, analogous to [[Total Sum of Squares (SST)]] for $y$.

## Variance of the error term

The population error $u_i=y_i-(\beta_0+\beta_1x_i)$ is unobserved. After fitting the regression line, we can calculate the residual $\hat u_i=y_i-\hat y_i$. These are different quantities.

Under [[Zero Conditional Mean]] and [[Homoskedasticity]],

$$
E(u_i\mid x_i)=0,
\qquad
\operatorname{Var}(u_i\mid x_i)=\sigma^2.
$$

Because $\operatorname{Var}(u_i\mid x_i)=E(u_i^2\mid x_i)-[E(u_i\mid x_i)]^2$, we have $E(u_i^2\mid x_i)=\sigma^2$. If the true errors were observable, their squared average would estimate the error variance:

$$
\tilde\sigma^2=\frac{1}{n}\sum_{i=1}^{n}u_i^2,
\qquad
E(\tilde\sigma^2\mid\mathbf{x})=\sigma^2.
$$

The denominator is $n$ because this averages $n$ squared errors. The error mean of zero is specified by the model; it is not estimated from the sample.

In practice, we use residuals after estimating both $\beta_0$ and $\beta_1$:

$$
\hat u_i=y_i-\hat\beta_0-\hat\beta_1x_i,
\qquad
SSR=\sum_{i=1}^{n}\hat u_i^2.
$$

OLS with an intercept imposes two restrictions on the residuals:

$$
\sum_{i=1}^{n}\hat u_i=0,
\qquad
\sum_{i=1}^{n}x_i\hat u_i=0.
$$

Under the regression assumptions used here, $E(SSR\mid\mathbf{x})=(n-2)\sigma^2$. Thus, the unbiased estimator of the error variance is

$$
\boxed{\hat\sigma^2=\frac{SSR}{n-2}
=\frac{\sum_{i=1}^{n}(y_i-\hat y_i)^2}{n-2}}.
$$

For example, when $n=10$, the expected $SSR$ is $8\sigma^2$. Dividing by $10$ would give an expected value of $0.8\sigma^2$; dividing by $8$ gives $\sigma^2$. The two degrees of freedom are used to estimate the intercept and slope. See [[Residual Sum of Squares (SSR)]].

## Variance of the slope estimator

Let $\mathbf{x}=(x_1,\ldots,x_n)$. Under the conditions of [[Unbiasedness of OLS]], including Zero Conditional Mean, $E(\hat\beta_1\mid\mathbf{x})=\beta_1$. The slope estimation error can be written as:

$$
\hat\beta_1-\beta_1
=
\frac{\sum_{i=1}^{n}(x_i-\bar x)u_i}{SST_x}.
$$

Conditional on $\mathbf{x}$, the $x_i$ and $SST_x$ are fixed. [[Random Sampling]] implies that the errors are independent across observations. Homoskedasticity gives $\operatorname{Var}(u_i\mid\mathbf{x})=\sigma^2$ for every $i$. Therefore,

$$
\operatorname{Var}(\hat\beta_1\mid\mathbf{x})
=
\frac{1}{SST_x^2}
\sum_{i=1}^{n}(x_i-\bar x)^2\sigma^2
=
\boxed{\frac{\sigma^2}{SST_x}}.
$$

## Variance of the intercept estimator

Using $\hat\beta_0=\bar y-\hat\beta_1\bar x$ and $\bar y=\beta_0+\beta_1\bar x+\bar u$,

$$
\hat\beta_0-\beta_0
=
\bar u-\bar x(\hat\beta_1-\beta_1).
$$

Conditional on $\mathbf{x}$,

$$
\operatorname{Var}(\bar u\mid\mathbf{x})=\frac{\sigma^2}{n},
\qquad
\operatorname{Cov}(\bar u,\hat\beta_1\mid\mathbf{x})
=
\frac{\sigma^2}{nSST_x}
\sum_{i=1}^{n}(x_i-\bar x)=0.
$$

Hence,

$$
\begin{aligned}
\operatorname{Var}(\hat\beta_0\mid\mathbf{x})
&=\operatorname{Var}(\bar u\mid\mathbf{x})
+\bar x^2\operatorname{Var}(\hat\beta_1\mid\mathbf{x})\\[0.8em]
&=\boxed{\sigma^2\left(\frac{1}{n}+\frac{\bar x^2}{SST_x}\right)}.
\end{aligned}
$$

A larger error variance $\sigma^2$ makes the estimates less precise. More variation in $x$ increases $SST_x$ and reduces the variance of the slope estimator. These formulas use Homoskedasticity; the unbiasedness result in Unbiasedness of OLS does not.
