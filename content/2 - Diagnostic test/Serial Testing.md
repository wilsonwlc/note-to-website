### Concept
- *Which:* [[Multiple tests|Multiple tests]]
- *What is it:* The tests are performed sequentially and each test is done only when the previous test result is positive
- *How to determine results:* Overall result is positive if all the tests show positive
### When 
- Rapid assessment is not required
### Formula
- Suppose we have $k$ different tests
$$
\begin{align*} \text{overall sensitivity} &=  \prod_{i=1}^{k} p_{se,i} \\ \text{overall specificity} &= 1 -\prod_{i=1}^{k} (1-p_{sp,i}) \end{align*}
$$
- $p_{se, i}$: sensitivity of the $i^{th}$ test
- $p_{sp,i}$: specificity of the $i^{th}$ test
### Interpretation
- It will generally decrease the [[Sensitivity|sensitivity]] and increase the [[Specificity|specificity]]