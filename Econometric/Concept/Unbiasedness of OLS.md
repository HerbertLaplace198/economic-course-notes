> [!definition]
> An estimator $\hat\theta$ is **unbiased** for a parameter $\theta$ if
> $$
> E(\hat\beta)=\beta.
> $$
> The expectation is taken over repeated random samples. Unbiasedness does not mean that an estimate from any particular sample equals the true parameter.

## Unbiasedness of OLS

Consider the simple linear regression model

$$
y_i=\beta_0+\beta_1x_i+u_i.
$$

Suppose the observations form a [[Random Sampling|random sample]], the Explanatory Variable has [[Sample Variation in the Explanatory Variable|sample variation]], and the error satisfies [[Zero Conditional Mean]]:

 Since $SST_x=\sum_{i=1}^{n}(x_i-\bar x)^2$. By sample variation, $SST_x>0$. The OLS slope is

$$
\hat\beta_1
=\frac{\sum_{i=1}^{n}(x_i-\bar x)(y_i-\bar y)}{SST_x}
=\frac{\sum_{i=1}^{n}(x_i-\bar x)y_i}{SST_x},
$$

because $\sum_{i=1}^{n}(x_i-\bar x)=0$. Substituting $y_i=\beta_0+\beta_1x_i+u_i$ gives

$$
\begin{aligned}
\hat\beta_1
&=\frac{\sum_{i=1}^{n}(x_i-\bar x)(\beta_0+\beta_1x_i+u_i)}{SST_x}\\[1em]
&=\beta_0\frac{\sum_{i=1}^{n}(x_i-\bar x)}{SST_x}
+\beta_1\frac{\sum_{i=1}^{n}(x_i-\bar x)x_i}{SST_x}
+\frac{\sum_{i=1}^{n}(x_i-\bar x)u_i}{SST_x}\\[1.2em]
&=\beta_1+\frac{\sum_{i=1}^{n}(x_i-\bar x)u_i}{SST_x}
\end{aligned}
$$

where $\sum_{i=1}^{n}(x_i-\bar x)x_i=SST_x$.

Let $\mathbf{x}=(x_1,\ldots,x_n)$. Random Sampling and Zero Conditional Mean imply $E(u_i\mid\mathbf{x})=0$. Conditional on $\mathbf{x}$, the values of $x_i$, $\bar x$, and $S_{xx}$ are fixed. Hence,

$$
\begin{aligned}
E(\hat\beta_1\mid\mathbf{x})
&=\beta_1+
\frac{\sum_{i=1}^{n}(x_i-\bar x)E(u_i\mid\mathbf{x})}{SST_x}\\
&=\beta_1
\end{aligned}
$$

For the intercept, $\bar y=\beta_0+\beta_1\bar x+\bar u$, so

$$
\hat\beta_0
=\bar y-\hat\beta_1\bar x
=\beta_0+\bar u-(\hat\beta_1-\beta_1)\bar x.
$$

Since $E(\bar u\mid\mathbf{x})=0$ and $E(\hat\beta_1\mid\mathbf{x})=\beta_1$,

$$
E(\hat\beta_0\mid\mathbf{x})=\beta_0.
$$

Taking expectations again gives $E(\hat\beta_0)=\beta_0$ and $E(\hat\beta_1)=\beta_1$. 
