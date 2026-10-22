### Motivation
- The estimates may be biased. *Reason:* The patients who are selected to establish the test's performance and those to whom the test are applied in clinical practice are different. *e.g.* People who are suspected to have a given disease may have other conditions that more likely to cause a positive test. Including them in the control group would underestimate the [[Specificity|specificity]]
### Concept
- *How it works:* The precision of the probabilities can be measured by the **standard error**. The standard error decreases as the sample size increases
## Assumption
- The test result follows **Binomial distribution**
### Formula
Assume $X \sim \mathrm{Bin}(n,p)$
#### 2-sided approximate CI
$$\hat{p} \pm z_{\frac{\alpha}{2}} \sqrt{\frac{\hat{p}(1-\hat{p})}{n}}$$
- *Reason:* Use **Central Limit Theorem** to approximate the binomial distribution *i.e.* $$\frac{\hat{p}-p}{\sqrt{\frac{p(1-p)}{n}}} \mathop{\longrightarrow}\limits^{d} N(0,1)$$
- *When:* $np$ and $n(1-p)$ are greater than or equal to 5
#### 1-sided exact CI
$$\begin{align*} [0, p_{U}) \hspace{5mm} \text{where } \sum\limits_{j=0}^{X_{obs}} \binom{n}{j} p_{U}^{j} (1-p_{U})^{n-j} &= \alpha \\ (p_{L},1] \hspace{5mm} \text{where } \sum\limits_{j=X_{obs}}^{n} \binom{n}{j} p_{L}^{j} (1-p_{L})^{n-j} &= \alpha \end{align*}$$
- *When:* the sample size is small
### Example
| Test      | Disease - Present | Disease - Absent |
| --------- | ----------------- | ---------------- |
| Positive  | 40                | 0                |
| Negative  | 10                | 30               |
| **Total** | 50                | 30               |
- The point estimate for [[Sensitivity|sensitivity]] is $\hat{p}_{se} = \operatorname{Pr}(\text{Positive} \mid \text{Present}) = \frac{40}{50} = 80\%$
- The point estimate of [[Specificity|specificity]] is $\hat{p}_{sp} = \operatorname{Pr}(\text{Negative} \mid \text{Absent}) = \frac{30}{30} = 100\%$
#### 2-sided approximate CI
- The standard error for sensitivity is $$\sqrt{\frac{\hat{p}_{se}(1-\hat{p}_{se})}{n_{P}}}=\sqrt{\frac{(0.8)(0.2)}{50}}=0.057$$
- The 95% **confidence interval** for sensitivity is $$0.8 \pm 1.96 \times 0.057 = (0.689, 0.911)$$
- The true sensitivity of the test can be as low as 68.9%, though it may be as high as 91.1% with 95% confidence
#### 1-sided CI
- Denote $X$ be the number of true negative
- $X \sim \mathrm{Bin}(n,p_{sp})$, where $n$ is the number of actual negative and $p_{sp}$ is the specificity
- Since $\hat{p}_{sp}=1$, an exact one-sided upper $(1-\alpha)\times 100\%$ C.I. for $p_{sp}$ should be constructed
- $X_{observed} = 30$ 
- The lower limit $p_{L}$ in $(p_{L},1]$ can be calculated from $$\begin{align*} \sum\limits_{j=X_{obs}}^{n} \binom{n}{j} p_{L}^{j} (1-p_{L})^{n-j} &= \alpha \\ \sum\limits_{j=30}^{30} \binom{n}{j} p_{L}^{j} (1-p_{L})^{30-j} &= 0.05 \\ p_{L}^{30} &= 0.05 \\ p_{L} &= 0.905\end{align*}$$
- Therefore a 95% confidence interval for the specificity is (90.5%, 100%]

