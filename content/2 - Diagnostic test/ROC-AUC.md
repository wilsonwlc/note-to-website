### Concept
- *What is it:* The area under an [[ROC|ROC curve]] 
- *Why we need it:* measure of the overall accuracy of a classifier *e.g.* [[Diagnostic test|diagnostic test]]
### Estimate
- A non-parametric method based on constructing trapezoids under the curve *i.e.* **Trapezoidal rule**
- A parametric method using a maximum likelihood estimator to fit a smooth curve to the data points
### Notation
- $W$: the area under the observed ROC curve
### Property
- **Standard error**: $$\mathrm{se}(W)=\sqrt{\frac{W(1-W)+(n_{P}-1)(Q_{1}-W^{2})+(n_{A}-1)(Q_{2}-W^{2})}{n_{P} \; n_{A}}}$$
	- $n_{p}$: the number of diseased cases involved in the estimation
	- $n_{A}$: the number of non-diseased cases (control)
	- $Q_{1}=\frac{W}{2-W}$
	- $Q_{2}=\frac{2W^{2}}{1+W}$
### Interpretation
- AUC ranges in value from 0 to 1. A classifier whose predictions are 100% wrong has an AUC of 0. The one whose predictions are 100% correct has an AUC of 1
- Larger AUC, better the classifier or test
### Rule of thumb
- AUC values of 0.50–0.70 may indicate low discriminatory ability, values of 0.70–0.90 moderate discriminatory ability, and values above 0.90 high discriminatory ability. These thresholds are approximate and should be interpreted in the context of the study, confidence intervals, and clinical or practical relevance