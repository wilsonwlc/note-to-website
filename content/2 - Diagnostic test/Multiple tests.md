### Motivation
- The result of a [[Diagnostic test|diagnosis test]] is not conclusive when the [[Predicative value|predictive value]] is neither very high nor very low. In that case, the tests should be done again so that a more decisive result can be made
### Calculation
- Suppose $n$ independent tests were performed
- Let $X$ be the number of positive test results
- If $X=k$, then $$\begin{align*} \text{post-test odds} &=  \text{pre-test odds} \times (LR^{+})^{k} \times (LR^{-})^{n-k} \\ \mathrm{Pr}(Present|X=k) &= \frac{p_{v}(LR^{+})^{k}(LR^{-})^{n-k}}{(1-p_{v})+p_{v}(LR^{+})^{k}(LR^{-})^{n-k}} \end{align*}$$
### Assumption
- The multiple tests results are statistically independent. 
	- This assumption can be guaranteed by proper design of the test procedure
- The [[Sensitivity|sensitivity]] and [[Specificity|specificity]] remain the same for each of the multiple tests.
	- *Problem:* This assumption may not hold
	- *Reason:* The sensitivity and specificity estimated from the original study population may not apply to patients undergoing repeated testing. A positive result selects patients who are more likely to have the disease, and may also select patients with particular characteristics that influence the probability of obtaining a positive result, such as disease severity, biomarker concentration, or a predisposition to false-positive results. Consequently, repeatedly applying the original likelihood ratios may overestimate the evidence for disease and inflate the posterior probability
	- *Solution:* Use different tests that assess different aspects of the disease and have distinct sources of error. Their combined results may provide more reliable evidence, provided their errors are sufficiently independent and their sensitivity and specificity remain applicable to the patients being tested
### Example
| Test          | Sensitivity | Specificity | $LR^{+}$ | $LR^{-}$ |
| ------------- | ----------- | ----------- | -------- | -------- |
| PSA 4.0 ng/ml | 0.67        | 0.97        | 22.33    | 0.34     |
| Abnormal DRE  | 0.50        | 0.94        | 8.33     | 0.53     |
- Apart from Prostate-specific antigen (PSA) on the blood, physical examination such as the DRE (digital rectal examination) can also be used for the diagnosis of prostate cancer
- The above table the sensitivity and specificity of these two kinds of test on men without symptoms (screening setting)
- As a single test alone, obviously the PSA is better for its higher sensitivity and specificity. 
- Suppose the prevalence of prostate cancer is 3 in 100. 
- Based on a positive PSA test result, we have $$\begin{align*} \text{posttest odds} &= \frac{0.03}{1 - 0.03} \times 22.33 = 0.6906 \\ Pr(Cancer|PSA+) &= \frac{0.6906}{1 + 0.6906} = 0.4085 \end{align*}$$
- This predictive value is not very useful. Hence we may proceed to apply the DRE test. 
- If the DRE also shows positive, then $$\begin{align*} \text{posttest odds} &= 0.6906 \times 8.33 = 5.7527 \\ Pr(Cancer| PSA^+, DRE^+) &= \frac{5.7527}{1 + 5.7527} = 0.8519 \end{align*}$$
- The physician can have more conclusive interpretation on this predictive value.
### Type
- [[Parallel Testing]]
- [[Serial Testing]]