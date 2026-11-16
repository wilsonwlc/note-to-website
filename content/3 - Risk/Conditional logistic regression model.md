### Motivation
- If the subjects are [[Matched case-control study|matched by design]], the analysis must take matching into account. *Reason:* Matching (especially individual matching) creates dependence within matched sets and can introduce selection bias or distort associations involving the matching factors. *Result:* If we included matching factor as covariates in logistic regression models, there would be bias in the OR estimates for the covariates of interest
### Model
$$
\operatorname{logit}\left\{p_{k}(X_{ik})\right\} = \alpha_{k} + \beta_{1} X_{ik1} + \beta_{2} X_{ik2} + \cdots + \beta_{p} x_{ikp}
$$
 - $p_{k}(X_{ik})$: the probability that the $i$-th individual in the $k$-th **matched set** has disease
- $k \in \{1,2,...,K\}$: index of matched set
- $i \in \{0,1,2,..., M \}$: the index of individual in a matched set. $i=0$ represents the case
- $\mathbf{X}_{ik}=(X_{ik1}, X_{ik2},... X_{ikp})^{T}$: the vector of covariates for the $i$-th person in the $k$-th matched set
	- *Caution:* They are NOT the covariates that were matched on. The covariates that were matched on are implicitly included in the model via stratification
### Interpretation
- Each matched set/pair has a different intercept $\alpha_{j}$
- $\alpha_{j}$ summarises the effect of the matching variables on the probability of disease
- $\beta_{p}$ represents the log OR for diseased comparing those exposed to covariate $p$ to those unexposed to covariate $p$
### Estimation
- Maximise the [[Conditional likelihood for conditional logistic regression|conditional likelihood]] to estimate the coefficient $\beta_{p}$ by numerical methods e.g. **Newton–Raphson**
- We cannot estimate the intercept. Hence, the disease probability $p(X_{ik})$ cannot be estimated as well. 
- We can still include interaction terms between matching variables and exposure factors to determine whether the effect of the exposure variable is consistent across different values of the matching variable
- The log odds ratios are independent of the intercepts, so they can be estimated
### Inference
- For individual parameters, both the likelihood ratio test and Wald test are valid
- Can use Hosmer-Lemeshow statistic for Goodness-of-Fit
- Can use likelihood ratio tests to compare nested models and conduct hypothesis tests for parameter estimates
### Example
- [[Example of Conditional logistic regression model|Example of Conditional logistic regression model]]