### Definition
The **likelihood function** of a parameter (or vector of parameters) $\theta$ given observed data $\mathbf{x}=(x_{1}, ..., x_{n})$ is defined as 
$$
L(\theta|\mathbf{x})=f_{\mathbf{X}}(\mathbf{x}|\theta)
$$

- $f(\mathbf{x}|\theta)$ is joint [[Probability mass function (pmf)|probability mass function]] (for discrete data) or the [[Probability density function (pdf)|probability density function]] (for continuous data), evaluated at the observed data $\mathbf{x}$ for a given value of the parameter $\theta$
### Notation
- It is also commonly written as 
$$
L(\theta;\mathbf{x})=L(\theta;x_{1},...,x_{n})=f_{\mathbf{X}}(x_{1},...,x_{n};\theta)
$$

### Interpretation
- $f_{\mathbf{X}}(\mathbf{x}|\theta)$ is regarded as a function of $\theta$, with the observed data $\mathbf{x}$ held fixed
- The likelihood tells us how well different values of $\theta$ fit the observed data $\mathbf{x}$. A higher likelihood means that, under that value of $\theta$, the observed data are more likely to be observed.
### Caution
- $L(\theta\mid\mathbf{x})$ is NOT the probability that $\theta$ is the true parameter *i.e.* $L(\theta\mid\mathbf{x}) \neq P(\theta\mid\mathbf{x})$
- The likelihood function does not integrate or sum to 1 over $\theta$ (unlike a probability density)
- The likelihood function is non-negative. Its values can be greater than 1 when the data is continuous because a probability density can exceed 1 *e.g.* the uniform distribution $U(0,0.5)$
### Property
- Assume $\mathbf{x}=(x_{1}, ..., x_{n})$ is iid observations from a distribution parameterised by $\theta$
- If $X$ is discrete with $p_X(t|\theta)$, then 
$$
L(\mathbf{x} \mid \theta) = \prod_{i=1}^{n} p_{X}(x_{i} \mid \theta)
$$
- If $X$ is continuous with $f_X(t|\theta)$, then 
$$
L(\mathbf{x} \mid \theta) = \prod_{i=1}^{n} f_{X}(x_{i} \mid \theta)
$$
### Practice
- Constants that don't depend on $\theta$ can be ignored, so we frequently use proportional likelihood $$L(\theta \mid x) \propto f(x \mid \theta)$$*Reason:* Multiplying the likelihood by a positive constant independent of $\theta$ does not change the information it provides for comparing parameter values






