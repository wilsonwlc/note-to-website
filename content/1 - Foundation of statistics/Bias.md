### Definition
$$
\text{bias}(\hat{\theta}) = \mathrm{E}(\hat{\theta}) - \theta
$$
- $\text{E}(\hat{\theta})$: the [[Expectation|expected value]] of the [[Point estimation|estimator]]
- $\hat{\theta}$ is an estimator of the parameter $\theta$
- It is the **estimator bias**
### Caution
- The expectation is taken with respect to the [[Sampling distribution|sampling distribution]] of $\hat{\theta}$ 
### Interpretation 
- If $\text{bias}(\hat{\theta}) > 0$, $\hat{\theta}$ overestimates $\theta$
- If $\text{bias}(\hat{\theta}) < 0$, $\hat{\theta}$ underestimates $\theta$
- If $\text{bias}(\hat{\theta}) = 0$ for any $\theta$, $\hat{\theta}$ is **unbiased** *i.e.* If $E(\hat{\theta})=\theta$ for all the values of $\theta$ in the parameter space, then the estimator $\hat{\theta}$ is called **unbiased estimator** of the parameter of $\theta$

### Source
#### Selection bias
- *When it happens:* the selection of subjects for a study is affected by variables which are associated with the outcome
- *Example:* If a study on exercise and cardiovascular health recruits volunteers through fitness clubs, then the study sample fails to represent the target population because the the volunteers are likely to be healthier and more health-conscious than the general population.
- *How to avoid it:* clearly defined eligible criteria to ensure that the participants included in a study are representative of the target population
#### Allocation bias
- *When it happens:* non-random or predictable assignment of participants to treatment groups, resulting in baseline differences between groups.
- *Example:* Investigators knowingly assign sicker patients to the experimental treatment
- *How to avoid it:* Randomisation, Double-blind
#### Recall bias
- *When it happens:* participants do not remember previous exposures or events accurately, and the accuracy of recall differs between comparison groups
- *Example:* Questions may be asked more times and more intensively in cases compared to controls. Patients with the disease are more likely to carefully consider whether or not an exposure occurred
- *How to avoid it:* external measures of exposure or disease history. However it is not always feasible
#### Misclassification bias
- *When it happens:* use questionnaire data, estimated data or incomplete information to determine the disease or exposure status of participants
- *How to avoid it:* practical considerations on the classification rule and procedures
##### Non differential
- *What is it:* the classification error is independent of the disease or exposure *i.e.* the error occurs equally across comparison groups
- *Consequence:* usually bias the effect estimate towards the null
##### Differential 
- *What is it:* the classification error is dependent of the disease or exposure *i.e.* the error differs between groups
- *Consequence:* may bias the estimate either towards or away from the null