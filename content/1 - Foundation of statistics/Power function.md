### Motivation
- When the [[Hypothesis|hypotheses]] are composite, the [[Type I error|Type I]] and [[Type II error|Type II]] error probabilities are no longer constants; they depend on the true value of the parameter. Consequently they are studied through a function of $\theta$
### Definition
The power function of a test $H_{0}:\theta \in \Theta_{0}$ against $H_{1}: \theta \in \Theta_{1}$ is the function of parameter $\theta$ that gives the probability of of rejecting $H_{0}$ *i.e.* 
$$
K(\theta) = P(\text{Reject} \; H_0 \mid \theta)
$$
### Interpretation
- When $\theta$ belongs to the (simple or composite) null hypothesis (*i.e.* $\theta \in H_{0}$), Type I error probability at that particular $\theta$ is $K(\theta)$
- When $\theta$ belongs to the (simple or composite) alternative hypothesis (*i.e.* $\theta \in H_{1}$), Type II error probability at that particular $\theta$ is $1-K(\theta)$