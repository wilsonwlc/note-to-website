### Concept
- Aka **Bayes' rule**, **Bayes' law**
### Definition
#### 2 events
For any two events $A$ and $B$ with $P(A)>0$ and $P(B)>0$, $$P(B|A) = P(A|B) \times \frac{P(B)}{P(A)}$$
- $P(B)$ is called the **prior probability** of $B$. *Why having this name:* It does not take into account any information about $A$
- $P(B|A)$ is called the posterior probability or conditional probability of $B$ given $A$. *Why having this name:* some additional information (occurrence of $A$) has been taken into account
#### General case
If $B_{1}$, $B_{2}$, ..., $B_{k}$ are [[Event & occurrence#Properties|mutually exclusive and exhaustive events]] (*i.e.* a partition of the sample space), and A is any event with $P(A)>0$, then 
for any $B_{j}$, $$P \left( B_{j} \mid A \right) = \frac{P \left( A \mid B_{j} \right) P \left( B_{j} \right)}{P(A)} = \frac{P \left( B_{j} \right) P \left( A \mid B_{j} \right)}{\sum_{i=1}^{k} P \left( B_{i} \right) P \left( A \mid B_{i} \right)}$$
- The second equality needs [[Law of Total Probability]]
### Interpretation
- From the definition 2 events,
	- It connects $P(A|B)$ and $P(B|A)$
	- $P(A|B)$ and $P(B|A)$ are different *e.g.* if we observed that a large proportion of lung cancer patients are smokers, we should not jump to the conclusion that smokers will have large chance to have lung cancer
	- $P(A|B)$ and $P(B|A)$ are the same if and only if $P(A)=P(B)$
	- It describes the way in which one's belief about $B$ are updated by having observed $A$