### Motivation
- *Situation:* Subjects were sampled in [[Matched case-control study|matched sets]]. *Problem:* The ordinary (unconditional) likelihood is invalid because it ignores the dependence induced by matching and the fact that selection probabilities depend on the matching variables
- *Solution:* By conditioning on the observed composition of each matched set, we eliminate the nuisance parameters associated with the matching variables and the set-specific baseline risks.
### Concept
- *What is it:*
	- It is a product of $K$ independent terms, where $K$ is the number of matched sets
	- Each term is a conditional probability, $P(A|B)$. It is the probability that the case in a particular matched set is the one with a particular observed value for the explanatory variables given that the values of all the explanatory variables observed in that particular matched set *i.e.* the probability that the individual with covariates vector is $\mathbf{X}_{0k}$ is  the case, given the observed set of covariate vectors $\{\mathbf{X}_{0k}, ..., \mathbf{X}_{Mk}\}$  in the $k$-th matched set
		- $P(B)$: The probability that one of the $M+1$ subjects in the $k$-th matched set is the case and the remainder are controls *i.e.*
			- Person with $\mathbf{X}_{0k}$ has disease and the rest are disease-free
			- Person with $\mathbf{X}_{1k}$ has disease and the rest are disease-free
			- ...
			- Person with $\mathbf{X}_{Mk}$ has disease and the rest are disease-free
		- $P(A \cap B)$ : the joint probability that $X_{0k}$ corresponds to the case and $X_{ik}$ corresponds to controls
### Construction
- Define 
	-  $k \in \{1,2,...,K\}$: index of matched set
	- $i \in \{0,1,2,..., M \}$: the index of individual in a matched set. $i=0$ represents the case
	- $\mathbf{X}_{ik}$: the vector of covariates for the $i$-th person in the $k$-th matched set
	- $P(\mathbf{X}_{ik}|Y=1)$: the probability that the $i$-th person with disease in the $k$-th matched set has covariate vector $\mathbf{X}_{ik}$
	- $P(\mathbf{X}_{ik}|Y=0)$: the probability that the $i$-th person without disease in the $k$-th matched set has covariate vector $\mathbf{X}_{ik}$
- By definition of conditional probability, 
$$
\begin{align*} P(A|B) &= \frac{P(A \cap B)}{P(B)} \end{align*}
$$
- $P(A \cap B)$ is 
$$
P(\mathbf{X}_{0k} \mid Y = 1) \prod_{i=1}^{M} P\left(\mathbf{X}_{ik} \mid Y = 0\right)
$$
- $P(B)$ is 
$$
\sum_{i=0}^{M} P\left(\mathbf{X}_{ik} \mid Y = 1\right) \prod_{r \neq i} P\left(\mathbf{X}_{rk} \mid Y = 0\right)
$$
- The conditional probability of interest is the ratio 
$$
L_{k} = \frac{P(\mathbf{X}_{0k} \mid Y = 1) \prod_{i=1}^{M} P\left(\mathbf{X}_{ik} \mid Y = 0\right)}{\sum_{i=0}^{M} P\left(\mathbf{X}_{ik} \mid Y = 1\right) \prod_{r \neq i} P\left(\mathbf{X}_{rk} \mid Y = 0\right)}
$$
- It is the conditional likelihood for the $k$-th stratum/matched set
- By Bayes' Theorem, we have 
$$
\begin{align*} P(\mathbf{X}_{ik} \mid Y = 1) &= \frac{P(Y = 1 \mid \mathbf{X}_{ik}) P(\mathbf{X}_{ik})}{P(Y = 1)} \\ P(\mathbf{X}_{ik} \mid Y = 0) &= \frac{P(Y = 0 \mid \mathbf{X}_{ik}) P(\mathbf{X}_{ik})}{P(Y = 0)} \end{align*}
$$
- Hence, 
$$
\begin{align*}
L_{k} &= \frac{\frac{P(Y = 1 \mid \mathbf{X}_{0k}) P(\mathbf{X}_{0k})}{P(Y = 1)} \prod_{i=1}^{M} \frac{P(Y = 0 \mid \mathbf{X}_{ik}) P(\mathbf{X}_{ik})}{P(Y = 0)}}{\sum_{i=0}^{M} \frac{P(Y = 1 \mid \mathbf{X}_{ik}) P(\mathbf{X}_{ik})}{P(Y = 1)} \prod_{r \neq i} \frac{P(Y = 0 \mid \mathbf{X}_{rk}) P(\mathbf{X}_{rk})}{P(Y = 0)}} \\
&= \frac{P(Y = 1 \mid \mathbf{X}_{0k}) \prod_{i=1}^{M} P\left(Y = 0 \mid \mathbf{X}_{ik}\right)}{\sum_{i=0}^{M} P\left(Y = 1 \mid \mathbf{X}_{ik}\right) \prod_{r \neq i} P\left(Y = 0 \mid \mathbf{X}_{rk}\right)}
\end{align*}
$$
- By a logistic model for disease in the $i$-th person in the $k$-th stratum, we have  
$$
\begin{align*}
\operatorname{logit} P(Y_{i} = 1 \mid \mathbf{X}_{ik}) 
&= \alpha_{k} + \sum\limits_{j=1}^{p} \beta_{j}X_{ikj}\\
P(Y = 1 \mid \mathbf{X}_{ik}) &= \frac{e^{\alpha_{k} + \mathbf{X}_{ik}^{T} \boldsymbol{\beta}}}{1 + e^{\alpha_{k} + \mathbf{X}_{ik}^{T} \boldsymbol{\beta}}}\\
P(Y = 0 \mid \mathbf{X}_{ik}) &= \frac{1}{1 + e^{\alpha_{k} + \mathbf{X}_{ik}^{T} \boldsymbol{\beta}}}
\end{align*}
$$
 - The conditional likelihood for the $k$-th stratum/matched set  
 $$
\begin{align*}
L_{k}(\boldsymbol{\beta}) &= \frac{e^{\alpha_{k} + \mathbf{X}_{0k}^{T} \boldsymbol{\beta}}}{\sum_{i=0}^{M} e^{\alpha_{k} + \mathbf{X}_{ik}^{T} \boldsymbol{\beta}}} \\ 
&= \frac{e^{\mathbf{X}_{0k}^{T} \boldsymbol{\beta}}}{\sum_{i=0}^{M} e^{\mathbf{X}_{ik}^{T} \boldsymbol{\beta}}}
\end{align*}
$$
 - Combining likelihoods to obtain likelihood over all strata, we have $$L(\boldsymbol{\beta}) = \prod_{k=1}^{K} L_{k}(\boldsymbol{\beta})$$