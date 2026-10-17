### Data
| Treatment | Response                         | Size     |
| --------- | -------------------------------- | -------- |
| 1         | $Y_{11}, Y_{12},..., Y_{1n_{1}}$ | $n_{1}$  |
| 2         | $Y_{21}, Y_{22},..., Y_{2n_{2}}$ | $n_{2}$  |
| $\vdots$  | $\vdots$                         | $\vdots$ |
| $k$       | $Y_{k1}, Y_{k2},..., Y_{kn_{k}}$ | $n_{k}$  |
- $n = n_{1}+n_{2}+...+n_{k}$
### Hypothesis
- $H_{0}$: All population distributions are identical.
- $H_{1}$: Not all population distributions are identical.
### Assumption
- Dependent variable is ordinal, interval, or ratio
- Independent variable is a factor with two or more levels.  That is, two or more groups 
- Observations between groups are independent.  That is, not paired or repeated measures data
### Testing
1. Pool the observations over all samples, thus constructing a combined sample of size $n=\sum\limits_{i} n_{i}$
2. Assign ranks to the individual observations, using the average rank in the case of tied observations
3. Compute the rank sum $R_{i}$ for each of the $k$ samples
4. Compute the test statistics
	- Case 1: there are no ties $$H = H^{*} = \frac{12}{n(n+1)} \times \sum_{i=1}^{k} \frac{R_{i}^{2}}{n_{i}} - 3(n+1)$$
	- Case 2: there are ties $$H = \frac{H^{*}}{1 - \frac{\sum_{j=1}^{T}(t_{j}^{3} - t_{j})}{n^{3} - n}}$$
		- $t_{j}$: number of observations with the same value in the $j$-th cluster of tied observations
		- $T$: number of tied groups 
5. For a level $\alpha$ test,
	- If $H \leq \chi_{\alpha, df=k-1}^{2}$, fail to reject $H_{0}$
	- If $H>\chi_{\alpha, df=k-1}^{2}$, reject $H_{0}$
6. The p-value is $$p = Pr(\chi_{k-1}^{2} > H)$$
### Practice
- This test procedure should be used only if minimum $n_{i} \geq 5$ *i.e.* if the smallest sample size for an individual group is at least 5. *Reason:* the decision rule is based on the large-sample approximation $$H \overset{\text{approx}}{\sim} \chi_{k-1}^{2}$$ under $H_0$