### Concept
- Aka **True Positive Rate**
### Formula
$$
\begin{align*} p_{se} &= \mathrm{Pr}(\text{Predict as positive}|\text{Actual positive}) \\ &= \frac{\text{True Positive}}{\text{\#Actual Positive}} \\ &= \frac{\text{True Positive}}{\text{True Positive} + \text{False Negative}} \\ &= 1-\text{False negative rate} \end{align*}
$$
### Interpretation
- High sensitivity means the classifier has a low rate of false negative *i.e.* it is good at correctly identifying positive instances. *e.g.* A sensitive diagnosis test will rarely miss people with the disease
### When
- [[Diagnostic test]]: there is an important penalty for missing a disease