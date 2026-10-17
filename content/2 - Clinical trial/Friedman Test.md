### Concept
- *What is it:* A non-parametric statistical test used to compare three or more treatments in a [[Randomised complete block design (RCBD)|randomised complete block design (RCBD)]] or repeated-measures design
### Hypothesis
- $H_0$: The treatment distributions are identical
- $H_{1}$: At least one treatment distribution differs
### Assumption
- Data are collected using a randomised complete block design (or repeated-measures design) in which each block receives all treatment conditions
- The response variable is measured on an ordinal, interval, or ratio scale
- The treatment factor has at least two levels, although the Friedman test is primarily used when there are three or more treatment levels
- There are two or more blocks, and each block is observed under every treatment condition
- Blocks are mutually independent
### Testing
1. Remove any blocks for which all $a$ responses are identical
2. Within each remaining block, rank the $a$ responses from smallest to largest, assigning average ranks in the presence of ties 
3. Compute the mean rank for each treatment, $\overline{R}_{1}, \overline{R}_{2}, ..., \overline{R}_{a}$
4. Calculate $$Q = \frac{12b}{a(a+1)} \sum\limits_{i=1}^{a} \left(\overline{R}_{i} - \frac{a+1}{2}\right)^{2} $$
	- $b$ is the number of blocks in which at least two values are unequal *i.e.* those not removed in Step 1
5. For a sufficiently large number of blocks, $Q$ is approximately distributed as a chi-square random variable with $a-1$ degrees of freedom. Reject $H_0$ at significance level $\alpha$ if $Q>\chi^{2}_{\alpha, df=a-1}$
### Rule of thumb
- When the number of block ($b$) is greater than 15 or number of treatment ($a$) is greater than 4, the chi-square approximation is adequate