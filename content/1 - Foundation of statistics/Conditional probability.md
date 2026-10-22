### Definition
Consider [[Event & occurrence|event]] $A$ and $B$. 
Assume $P(B) > 0$
The **conditional probability** of $A$ given the occurrence of B is written as and is defined as $$P(A|B) = \frac{P(A \cap B)}{P(B)}$$
### Interpretation
- When part of the outcome is fixed *i.e.* we have some information in advance, then the calculation of probability of its occurrence should be restricted to a smaller sample space based on the new information
- $P(A|B) \geq P(A \cap B)$
	- When $P(B) = 1$, $P(A|B) = P(A \cap B)$
	- When $P(B) < 1$, $P(A|B) > P(A \cap B)$
### Property
- **Multiplication theorem**
	- For any two events $A$ and $B$ with $P(B) > 0$, $$P(A\cap B) = P(B) P(A|B)$$
	- For any three events $A$, $B$, $C$ with $P(B \cap C) >0$, $$P \left( A \cap B \cap C \right) = P(C) P \left( B \mid C \right) P \left( A \mid B \cap C \right) $$