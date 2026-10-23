### Definition
By Kolmogorov's Axioms, ![[Kolmogorov's Axioms#Axioms]]
### Property
- $P(\phi) = 0$
- $P(A^{c}) =1-P(A)$
- If $A \subset B$, then $P(A) \leq P(B)$
- $P(A) \leq 1$ for any event $A$
- **Inclusion-Exclusion Formula** $$\begin{align*} & P \left( E_{1} \cup E_{2} \cup \cdots \cup E_{n} \right) \\ &= \sum_{i=1}^{n} P \left( E_{i} \right) - \sum_{i_{1} < i_{2}} P \left( E_{i_{1}} \cap E_{i_{2}} \right) + \cdots \newline &\quad + (-1)^{r+1} \sum_{i_{1} < i_{2} < \cdots < i_{r}} P \left( E_{i_{1}} \cap E_{i_{2}} \cap \cdots \cap E_{i_{r}} \right) + \cdots \newline &\quad + (-1)^{n+1} \sum_{i_{1} < i_{2} < \cdots < i_{n}} P \left( E_{i_{1}} \cap E_{i_{2}} \cap \cdots \cap E_{i_{n}} \right) \end{align*}$$
- **Boole's Inequality** $$P \left( \bigcup_{i=1}^{\infty} E_{i} \right) \leq \sum_{i=1}^{\infty} P \left( E_{i} \right)$$
- **Continuity**
	- For an increasing sequence *i.e.* $E_{1} \subset E_{2} \subset \cdots \subset E_{n} \subset E_{n+1} \subset \cdots$, $$\lim_{n \to \infty} E_{n} = \bigcup_{i=1}^{\infty} E_{i}$$
	- For a decreasing sequence *i.e.* $E_{1} \supset E_{2} \supset \cdots \supset E_{n} \supset E_{n+1} \supset \cdots$, $$\lim_{n \to \infty} E_{n} = \bigcap_{i=1}^{\infty} E_{i}$$
- If $\{E_{n} : n\geq 1\}$ is an increasing (or decreasing) sequence of events, then $$P \left( \lim_{n \to \infty} E_{n} \right) = \lim_{n \to \infty} P \left( E_{n} \right)$$
- [[Law of Total Probability]]
- [[Bayes' Theorem]]

### Type
- [[Conditional probability]]
