### Concept
- Aka **3rd quartile**, $\frac{3}{4}$-**quantile**, **75th percentile**
- *Notation:* $Q_{3}$ or $P_{75}$
- *What is it:* The value below which 75% of the data falls
### Interpretation
- [[Median]] of the upper half of the dataset
### Calculation
#### Population
- Refer to [[Quantile#Definition]]
#### Sample
1. Order the data from smallest to largest.
2. Find the overall median
3. Form the upper half:
	- If the dataset has an odd number of observations, exclude the overall median. The upper half consists of the $\frac{n-1}{2}$ observations that lie strictly above the median
	- If the dataset has an even number of observations, split the data into two equal halves of size $\frac{n}{2}$​. The upper half is the second (larger) half
4. $Q_{3}$ is the median of that upper half
### Example
#### Odd
- Data: 1, 3, 4, 5, 7, 8, 9, 10, 12
- Median: $Q2= 7$ 
- Upper half (exclude 7): 8, 9, 10, 12
- $Q3 = \text{median} = 9.5$
#### Even
- Data: 1, 3, 4, 5, 7, 8, 9, 10
- Median: $Q2=\frac{5+7}{2}=6$
- Upper half: 7, 8, 9, 10
- $Q3 = \text{median} = 8.5$
### Caution
- There is no single universally agreed computational rule for discrete data. Always state which method you are using when precision matters