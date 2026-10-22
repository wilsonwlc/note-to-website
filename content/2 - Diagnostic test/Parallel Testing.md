### Concept
- *Which:* [[Multiple tests|Multiple tests]]
- *What is it:* All the tests are performed at the same time
- *How to determine results:* Overall result is positive if any of the tests shows positive
### When
- Rapid assessment
### Formula
- Suppose we have $k$ different tests
$$\begin{align*} \text{overall sensitivity} &= 1 - \prod_{i=1}^{k} (1-p_{se,i}) \\ \text{overall specificity} &= \prod_{i=1}^{k} p_{sp,i} \end{align*}$$
- $p_{se, i}$: sensitivity of the $i^{th}$ test
- $p_{sp,i}$: specificity of the $i^{th}$ test
### Interpretation
- It will generally increase the [[Sensitivity|sensitivity]] and decrease the [[Specificity|specificity]]