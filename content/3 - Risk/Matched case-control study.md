### Concept
- *Which:* a special case of [[Case-Control study|case-control study]]
- *Why we need it:* control for [[Confounding factor|confounding]] and bias to increase precision
- *What is matching:* pairing or grouping subjects based on pre-specified characteristics. It is a form of stratification
- *When it takes place:* implemented in the design stage
- *What is matched case-control study:* each person with disease who is included in the study as a case is matched with one or more disease free people (the controls). 
	- Design with $M$ controls per case is known as $1:M$ matched study
	- The case and each of the $M$ controls matched to that case are called the **matched set**
	- The characteristics used to pair or group cases and controls are called **matching factors** or **matching variables**
- *What covariates matched based on:* age, ethnicity, residential area
- *How to analyse its data:* [[Conditional logistic regression model|Conditional logistic regression model]]
### Practice
- *How many covariates are used for matching:* between 1 and 5
- We don't have to have the same number of control for all cases 
- In each matched set, we can have more than 1 case
### Interpretation
- All individuals in a matched set will have the same values for the **matching variables**
- The probability that an individuals are included in the study is a function of his or her matching variables
- Conditional on the matching variables, the probability of being selected into the study does not depend on the exposure of interest