### Assumption
- No carryover effect *i.e.* The wash-out period is sufficiently long for the effect of the first treatment to wash out. ^6e2141
### Model
| Sequence | Period | Model                                                            |
| -------- | ------ | ---------------------------------------------------------------- |
| AB       | 1      | $Y_{1j1}= \mu + \pi_{1} + \tau_{A} + \eta_{1j} + \epsilon_{1j1}$ |
| AB       | 2      | $Y_{1j2}= \mu + \pi_{2} + \tau_{B} + \eta_{1j} + \epsilon_{1j2}$ |
| BA       | 1      | $Y_{2j1}= \mu + \pi_{1} + \tau_{B} + \eta_{2j} + \epsilon_{2j1}$ |
| BA       | 2      | $Y_{2j2}= \mu + \pi_{2} + \tau_{A} + \eta_{2j} + \epsilon_{2j2}$ |
- For sequence AB, $j= 1,...,n_{1}$ 
- For sequence BA, $j= 1,...,n_{2}$
- $N$: total number of patients where $N=n_{1}+n_{2}$
- $\mu$: grand mean
- $\pi_{k}$: period effect of period $k$ $(k = 1,2)$
- $\tau_{l}$: treatment effect of treatment $l$ $(l = A, B)$
- $\eta_{ij}$: effect of patient $j$ in sequence $i$, where $i=1,2$ and $j=1,\ldots,n_i$ and  $\eta_{ij} \stackrel{iid}{\sim} N(0,\sigma_\eta^2)$
- $\epsilon_{ijk}$: random error for patient $j$ in sequence $i$ during period $k$, where  $i=1,2$, $j=1,\ldots,n_i$, $k=1,2$, and  $\epsilon_{ijk} \stackrel{iid}{\sim} N(0,\sigma^2)$
- $\{\eta_{ij}\}$ and $\{\epsilon_{ijk}\}$ are mutually independent
### Hypothesis
- $H_{0}$: $\pi_{1}=\pi_{2}$
- $H_{1}$: $\pi_{1} \neq \pi_{2}$
### Step
#### Notation
- Denote $D_{ij}=Y_{ij1}-Y_{ij2}$ as the difference in responses after the two periods for the patient $j$ in sequence $i$ $$D_{ij} = \left\{ \begin{array}{ll} \pi_{1} - \pi_{2} + \tau_{A} - \tau_{B} + \epsilon_{1j1} - \epsilon_{1j2} & \text{for Sequence AB} \\ \pi_{1} - \pi_{2} + \tau_{B} - \tau_{A} + \epsilon_{2j1} - \epsilon_{2j2} & \text{for Sequence BA}  \end{array} \right. $$
	- $\mathrm{Var}(D_{ij})=2\sigma^{2}$ 
- The group means are $$\begin{align*} \overline{D}_{AB} &= \frac{1}{n_{1}} \sum\limits_{j=1}^{n_{1}} D_{1j} = \pi_{1} - \pi_{2} + \tau_{A} - \tau_{B} + \overline{\epsilon}_{11} - \overline{\epsilon}_{12} \\ \overline{D}_{BA} &= \frac{1}{n_{2}} \sum\limits_{j=1}^{n_{2}} D_{2j} = \pi_{1} - \pi_{2} + \tau_{B} - \tau_{A} + \overline{\epsilon}_{21} - \overline{\epsilon}_{22} \\ \end{align*}$$
	- $\overline{\epsilon}_{11} = \frac{1}{n_{1}} \sum\limits_{j=1}^{n_{1}} \epsilon_{1j1}$ and  $\overline{\epsilon}_{12} = \frac{1}{n_{1}} \sum\limits_{j=1}^{n_{1}} \epsilon_{1j2}$
	- $\overline{\epsilon}_{21} = \frac{1}{n_{2}} \sum\limits_{j=1}^{n_{2}} \epsilon_{2j1}$ and  $\overline{\epsilon}_{22} = \frac{1}{n_{2}} \sum\limits_{j=1}^{n_{2}} \epsilon_{2j2}$
#### Point estimate
The treatment effect can be cancelled out by adding $\overline{D}_{AB}$ and $\overline{D}_{BA}$ *i.e.* $$\overline{D}_{AB} + \overline{D}_{BA} = 2(\pi_{1} - \pi_{2}) + \overline{\epsilon}_{11} - \overline{\epsilon}_{12} + \overline{\epsilon}_{21} - \overline{\epsilon}_{22}$$
Denote $\pi_{D} = \pi_{1} - \pi_{2}$ 
$$\hat{\pi}_{D} = \frac{1}{2}(\overline{D}_{AB} + \overline{D}_{BA})$$
##### Expectation
$$\begin{align*} \mathrm{E}(\hat{\pi}_{D}) &= \pi_{1} - \pi_{2} = \tau_{D} \end{align*}$$
##### Variance
$$\begin{align*}\mathrm{Var}(\hat{\pi}_{D}) &= \frac{1}{2} \sigma^{2} \left(\frac{1}{n_{1}}+ \frac{1}{n_{2}}\right) = \frac{1}{4} \sigma^{2}_{D} \left(\frac{1}{n_{1}}+ \frac{1}{n_{2}}\right)  \end{align*}$$
- $\sigma^{2}_{D}=\mathrm{Var}(D_{ij})=2\sigma^{2}$ 
#### Standard error
$$\mathrm{se}(\hat{\pi}_{D})=\frac{1}{2}S_{D}\sqrt{\frac{1}{n_{1}}+\frac{1}{n_{2}}}$$

- Since $\sigma_{D}^{2}$ is unknown, it is usually estimated based on the pooled sample variances of the two sequence groups $$\hat{\sigma}_{D}^{2} = S_{D}^{2}={\frac{(n_{1}-1)S_{AB}^{2}+(n_{2}-1)S_{BA}^{2}}{n_{1}+n_{2}-2}}$$
	- $S_{AB}^{2}=\frac{1}{n_{1}-1}\sum_{j=1}^{n_{1}}(D_{1j}-\overline{D}_{A B})^{2}$
	- $S_{BA}^{2}=\frac{1}{n_{2}-1}\sum_{j=1}^{n_{2}}(D_{2j}-\overline{D}_{B A})^{2}$
#### Test statistics
$$T_{period}=\frac{\hat{\pi}_{D}}{\mathrm{se}(\hat{\pi}_{D})}=\frac{\overline{D}_{A B}+\overline{D}_{B A}}{S_{D}\sqrt{{\frac{1}{n_{1}}}+{\frac{1}{n_{2}}}}}\stackrel{H_{0}}{\sim}t(n_{1}+n_{2}-2)$$

#### Confidence interval 
- The $100(1-\alpha)\%$ confidence interval for $\pi_{D}=\pi_{1}-\pi_{2}$ is 
$$\frac{\overline{D}_{A B}+\overline{D}_{B A}}{2}\pm t_{\frac{\alpha}{2},d f=n_{1}+n_{2}-2}\frac{S_{D}}{2}\sqrt{\frac{1}{n_{1}}+\frac{1}{n_{2}}}$$