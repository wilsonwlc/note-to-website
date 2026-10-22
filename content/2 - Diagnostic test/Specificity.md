### Concept
- Aka **True negative rate**
### Formula
$$\begin{align*} p_{sp} &= \mathrm{Pr}(\text{Predict as negative} | \text{Actual negative}) \\ &= \frac{\text{True Negative}}{\text{\#Actual Negative}} \\ &= \frac{\text{True Negative}}{\text{True Negative + False Positive}} \\ &= 1-\text{False positive rate} \end{align*}$$
### Interpretation
- High specificity means the classifier has a low rate of false positive *i.e.* it is good at correctly identifying negative instances *e.g.* A specific diagnosis test will rarely misclassify people as having the disease when they do not
### When
- [[Diagnostic test]]: confirm diagnostic that has been suggested by other data