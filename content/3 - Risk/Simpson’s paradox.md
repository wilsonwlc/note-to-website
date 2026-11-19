### Concept
- *What is it:* a statistical phenomenon in which a trend observed within several individual groups disappears or reverses when the groups are combined
- *Why it happens:* It occurs when a [[3 - Risk/Confounding factor|confounding factor]] is associated with both the explanatory variable and the outcome, and the groups being compared contain different proportions of observations from different subgroups. *e.g.* when comparing two medical treatments, patient severity (mild or severe illness) may be a confounding variable. One treatment group may contain mostly mildly ill patients, while the other contains mostly severely ill patients. When the patients are combined, the overall result can be dominated by the subgroup with more observations, potentially reversing the trend observed within each subgroup.
- *Why it is important:* It highlights how analysing aggregated data without considering differences between subgroups can lead to misleading conclusions. *e.g.* when comparing two medical treatments, one treatment may appear more effective overall simply because more patients receiving it have mild illnesses, even though it is less effective within each subgroup (mild and severe cases). Therefore, it is important to examine both the overall results and the results within individual subgroups before drawing conclusions.
- *When it happens:* 
	- [[Observational Study|Observational studies]]
	- **Experimental studies**
- *How to address it:*
	- Identify potential confounding variables
	- Examine the relationship between variables within relevant subgroups
	- Use appropriate statistical methods to control for confounding variables *e.g.* **regression**, **standardisation** 
### Example
#### Example 1
- Consider data from a study examining the relationship between smoking and 20-year survival rates of women (Appleton et al., 1996)
- The data suggest that smoking might be beneficial because 43% of non-smokers died compared to 38% of smoker *i.e.* smoking would result in a decreasing risk of death ![[Simpson's paradox - example - without confounding factor.png|432]]
- *Problem:* The above result does not show a correct interpretation of the data because it ignored an important [[Confounding factor|confounding variable]] that is strongly related to smoking and survival - women's ages at the start of the study
- When survival rates are determined for women in each of the 10-year age ranges (15-54, 55-64, 65-74), the non-smoking group does better in each case ![[Simpson's paradox - example - with confounding factor.png]]