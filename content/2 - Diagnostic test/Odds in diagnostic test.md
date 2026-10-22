### Formula
#### Pre-test odds
$$\text{pre-test odds} = \frac{\mathrm{Pr}(Present)}{\mathrm{Pr}(Absent)} = \frac{p_{v}}{1-p_{v}}$$
#### Post-test odds
$$\text{Post-test odds} = \text{Pre-test odds} \times \text{Likelihood ratio}$$
##### Positive post-test odds
$$\begin{align*} \text{Positive post-test odds} &= \frac{\mathrm{Pr}(Present|Positive)}{\mathrm{Pr}(Absent|Positive)} \\ &= \frac{\frac{LR^{+} p_{v}}{LR^{+}p_{v}+(1-p_{v})}}{1- \frac{LR^{+} p_{v}}{LR^{+}p_{v}+(1-p_{v})}} \\ &= \frac{p_{v}}{1-p_{v}} LR^{+} \end{align*}$$
- $\mathrm{Pr}(Present|Positive)$ is [[Predicative value#Positive predictive value (PPV)|Positive Predictive Value (PPV)]]
- $LR^{+}$ is the [[Likelihood Ratio|Likelihood Ratio]]
##### Negative post-test odds
$$\begin{align*} \text{Negative post-test odds} &= \frac{\mathrm{Pr}(Present|Negative)}{\mathrm{Pr}(Absent|Negative)} \\ &= \frac{1-\frac{1-p_{v}}{(1-p_{v})+LR^{-}p_{v}}}{\frac{1-p_{v}}{(1-p_{v})+LR^{-}p_{v}}} \\ &= \frac{p_{v}}{1-p_{v}}LR^{-} \end{align*}$$
- $\mathrm{Pr}(Absent|Negative)$ is [[Predicative value#Negative predictive value (NPV)|Negative Predictive Value (NPV)]]
- $LR^{-}$ is the [[Likelihood Ratio|Likelihood Ratio]]
### Interpretation
- Pre-test odds is the **odds** corresponding to the [[Prevalence|prevalence]]
- Positive Predictive Value (PPV) is $$PPV = \frac{\text{Positive post-test odds}}{1+\text{Positive post-test odds}}$$
- Negative Predictive Value (NPV) is $$\text{NPV} = \frac{1}{1 + \text{Negative post-test odds}}$$
### Example
- Give $p_{v}=0.003$ and $LR^{+} = 49.5$,  then
	- $\text{pre-test odds} = \frac{0.003}{1-0.003}=0.003$
	- If a positive test result was observed, $\text{post-test odds}=\text{pre-test odds} \times LR^{+}=0.1489$
	- $PPV=\frac{0.1489}{1+0.1489}=0.1296$