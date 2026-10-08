---
logical_role: derived_result
---
Let $x^*(\theta)$ maximize $f(x,\theta)$ over a choice set that does not depend on $\theta$. The **value function** records the best attainable value:

$$
V(\theta)=f(x^*(\theta),\theta)=\max_x f(x,\theta).
$$

At a point where $V$ is differentiable, the **envelope theorem** gives

$$
\boxed{V'(\theta)=
\left.\frac{\partial f(x,\theta)}{\partial\theta}\right|_{x=x^*(\theta)}}.
$$

For a differentiable **interior** optimum, the chain rule shows why:

$$
\begin{aligned}
V'(\theta)
&=\frac{\partial f}{\partial\theta}
+\nabla_x f\cdot\frac{dx^*}{d\theta}\\[0.8em]
&=\frac{\partial f}{\partial\theta},
\end{aligned}
$$

because the first-order condition is $\nabla_x f=0$ at $x^*$. The optimal choice **can change** with $\theta$; its adjustment has no first-order effect on the optimized value.

## When the constraint also changes

For the consumer problem over a budget set,

$$
v(p,m)=\max_{x:\,p\cdot x\leq m}u(x),
\qquad
\mathcal L=u(x)+\lambda(m-p\cdot x),
$$

the constrained envelope theorem differentiates the **Lagrangian** with respect to the parameter. Where the required derivatives exist,

$$
\boxed{\frac{\partial v}{\partial m}=\lambda^*},
\qquad
\boxed{\frac{\partial v}{\partial p_j}=-\lambda^*x_j^*}.
$$

Thus, $\lambda^*$ is the marginal value of additional income; a small increase in the price of good $j$ reduces maximized utility at a rate determined by its chosen quantity and that marginal value.
