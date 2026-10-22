### Motivation
- Prefer a more [[Specificity|sensitive]] and more [[Specificity|specific]] classification system *e.g.* [[Diagnostic test|diagnostic test]]
- However, there is always a trade-off between sensitivity and specificity
### Concept
- Stand for **Receiver Operating Characteristic**
- *What is it:* A graphical representation that illustrates the diagnostic ability of a binary classification system as its discrimination threshold is varied
- *How to plot it:* This curve plots two parameters 
	- *y-axis*: True Positive Rate (TPR) / [[Sensitivity|Sensitivity]]
	- *x-axis*: False Positive Rate (FPR) / 1-[[Specificity|Specificity]]

### Interpretation
![[ROC curve.png|377]]
- A diagonal line (45-degree line) in the ROC plot represents a random classifier. Points above this line indicate better-than-random performance
- The best cutoff point is at or near the "shoulder" of the ROC curve, at which the sensitivity is substantially increasing with little decreasing of the specificity.