### Concept
- *When we need it:* allocate patients treatment groups
### Simple Randomisation
#### Step
1. For each participant, independently generate a random variable $U \sim \mathrm{Uniform}(0,1)$
2. Allocate the participant to treatment group $X = 1+ \lfloor g \times U \rfloor$
	- $g$: the number of treatment groups
	- $\lfloor . \rfloor$: floor function
#### Interpretation
- $X$ takes values in the set $\{1, 2,..., g\}$ with equal probability $$P(X=k) = \frac{1}{g}$$
	- $k=1,...,g$
	- $X \sim \text{Discrete Uniform}\{1, 2,..., g\}$
#### Cons
- In simple randomisation, each participant is assigned independently to a treatment group purely by chance. In a small trial, this can easily produce unequal numbers in each group and hence imbalance in important baseline characteristics
#### When
- Large trial
### Random Permutation
#### Step
Assume there are $n$ (*e.g.* 20) patients and $g$ treatments (*e.g.* 2 treatments: A and B)
1. Decide treatment allocation size *i.e.* number of patients for each treatment *e.g.* 10 patients for Treatment A, 10 patients for Treatment B
2. Create the treatment allocation list which contains $n$ treatment labels *e.g.* `[A,A,A,A,A,A,A,A,A,A,B,B,B,B,B,B,B,B,B,B]`
3. Apply a random permutation *i.e.* shuffle *e.g.* `[B,A,A,B,B,A,B,A,A,B,A,B,A,B,A,B,B,A,A,B]`
4. Enrol patient sequentially *e.g.* 
	- Patient 1 receives Treatment B
	- Patient 2 receives Treatment A
	- Patient 3 receives Treatment A
#### Cons
- Interim imbalance can happen although final balance is guaranteed. 
	- *e.g.* If the permuted allocation list is `[A,A,B,A,A,A,B,A,B,B,A,B,A,B,B,A,A,B,B,A]`. Among the first 6 patients, only 1 receives Treatment B
	- *When it happens:* the trials stop early or recruitment is slow. This matters especially in small trials, sequential enrolment, or multi-centre trials
	- *Solution:* Randomly Permuted Blocks
### Randomly Permuted Blocks
#### Step
Assume there are $n$ (*e.g.* 40) patients and $g$ treatments (*e.g.* 2 treatments: A and B) 
1. Choose allowable block lengths *e.g.* `{4,6,8}`
2. Randomly select a block length *e.g.* 6
3. Create balanced treatment labels within the block *e.g.* `[A,A,A,B,B,B]`
4. Randomly permute treatments within the block *e.g.* `[B,A,B,A,A,B]`
5. Repeated Step 2 to Step 4 for subsequent blocks until all $n$ patients are allocated *e.g.*
	- Block 1 with size 6: `[B,A,B,A,A,B]`
	- Block 2 with size 4: `[A,B,B,A]`
#### Practice
##### Block size
- The block size should usually be multiple of $g$
- Small block size (*e.g.* 2) increase predictability of allocation
#### Caution
- If the block size is fixed, investigator may predict future allocation. *e.g.* When the fixed block size is 4 and the allocation `A,B,A` is observed, we can expect the next patient receive Treatment B. This can create risk of allocation bias (*Reason:* allocation sequence is predictable) and selection bias (*Reason:* investigator behaviour may be influenced by prediction)