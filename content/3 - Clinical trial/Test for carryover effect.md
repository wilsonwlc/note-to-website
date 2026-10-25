### Model
| Sequence | Period | Model                                                              |
| -------- | ------ | ------------------------------------------------------------------ |
| AB       | 1      | $Y_{1j1}=\mu+\pi_{1}+\tau_{A}+\eta_{1j}+\epsilon_{1j1}$            |
| AB       | 2      | $Y_{1j2}=\mu+\pi_{2}+\tau_{B}+\rho_{A B}+\eta_{1j}+\epsilon_{1j2}$ |
| BA       | 1      | $Y_{2j1}=\mu+\pi_{1}+\tau_{B}+\eta_{2j}+\epsilon_{2j1}$            |
| BA       | 2      | $Y_{2j2}=\mu+\pi_{2}+\tau_{A}+\rho_{B A}+\eta_{2j}+\epsilon_{2j2}$ |
- For sequence AB, $j= 1,...,n_{1}$ 
- For sequence BA, $j= 1,...,n_{2}$
- $N$: total number of patients where $N=n_{1}+n_{2}$
- $\mu$: grand mean
- $\pi_{k}$: period effect of period $k$ $(k = 1,2)$
- $\tau_{l}$: treatment effect of treatment $l$ $(l = A, B)$
- $\eta_{ij}$: effect of patient $j$ in sequence $i$ where $i=1,2$ and $j = 1,2, ..., n_{i}$ and $\eta_{ij} \mathop{\sim}\limits^{iid} N(0,\sigma^{2}_{\eta})$
- $\epsilon_{ijk}$: random error and $\epsilon_{ijk} \mathop{\sim}\limits^{iid} N(0,\sigma^{2})$
- $\{\eta_{ij}\}$ and $\{\epsilon_{ijk}\}$ are mutually independent
- $\rho_{AB}$: the residual effect of treatment A carried to treatment B
- $\rho_{BA}$: the residual effect of treatment B carried to treatment A
### Hypothesis
- $H_{0}$: $\rho_{AB} - \rho_{BA} = 0$
- $H_{1}$: $\rho_{AB} - \rho_{BA} \neq 0$
### Step
#### Notation
- Denote $T_{ij}=Y_{ij1}+Y_{ij2}$ as the sum of the responses over the two periods for patient $j$ in sequence $i$
	- For sequence AB $(i=1,j=1,2,..., n_{1})$, 
	$$
	\begin{aligned} T_{1j} &=Y_{1j1}+Y_{1j2} \\ &=2\mu+\pi_1+\pi_2+\tau_A+\tau_B+\rho_{AB} + 2\eta_{1j} +\epsilon_{1j1} +\epsilon_{1j2} \end{aligned}
	$$
	- For sequence BA $(i=2, j=1,2,..., n_{2})$, 
	$$
	\begin{aligned} T_{2j} &=Y_{2j1}+Y_{2j2} \\ &=2\mu+\pi_1+\pi_2+\tau_A+\tau_B+\rho_{BA} +2\eta_{2j}  +\epsilon_{2j1}  +\epsilon_{2j2}  \end{aligned}
	$$
	- Under $H_{0}$ *i.e.* $\rho_{AB} = \rho_{BA}$, $T_{1j}$ and $T_{2j}$ have the same distribution
	- The variance is 
	$$
	\begin{aligned}  \operatorname{Var}(T_{ij})  &= \operatorname{Var}  \left(  2\eta_{ij}  +\epsilon_{ij1}  +\epsilon_{ij2}  \right) \\  &=4\sigma_\eta^2+2\sigma^2  \end{aligned}
	$$
- Let $\bar{\eta}_{1} = \frac{1}{n_{1}} \sum_{j=1}^{n_{1}} \eta_{1j}$, $\bar{\eta}_{2} = \frac{1}{n_{2}} \sum_{j=1}^{n_{2}} \eta_{2j}$ and $\bar{\epsilon}_{ik} = \frac{1}{n_{i}} \sum_{j=1}^{n_{i}} \epsilon_{ijk}$ for $i=1,2$ and $k=1,2$
- Define the group means by 
$$
\begin{align*} \overline{T}_{AB} &= \frac{1}{n_{1}}\sum\limits_{j=1}^{n_{1}} T_{1j} \\ &= 2\mu + \pi_{1} + \pi_{2} + \tau_{A} + \tau_{B} + \rho_{AB} + 2\bar{\eta}_{1} + \bar{\epsilon}_{11} + \bar{\epsilon}_{12} \\ \overline{T}_{BA} &= \frac{1}{n_{2}}\sum\limits_{j=1}^{n_{2}} T_{2j} \\ &= 2\mu + \pi_{1} + \pi_{2} + \tau_{A} + \tau_{B} + \rho_{BA} + 2\bar{\eta}_{2} + \bar{\epsilon}_{21} + \bar{\epsilon}_{22} \end{align*}
$$
#### Point estimate
Denote 
$$
\rho_{D} = \rho_{AB} - \rho_{BA}
$$
$$
\hat{\rho}_{D} = \overline{T}_{AB} - \overline{T}_{BA}
$$
##### Expectation
$$
\mathrm{E}(\hat{\rho}_{D})=\rho_{AB} - \rho_{BA} = \rho_{D}
$$
##### Variance 
$$
\begin{align*} \mathrm{Var}(\hat{\rho}_{D}) = \left(\frac{1}{n_{1}} + \frac{1}{n_{2}}\right) \sigma_{T}^{2} \end{align*}
$$
- $\sigma_{T}^{2} = \mathrm{Var}(T_{ij}) = 4\sigma_{\eta}^{2}+2\sigma^{2}$
#### Standard error
$$
\mathrm{se}(\hat{\rho}_{D}) = \sqrt{\frac{1}{n_{1}} + \frac{1}{n_{2}}} S_{T}
$$
- The unknown $\sigma_{T}^{2}$ can be estimated by the pooled sample variance $$\hat{\sigma}_{T}^{2} = S^{2}_{T} ={\frac{(n_{1}-1)S_{AB}^{2}+(n_{2}-1)S_{BA}^{2}}{n_{1}+n_{2}-2}}$$
	- $S_{AB}^{2} = \frac{1}{n_{1}-1} \sum\limits_{j=1}^{n_{1}}(T_{1j} - \overline{T}_{AB})^{2}$
	- $S_{BA}^{2} = \frac{1}{n_{2}-1} \sum\limits_{j=1}^{n_{2}}(T_{2j} - \overline{T}_{BA})^{2}$
#### Test statistics
$$
T_{carryover} = \frac{\overline{T}_{AB}-\overline{T}_{BA}}{S_{T} \sqrt{\frac{1}{n_{1}} + \frac{1}{n_{2}}}} \stackrel{H_{0}}{\sim}t\left(n_{1}+n_{2}-2\right)
$$

### Comparison
#### Bias in the treatment effect estimator due to carryover
- Recall $D_{ij}=Y_{ij1}-Y_{ij2}$
- If a carryout effect exists, 
	- For Sequence AB, 
	$$
	\begin{align*} E(D_{1j}) &= E(Y_{1j1}-Y_{1j2}) \\ &= E\left[(\mu+\pi_{1}+\tau_{A}+\eta_{1j}+\epsilon_{1j1})-(\mu+\pi_{2}+\tau_{B}+\rho_{A B}+\eta_{1j}+\epsilon_{1j2})\right] \\ &= (\pi_{1}-\pi_{2})+(\tau_{A}-\tau_{B}) - \rho_{AB} \\ E(\overline{D}_{AB}) &= E\left(\frac{1}{n_{1}} \sum\limits_{j=1}^{n_{1}} D_{1j}\right) \\ &= (\pi_{1}-\pi_{2})+(\tau_{A}-\tau_{B}) - \rho_{AB}\end{align*}
	$$
	- For Sequence BA, 
	$$
	E(\overline{D}_{BA}) = (\pi_{1} - \pi_{2}) + (\tau_{B} - \tau_{A}) - \rho_{BA}
	$$
- Since $\hat{\pi}_{D} = \frac{1}{2}(\overline{D}_{AB} + \overline{D}_{BA})$, 
$$
\begin{align*} E(\hat{\tau}_{D}) &= E \left[ \frac{1}{2}(\overline{D}_{AB} + \overline{D}_{BA}) \right] \\ &= \tau_{A} - \tau_{B} - \frac{1}{2}(\rho_{AB} - \rho_{BA}) \end{align*}
$$

- $\hat{\tau}_{D}$ is unbiased for $\tau_{A}-\tau_{B}$ only if $\rho_{AB} = \rho_{BA}$. Otherwise, it is biased.
- A non-zero difference $\rho_{AB}-\rho_{BA}$ introduces bias into the estimation of the treatment effect, which may lead to misleading inferences