### Data
|              | **Factor B**                          |                                       |          |
| ------------ | ------------------------------------- | ------------------------------------- | -------- |
| **Factor A** | Level 1                               | Level 2                               | $\dots$  |
| Level 1      | $y_{111}, y_{112}, ..., y_{11n_{11}}$ | $y_{121}, y_{122}, ..., y_{12n_{12}}$ | $\dots$  |
| Level 2      | $y_{211}, y_{212}, ..., y_{21n_{21}}$ | $y_{221}, y_{222}, ..., y_{22n_{22}}$ | $\dots$  |
|              | $\vdots$                              | $\vdots$                              | $\ddots$ |
- Each table entry represents a treatment combination
- $i$ indexes the levels of Factor A 
- $j$ indexes the levels of Factor B
- $k$ indexes the observations within the $(i,j)$-th treatment combination
- $n_{ij}$ is the group size in the $(i,j)$-th treatment combination
- Total size: $n=\sum\limits_{i}\sum\limits_{j} n_{ij}$
- $y_{ijk}$ denotes the response from the $k$-th experimental unit in the $(i,j)$-th treatment combination

### Model
$$y_{ijk} = \mu + \alpha_{i} + \beta_{j} + \gamma_{ij} + \varepsilon_{ijk}$$
- $i=1,2,..., I$
- $j= 1,2,..., J$
- $k=1,2,..., n_{ij}$
- $y_{ijk}$: $k$-th response in the $(i, j)$-th treatment group
- $\alpha_{i}$ represents main effect of the $i$-th level of Factor A
- $\beta_{j}$ represents main effect of the $j$-th level of Factor B
- $\gamma_{ij}$ represents interaction effect of the $(i, j)$-th treatment combination
- $\sum\limits_{i=1}^{I} \alpha_{i} = \sum\limits_{j=1}^{J} \beta_{j} = 0$
- $\sum_{i=1}^{I} \gamma_{ij} = 0 \quad \forall j$
- $\sum_{j=1}^{J} \gamma_{ij} = 0 \quad \forall i$
- $\varepsilon_{ijk}$ represents the random error associated with the $k$-th observation in the $(i,j)$-th treatment combination
- $\varepsilon_{ijk} \mathop{\sim}\limits^{iid} N(0,\sigma^{2})$

### Hypothesis
- Factor A main effects 
	- $H_{0}$: $\alpha_{1} = \alpha_{2} = \cdots = \alpha_{I} = 0$
	- $H_{1}$: at least one $\alpha_{i} \ne 0$
- Factor B main effects 
	- $H_{0}$: $\beta_{1} = \beta_{2} = \cdots = \beta_{J} = 0$
	- $H_{1}$: at least one $\beta_{j} \neq 0$
- Interaction effects $A \times B$ 
	- $H_{0}$: $\gamma_{ij} = 0 \; \forall i,j$
	- $H_{1}$: $\gamma_{ij} \neq 0$ for at least one  $(i, j)$
### Estimation
#### Balanced design 
- Group mean for the $(i, j)$-th treatment combination $$\overline{y}_{ij} = \frac{1}{n_{ij}} \sum\limits_{k=1}^{n_{ij}} y_{ijk}$$
- Group variance for the $(i, j)$-th treatment combination $$s_{ij}^{2} = \frac{1}{n_{ij}-1}\sum\limits_{k=1}^{n_{ij}} (y_{ijk}-\overline{y}_{ij})^{2}$$
- Factor A group means $$\overline{y}_{i+} = \frac{1}{n_{i+}} \sum\limits_{j} n_{ij} \overline{y}_{ij}$$
	- $n_{i+}=n_{i1}+n_{i2}+...+n_{iJ}$
- Factor B group means $$\overline{y}_{+j} = \frac{1}{n_{+j}} \sum\limits_{i} n_{ij} \overline{y}_{ij}$$
	- $n_{+j} = n_{1j}+...+n_{Ij}$
- Overall sample mean $$\overline{y} = \frac{1}{n}\sum\limits_{i} \sum\limits_{j} n_{ij} \overline{y}_{ij} = \frac{1}{n} \sum\limits_{i} n_{i+} \overline{y}_{i+} = \frac{1}{n} \sum\limits_{j} n_{+j} \overline{y}_{+j} $$
- Factor A sum of square $$SS_{A} = \sum\limits_{i} n_{i+} \overline{y}_{i+}^{2} - n \overline{y}^2$$
- Factor B sum of squares $$SS_{B} = \sum\limits_{j} n_{+j} \overline{y}_{+j}^{2} - n \overline{y}^{2}$$
- Error sum of squares $$SS_{E} = \sum\limits_{i} \sum\limits_{j} (n_{ij}-1) s_{ij}^{2}$$
- Interaction sum of squares $$SS_{AB} = \sum\limits_{i} \sum\limits_{j} n_{ij}\overline{y}_{ij}^{2} - \sum\limits_{i} n_{i+} \overline{y}_{i+}^{2} - \sum\limits_{j} n_{+j} \overline{y}_{+j}^{2} + n\overline{y}^{2} $$
- Total sum of squares $$SS_{T} = SS_{A} + SS_{B} + SS_{AB} + SS_{E}$$
##### ANOVA table
| Source      | SS        | d.f.         | MS                                     | F-ratio                  | Critical value                   |
| ----------- | --------- | ------------ | -------------------------------------- | ------------------------ | -------------------------------- |
| Factor A    | $SS_{A}$  | $I-1$        | $MS_{A} = \frac{SS_{A}}{I-1}$          | $\frac{MS_{A}}{MS_{E}}$  | $F_{1-\alpha, I-1, n-IJ}$        |
| Factor B    | $SS_{B}$  | $J-1$        | $MS_{B} = \frac{SS_{B}}{J-1}$          | $\frac{MS_{B}}{MS_{E}}$  | $F_{1-\alpha, J-1, n-IJ}$        |
| Interaction | $SS_{AB}$ | $(I-1)(J-1)$ | $MS_{AB} = \frac{SS_{AB}}{(I-1)(J-1)}$ | $\frac{MS_{AB}}{MS_{E}}$ | $F_{1-\alpha, (I-1)(J-1), n-IJ}$ |
| Error       | $SS_{E}$  | $n-IJ$       | $MS_{E} = \frac{SS_{E}}{{n-IJ}}$       |                          |                                  |
| Total       | $SS_{T}$  | $n-1$        |                                        |                          |                                  |

### Test
1. Test the interaction effect $A \times B$
2. If the interaction is not significant,
	- Examine the main effects of Factors A and B. If a main effect is significant, at least one marginal mean of that factor differs from another marginal mean.
	- *Follow-up actions:*
		1. Perform multiple comparison *e.g.* [[Scheffé method|Scheffé method]]
		2. Check ANOVA assumptions
3. If the interaction is significant, 
	- *Interpretation:* The effect of one factor depends on the level of the other factor. The main effects are averages across the levels of the other factor and may therefore mask important differences among treatment combinations
	- *Action 1:* Perform simple effect analysis
		- *What it is:* A simple effect is the effect of one factor at a specific level of the other factor
		- *What it does:*  
			- Compare levels of A within each level of B
			- Compare levels of B within each level of A
		- *How to do it:*
			- Fit separate one-way ANOVAs within each level of the other factor
			- Contrast tests within the two-way ANOVA model
		- If a simple effect is significant and the factor has more than two levels, perform post-hoc multiple comparisons within that simple effect.
	- *Action 2:* Produce an interaction plot to visualise how the effect of one factor changes across levels of the other factor