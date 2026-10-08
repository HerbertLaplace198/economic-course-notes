>[!definition]
> A regression model is **linear in parameters** if the unknown parameters enter the model linearly. The model can be written as
> $$
> y_i=\beta_0+\beta_1z_{i1}+\cdots+\beta_kz_{ik}+u_i,
> $$
> where each $z_{ij}$ is an observed variable or a known transformation of observed variables and does not depend on the unknown parameters.

In matrix notation,

$$
y=X\beta+u.
$$

The parameters $\beta_0,\beta_1,\ldots,\beta_k$ must appear additively, be rai