### Motivation
- *Situation:* Some **nuisance factors** are known to affect the response
	- Nuisance factors are factors that influence the response variable but are not the primary focus of the study. *e.g.* sex, age, exposure, disease history
-  *Expected result*: If the variation attributable to nuisance factors can be accounted for, the residual variability is reduced, leading to more precise treatment comparisons
- *Solution*: These nuisance sources of variability can be systematically controlled through a technique called **blocking** 
	- *What blocking does:* group experimental units with similar values of the nuisance factor into homogeneous **blocks**
### Concept
- *What is it:* A randomisation design in which randomisation is restricted within blocks
- *What it does:* 
	1. Experimental units are first grouped into relatively homogeneous blocks according to a nuisance factor.
	2. Treatments are then randomly assigned within each block such that each treatment appears exactly once in every block. Consequently, there is one observation for each treatment-block combination.
### Analysis
#### Parametric method
- [[Two-way ANOVA]]
	- *Action:* The **treatment effect** and **block effect** are assessed under an additive model
	- *Interpretation:* 
		- When an additive model is assumed, if there is a difference between treatments, the magnitude of this effect does not vary from block to block except for random variation
		- Assuming both the treatment effect and block effect are significant, ignoring the blocks and analysing the data as a single-factor experiment may still lead to a significant treatment effect. However, the analysis becomes less efficient because variation due to blocks is absorbed into the residual error, increasing the residual variance and reducing the power of the treatment test
		- If the block effect is not statistically significant, the chosen blocking factor may have contributed little to explaining variability in the response. This may suggest that blocking on that factor is less beneficial in future experiments, although scientific considerations should also be taken into account
		- Because a standard RCBD contains only one observation per treatment-block combination, treatment × block interaction cannot be estimated directly. Tukey's one-degree-of-freedom test may be used to assess a specific form of non-additivity in the model
#### Non-parametric method
- [[Friedman Test]]
### Comparison
#### Randomised Complete Block Design (RCBD) vs Factorial design
- *Similarity:* 
	- Both designs can be analysed using a [[Two-way ANOVA|two-way ANOVA ]] framework.
	- The additive RCBD model has the same mathematical form as a two-way ANOVA model without an interaction term.
- *Difference:* 
	- *Design:* In an RCBD, the treatment factor is the primary factor of interest, whereas the block factor is a nuisance factor introduced to reduce variability. In a factorial design, both factors are treatment factors of scientific interest.
	- *Interaction:* In a standard RCBD, treatment × block interaction is assumed absent (or cannot be estimated directly because there is only one observation per treatment-block combination). A factorial design is typically used to investigate both main effects and interaction effects between factors.
	- *Randomisation:* Randomisation in an RCBD is restricted within blocks whereas . randomisation in a factorial design is generally unrestricted