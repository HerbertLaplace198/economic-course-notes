> [!question] Question 1 — Simple Linear Regression  
> Please use the CEOSEAL1.dta (STATA format) data in the course
data package to run a simple linear regression, where Y is salary and
X is roe. Please explain how the standard error 11.12325 after the
estimated parameter of the explanatory variable 18.50119 is
obtained.

我怕说不清楚我先用中文举例子重复一下我的理解(后面有英文"正式?"的回答)
就像物理学中的加速度，有定义式 $\mathbf{a}=\frac{d\mathbf{v}}{dt}$，决定式 $\mathbf{a}=\frac{\mathbf{F}_{\mathrm{net}}}{m}$
stata中的beta的计算方式就是利用决定式子，因为beta的变异来源于抽样产生的cov(u，x)，所以他的variance自然而然是u的函数，我们重复抽样就是类似于定义式，来计算beta的variance。


In the proof of unbiasedness we have this formula:
$$
\hat\beta_1-\beta_1
=
\frac{\sum_{i=1}^{n}(x_i-\bar x)u_i}{SST_x}.
$$
Condition on the observed explanatory values $\mathbf{x}=(x_1,\ldots,x_n)$. Imagine repeatedly drawing new errors while holding these $x$ values fixed. Each draw can produce a different $\hat\beta_1$, so $\hat\beta_1\mid\mathbf{x}$ has a sampling distribution.

 $E(u_i\mid\mathbf{x})=0$. it does **not** say that every realized $u_i$ is zero. In a particular sample, the errors can therefore produce a nonzero estimation error:

$$  
\hat\beta_1-\beta_1  
=\frac{\sum_{i=1}^{n}(x_i-\bar x)u_i}{SST_x}.  
$$

By [[Unbiasedness of OLS]], $E(\hat\beta_1\mid\mathbf{x})=\beta_1$. Hence,

$$  
\begin{aligned}  
\operatorname{Var}(\hat\beta_1\mid\mathbf{x})  
&=E\left[(\hat\beta_1-\beta_1)^2\mid\mathbf{x}\right]\\[0.8em]  
&=\operatorname{Var}\left(  
\frac{\sum_{i=1}^{n}(x_i-\bar x)u_i}{SST_x}  
\middle|\mathbf{x}\right)\\[0.8em]  
&=\frac{1}{SST_x^2}  
\sum_{i=1}^{n}(x_i-\bar x)^2\sigma^2\\[0.8em]  
&=\frac{\sigma^2}{SST_x}.  
\end{aligned}  
$$

The first line describes the **average squared estimation error across repeated samples**. The last line calculates that same quantity from the population error variance $\sigma^2$, using [[Random Sampling]] and [[Homoskedasticity]]. Thus, $\hat\beta_1$ has a sampling distribution, and $\operatorname{Var}(\hat\beta_1\mid\mathbf{x})$ measures how spread out that distribution is.

run dofile
```stata
use "CEOSEAL1.dta", clear
reg salary roe
```

and we get
``` stata

      Source |       SS           df       MS      Number of obs   =       209
-------------+----------------------------------   F(1, 207)       =      2.77
       Model |  5166419.04         1  5166419.04   Prob > F        =    0.0978
    Residual |   386566563       207  1867471.32   R-squared       =    0.0132
-------------+----------------------------------   Adj R-squared   =    0.0084
       Total |   391732982       208  1883331.64   Root MSE        =    1366.6

------------------------------------------------------------------------------
      salary | Coefficient  Std. err.      t    P>|t|     [95% conf. interval]
-------------+----------------------------------------------------------------
         roe |   18.50119   11.12325     1.66   0.098    -3.428196    40.43057
       _cons |   963.1913   213.2403     4.52   0.000     542.7902    1383.592
------------------------------------------------------------------------------
```
according to **According to Wooldridge's Introductory econometrics (2016, p. 50)**
![[Screenshot 2026-09-21 at 19.04.09.png]]
we can calculate by stata 
```stata

summarize roe if e(sample)
```
and we get
```stata
    Variable |        Obs        Mean    Std. dev.       Min        Max
-------------+---------------------------------------------------------
         roe |        209    17.18421    8.518509         .5       56.3
```
so: 
$$
\operatorname{se}(\hat\beta_{\mathrm{roe}})
=\frac{\hat\sigma}{\sqrt{SST_{\mathrm{roe}}}}
\approx\frac{1366.55}{122.856}
\approx\boxed{11.12325}.$$

> [!question] Question 2 — Sampling Distribution of the OLS Estimators
> Design a population regression equation. Draw all possible subsamples of a chosen size, estimate a simple linear regression in each subsample, and verify that the mean of the resulting sampling distribution equals the population coefficients.

continue use salary case but believe it is population in dataset.

```stata
use "CEOSEAL1.dta", clear
generate int id = _n
tempfile estimates
tempname results
postfile `results' double b0 b1 using `estimates', replace

forvalues i = 1/208 {
    local first_j = `i' + 1
    forvalues j = `first_j'/209 {
        quietly regress salary roe if id != `i' & id != `j'
        post `results' (_b[_cons]) (_b[roe])
    }
}

postclose `results'
use `estimates', clear
summarize b0
summarize b1
```
got
```stata

    Variable |        Obs        Mean    Std. dev.       Min        Max
-------------+---------------------------------------------------------
          b0 |     21,736    963.1696    11.97231   851.9398   1007.713
          
    Variable |        Obs        Mean    Std. dev.       Min        Max
-------------+---------------------------------------------------------
          b1 |     21,736    18.50266    .6767555    12.6758   22.69944


```

we almost get our SRF equal to PRF in Coeff.


```stata
------------------------------------------------------------------------------
      salary | Coefficient  Std. err.      t    P>|t|     [95% conf. interval]
-------------+----------------------------------------------------------------
         roe |   18.50119   11.12325     1.66   0.098    -3.428196    40.43057
       _cons |   963.1913   213.2403     4.52   0.000     542.7902    1383.592
------------------------------------------------------------------------------
```