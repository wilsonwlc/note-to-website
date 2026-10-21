### Concept
- *What is it:* A Latin square of order $n$ is an $n \times n$  arrangement of n treatments such that
	- Each treatment appears exactly once in every row
	- Each treatment appears exactly once in every column
- *Motivation:* In an $n$-treatment crossover trial, there are $n!$ possible treatment sequences. Using all possible sequences is usually impractical, so Latin square sequences provide a smaller, structured set of treatment sequences
- *Why we need it:* 
	- Ensure that each treatment appears equally often in each period and in each sequence
	- Allow estimation of treatment effects while controlling for two nuisance factors represented by the rows and columns (for example, sequence effects and period effects in crossover trials)
### Assumption
- No treatment × row interaction
- No treatment × column interaction
- Independent errors
- Homoscedastic errors
- Normal errors (for ANOVA inference)
### Cons
- A Latin square of order $n$ requires exactly $n$ treatments, $n$ rows and $n$ columns. Consequently, the design is inflexible when the numbers of treatments and blocking levels differ
### Model

$$Y_{ijk} = \mu + \pi_{i} + \tau_{j} + \rho_{k} + \epsilon_{ijk}$$
- $Y_{ijk}$: response observed in row $i$ and column $k$ receiving treatment $j$
- $\mu$: overall mean response
- $\pi_{i}$: effect row $i$. It represents the first nuisance factor e.g. sequence effect in a crossover trial
- $\rho_{k}$: effect of column $k$. It represents the second nuisance factor *e.g.* period effect in a crossover trial
- $\tau_{j}$: effect of treatment $j$
- $\epsilon_{ijk}$: random error associated with the observation in row $i$, column $k$, and treatment $j$ with $\epsilon_{ijk} \stackrel{iid}{\sim} N(0,\sigma^2)$ 
### Example
#### 4 × 4 Latin squares 
| Sequence | Period 1 | Period 2 | Period 3 | Period 4 |
| -------- | -------- | -------- | -------- | -------- |
| 1        | A        | B        | C        | D        |
| 2        | B        | D        | A        | C        |
| 3        | C        | A        | D        | B        |
| 4        | D        | C        | B        | A        |
 - Each treatment occurs once in every row and once in every column