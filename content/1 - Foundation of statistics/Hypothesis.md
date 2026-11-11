### Concept
- Aka **statistical hypothesis**
- *What is it:* An assertion or statement about the population, usually formulated in terms of population parameters
- *What it is consisted of:*
	- The **null hypothesis**, $H_{0}$. It is usually a statement about something that has been established, or something that has an authoritative standing, or something worth protecting
	- The **alternative hypothesis**, denoted by $H_{1}$. It is usually a statement about something that challenges the authority, or something that needs not be protected strongly
### Notation
In parametric case 
$$
\begin{align*} H_{0}: \theta \in \Theta_{0} \\ H_{1}: \theta \in \Theta_{1} \end{align*}
$$
- $\Theta_{0}$ and $\Theta_{1}$ are disjoint subsets of the parameter space $\Theta$
- *Caution:* In non-parametric setting, the hypotheses may not be specified in terms of the parameters
### Type
- A hypothesis is **simple** if it completely specifies the distribution of the data *e.g.* $H_{0}: \theta = \theta_{0}$ 
- A hypothesis is **composite** if it does not *e.g.* $H_{0}: \theta \in \Theta_{1}$ 
### Practice
#### Form
- Often, the null hypothesis has the form $H_{0}:\theta=\theta_{0}$ for some hypothetical value $\theta_{0}$
- The alternative hypothesis has one of three forms 
	- $H_{1}:\theta>\theta_{0}$ or $H_{1}:\theta<\theta_{0}$: **one-sided alternatives**
	- $H_{1}:\theta \neq \theta_{0}$: **two-sided alternative**
#### Criteria for choosing $H_{0}$ and $H_{1}$
1. Since we keep [[Type I error|Type I error]] $\alpha = P(\text{Reject } H_0 \mid H_0 \text{ true})$ in a low level, we should choose a statement as $H_{0}$ when falsely rejecting it would have serious consequences
2. When we aim at establishing an assertion with substantive support obtained from the data, the negation of the assertion is taken to be the null hypothesis $H_0$, and the assertion itself is taken to be the alternative hypothesis $H_1$