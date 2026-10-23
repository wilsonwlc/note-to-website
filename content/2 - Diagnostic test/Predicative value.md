### Concept
- *What is it:* The probability of having the disease, given the result of a test
- *Pre-requisite:* [[Prevalence|Prevalence]]
### Formula
#### Positive predictive value (PPV)
$$\begin{align*} PPV &= \mathrm{Pr}(Present|Positive) \\ &= \frac{\mathrm{Pr}(+|Present)\mathrm{Pr}(Present)}{\mathrm{Pr}(+|Present)\mathrm{Pr}(Present) + \mathrm{Pr}(+|Absent)\mathrm{Pr}(Absent)} \\&= \frac{p_{se}p_{v}}{p_{se}p_{v}+(1-p_{sp})(1-p_{v})} \\ &= \frac{LR^{+} p_{v}}{LR^{+}p_{v}+(1-p_{v})} \end{align*}$$
- $p_{se}$ and $p_{sp}$ are [[Sensitivity|sensitivity]] and [[Specificity|specificity]] respectively
- $LR^{+}$ and $LR^{-}$ are [[Likelihood Ratio|Likelihood Ratio]]
- $p_{v}$: [[Prevalence|Prevalence]]
- *Reason:* [[Bayes' Theorem|Bayes rules]]
#### Negative predictive value (NPV)
$$\begin{align*} NPV &= \mathrm{Pr}(Absent|Negative) \\ &= \frac{\mathrm{Pr}(-|Absent) \mathrm{Pr}(Absent)}{\mathrm{Pr}(-|Absent)\mathrm{Pr}(Absent) + \mathrm{Pr}(-|Present) \mathrm{Pr}(Present)} \\ &= \frac{p_{sp}(1-p_{v})}{p_{sp}(1-p_{v})+(1-p_{se})p_{v}} \\ &= \frac{1-p_{v}}{(1-p_{v})+LR^{-}p_{v}} \end{align*}$$
- $p_{se}$ and $p_{sp}$ are [[Sensitivity|sensitivity]] and [[Specificity|specificity]] respectively
- $LR^{+}$ and $LR^{-}$ are [[Likelihood Ratio|Likelihood Ratio]]
- $p_{v}$: [[Prevalence|Prevalence]]
- *Reason:* [[Bayes' Theorem|Bayes rules]]
### Example
- Assume a test is used on a random person
- If the prevalence representing the proportion of a disease in the general population is 0.3%, the false negative rate of the test is 1%, the false positive rate is 2%, then
	- $p_{v}=0.003$
	- $p_{se}=1-0.01=0.99$
	- $p_{sp}=1-0.02=0.98$
	- $LR^{+} = \frac{p_{se}}{1 - p_{sp}} = \frac{0.99}{1 - 0.98} = 49.5$
	- $LR^{-} = \frac{1 - p_{se}}{p_{sp}} = \frac{1 - 0.99}{0.98} = 0.0102$
	- $PPV = \frac{LR^{+} p_{\nu}}{LR^{+} p_{\nu} + (1 - p_{\nu})} = 0.1296$
	- $NPV = \frac{1 - p_{\nu}}{(1 - p_{\nu}) + LR^{-} p_{\nu}} = 0.99997$

- An individual being tested positive will have only about 13% chance to be infected by the virus. 
- An individual being tested negative can feel safe as the chance of being infected is just 0.00003. 
- In this example the prevalence is too small that a negative result is much more reliable than a positive result
### Caution
- In general, the prevalence of disease is more important than **sensitivity** and **specificity** in determining **predicted value**. Using an inaccurate **prevalence** will result in very misleading clinical judgments
- *Practice:* In clinical practice, diagnostic tests are often performed on patients who have particular symptoms or clinical conditions associated with the virus. *Problem:* The prevalence of the virus in this patient group may therefore be higher than in the general population. Using the general population prevalence to calculate the positive predictive value for these patients would generally underestimate the PPV, provided that the test's sensitivity and specificity remain unchanged.
- *Solution:* 
	- Increase the accuracy of prevalence estimates: a difficult task
	- Perform **multiple tests** to reduce the domination of prevalence. More data can then be observed to dominate the prior information