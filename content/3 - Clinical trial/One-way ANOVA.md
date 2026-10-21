### Data
| Treatment | Response                         | Size     | Mean               | Standard deviation |
| --------- | -------------------------------- | -------- | ------------------ | ------------------ |
| 1         | $Y_{11}, Y_{12},..., Y_{1n_{1}}$ | $n_{1}$  | $\overline{Y}_{1}$ | $S_{1}$            |
| 2         | $Y_{21}, Y_{22},..., Y_{2n_{2}}$ | $n_{2}$  | $\overline{Y}_{2}$ | $S_{2}$            |
| $\vdots$  | $\vdots$                         | $\vdots$ | $\vdots$           | $\vdots$           |
| $k$       | $Y_{k1}, Y_{k2},..., Y_{kn_{k}}$ | $n_{k}$  | $\overline{Y}_{k}$ | $S_{k}$            |
- Group mean: $\overline{Y}_{i} = \frac{1}{n_{i}} \sum\limits_{j=1}^{n_{i}} Y_{ij}$
- Group variance: $S_{i}^{2}=\frac{1}{n_{i}-1}\sum\limits_{j=1}^{n_{i}} (Y_{ij}-\overline{Y}_{i})^{2}$ for $i=1,2,...,k$
- $n = n_{1}+n_{2}+...+n_{k}$

### Model
$$Y_{ij} = \mu + \alpha_{i}+\varepsilon_{ij}$$
- $i=1,2,...,k$ and $j=1,2,..., n_{k}$
- $\sum\limits_{i=1}^{k} \alpha_{i}=0$
- $\varepsilon_{ij} \mathop{\sim}\limits^{iid} N(0,\sigma^{2})$

### Hypothesis
- $H_{0}: \alpha_{1}=\alpha_{2}=...=\alpha_{k}=0$
- $H_{1}: H_{0} \text{ is not ture}$
### Estimation
- Overall sample mean   
$$
\begin{align*} \overline{Y} = \frac{1}{n} \sum\limits_{i=1}^{k} n_{i}\overline{Y}_{i} \end{align*}
$$
- Regression Sum of Squares (SSR) / Between-group sum of squares 
$$
\begin{align*} 
SS_{A} &= \sum\limits_{i=1}^{k} n_{i} \overline{Y}^{2}_{i} - n \overline{Y}^{2} \end{align*} 
$$
- Error sum of square / Within-group sum of squares 
$$
\begin{align*} SS_{E} &= \sum\limits_{i=1}^{k} (n_{i}-1)S_{i}^{2} \end{align*}
$$
- Total Sum of Squares (SST)
$$
\begin{align*} 
SS_{T} &= SS_{A} + SS_{E} \end{align*}
$$
### Testing
#### ANOVA table
| Source    | SS       | d.f.  | MS                            | F-ratio                 |
| --------- | -------- | ----- | ----------------------------- | ----------------------- |
| Treatment | $SS_{A}$ | $k-1$ | $MS_{A}=\frac{SS_{A}}{k-1}$   | $\frac{MS_{A}}{MS_{E}}$ |
| Error     | $SS_{E}$ | $n-k$ | $MS_{E} = \frac{SS_{E}}{n-k}$ |                         |
| Total     | $SS_{T}$ | $n-1$ |                               |                         |
- $MS_{E}$ is the pooled sample variance
#### Step
1. Compile the ANOVA table 
2. Calculate test statistics $F=\frac{MS_{A}}{MS_{E}}$
3. Under $H_{0}$, $F \sim F_{k-1, n-k}$ 
4. Reject $H_{0}$ at significance level $\alpha$ if $F > F_{\alpha, df = k-1, n-k}$ 
### Model diagnostics
- Normality of errors
- Constant variance (homoscedasticity)
- Independence of errors
- *Solution:* transformations or nonparametric approaches
### Interpretation
#### Model
- The variation of each response about the grand mean $\mu$ is due to two components:
	- the $i$-th treatment effect $\alpha_{i}$ *i.e.* between group variation
	- the $(i,j)$-th random error $\epsilon_{ij}$ *i.e.* within group variation
#### Estimation
- $SS_{A}$ measures the variation within the data that is due to differences among the treatments
- $SS_{E}$ measures variation within the data that is due to error
- $SS_{T}$ measures the total amount of variation within the data set
#### Testing
- If $k$ treatment effects are not all the same (*i.e.* $H_{0}$ is false), then $k$ sample means $\overline{Y}_{i}$'s probably vary considerably around $\overline{Y}$. 
- That means
	- $MS_{A}$ tends to be large 
	- $MS_{E}$ has no tendency to be large. *Reason:* It is the sum of squared deviations within each treatment group and hence does not affected by the magnitude of treatment effects
- We can reject $H_{0}$ if $MS_{A}$ is too large compared to $MS_{E}$ (*i.e.* $F$ is too large)