### Concept
- *Why we need it:* 
	- After the overall F-test is significant in [[One-way ANOVA|ANOVA]] comparing $k$ treatment groups, we may want to know 
		- Which treatment groups differ
		- Is one treatment different from the average of the others
		- Is a combination of treatments different from another combination
	- However, making many comparisons increases the probability of a Type I error, so an adjustment is needed
- *What is it:* a multiple-comparison procedure
- *When to use it:* 
	- Clinical trial: after ANOVA *AND* make inferences about all possible **contrasts** (*i.e.* linear combination of treatment means. The sum of its weights is zero) among treatment means *AND* control **family-wise error rate (FWER)**
### Formula
#### Pairwise difference
- Assume there are $k$ treatments, $n$ participants in total, $n_{i}$ participants receiving Treatment $i$, and the treatment effect is $\alpha_{i}-\alpha_{j}$ 
- Point estimate $$\overline{Y}_{i} - \overline{Y}_{j}$$
- Standard error $$\sqrt{MS_{E} \times \left( \frac{1}{n_{i}}+ \frac{1}{n_{j}} \right)}$$
- Critical value $$\sqrt{(k-1) \times F_{\alpha, df = k-1, n-k}}$$
- A simultaneous $100(1-\alpha)\%$ confidence interval $$(\overline{Y}_{i} - \overline{Y}_{j}) \pm \left[ \sqrt{(k-1) \times F_{\alpha, df = k-1, n-k}} \times \sqrt{MS_{E} \times \left( \frac{1}{n_{i}}+ \frac{1}{n_{j}} \right)}   \right]$$
#### Contrasts
- Define $$L = \sum\limits_{i=1}^{k} w_{i}\alpha_{i}$$
	- $k$: number of treatments
	- $\alpha_{i}$ is a treatment mean
	- $\sum\limits_{i=1}^{k} w_{i} = 0$
- Point estimate $$\hat{L}=\sum\limits_{i=1}^{k} w_{i} \overline{Y}_{i}$$
- Standard error $$se(\hat{L}) = \sqrt{MS_{E} \sum\limits_{i=1}^{k} \frac{w_{i}^{2}}{n_{i}}}$$
- A simultaneous $100(1-\alpha)\%$ confidence interval $$\hat{L} \pm \sqrt{MS_{E} \sum\limits_{i=1}^{k} \frac{w_{i}^{2}}{n_{i}}} \times \sqrt{(k-1) \times F_{\alpha, df = k-1, n-k}} $$