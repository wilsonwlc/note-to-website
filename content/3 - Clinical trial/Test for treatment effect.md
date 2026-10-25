![[Test for period effect#Assumption]]
![[Test for period effect#Model]]

### Hypothesis
- $H_{0}$: $\tau_{A}=\tau_{B}$
- $H_{1}$: $\tau_{A} \neq \tau_{B}$
### Step
![[Test for period effect#Notation]]

#### Point estimate
The period effect can be eliminated by taking the difference between $\overline{D}_{AB}$ and $\overline{D}_{BA}$ *i.e.* 
$$
\overline{D}_{A B}-\overline{D}_{B A}=2(\tau_{A}-\tau_{B})+\overline{\epsilon}_{11}-\overline{\epsilon}_{12}-\overline{\epsilon}_{21}+\overline{\epsilon}_{22}
$$
Denote $\tau_{D} = \tau_{A} - \tau_{B}$
$$
\hat{\tau}_{D} = \frac{1}{2}(\overline{D}_{AB} - \overline{D}_{BA})
$$
##### Expectation
$$
\mathrm{E}(\hat{\tau}_{D})=\tau_{A}-\tau_{B}=\tau_{D}
$$
##### Variance
$$
\begin{align*}\mathrm{Var}(\hat{\tau}_{D}) &= \frac{1}{2} \sigma^{2} \left(\frac{1}{n_{1}}+ \frac{1}{n_{2}}\right) = \frac{1}{4} \sigma^{2}_{D} \left(\frac{1}{n_{1}}+ \frac{1}{n_{2}}\right)  \end{align*}
$$
- $\sigma^{2}_{D}=\mathrm{Var}(D_{ij})=2\sigma^{2}$ 
#### Standard error
$$
\mathrm{se}(\hat{\tau}_{D})=\frac{1}{2}S_{D}\sqrt{\frac{1}{n_{1}}+\frac{1}{n_{2}}}
$$

- The unknown error variance $\sigma_{D}^{2}$ can be estimated based on the pooled sample variances of the differences $$\hat{\sigma}_{D}^{2} = S_{D}^{2}={\frac{(n_{1}-1)S_{AB}^{2}+(n_{2}-1)S_{BA}^{2}}{n_{1}+n_{2}-2}}$$
	- $S_{AB}^{2}=\frac{1}{n_{1}-1}\sum_{j=1}^{n_{1}}(D_{1j}-\overline{{{D}}}_{A B})^{2}$
	- $S_{BA}^{2}=\frac{1}{n_{2}-1}\sum_{j=1}^{n_{2}}(D_{2j}-\overline{{{D}}}_{B A})^{2}$
#### Test statistics
$$
T_{treatment}={\frac{\overline{D}_{AB}-\overline{D}_{BA}}{S_{D}\sqrt{\frac{1}{n_{1}}+ \frac{1}{n_{2}}}}}\stackrel{H_{0}}{\sim}t\left(n_{1}+n_{2}-2\right)
$$
#### Confidence interval
The $100(1-\alpha)\%$ confidence interval for $\tau_{D}=\tau_{A}-\tau_{B}$ is 
$$
\frac{\overline{D}_{A B}-\overline{D}_{B A}}{2}\pm t_{\frac{\alpha}{2},d f=n_{1}+n_{2}-2}\frac{S_{D}}{2}\sqrt{\frac{1}{n_{1}}+ \frac{1}{n_{2}}}
$$