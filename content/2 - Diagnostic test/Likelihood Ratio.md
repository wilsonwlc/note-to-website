### Concept
- *Why we need it:* describe the performance of a [[Diagnostic test|diagnostic test]] *i.e.* the ability to discriminate between diseased and non-diseased people
### Formula
$$
\begin{align*} LR^{+} &= \frac{\mathrm{Pr}(Positive|Present)}{\mathrm{Pr}(Positive|Absent)} = \frac{p_{se}}{1-p_{sp}} \\ LR^{-} &= \frac{\mathrm{Pr}(Negative|Present)}{\mathrm{Pr}(Negative|Absent)} = \frac{1-p_{se}}{p_{sp}} \end{align*}
$$
### Interpretation
- Large value of $LR^{+}$ and small value of $LR^{-}$ would be desirable for an accurate test
### Example
- Assume the sensitivity and specificity of Prostate-specific antigen (PSA) are 0.95 and 0.78 respectively when the cutoff point of PSA level is set to 5.5 ng/mm. 
- $LR^{+} = \frac{0.95}{1-0.78}=4.32$
- $LR^{-} = \frac{{1-0.95}}{0.78}=0.06$
- It is 4.32 more likely that a positive test result would be found in diseased people compared to non-diseased people.
### Caution
- It is NOT used to make inference on a tested individual. A positive result from a test with large $LR^{+}$ does not mean that the tested individual is highly probable to have the disease