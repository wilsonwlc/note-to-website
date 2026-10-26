### Concept
- Aka **2nd quartile**, $\frac{1}{2}$-**quantile**, **50th percentile**
- *Notation:* $Q_{2}$ or $P_{50}$
- *What is it:* The value below which 50% of the data falls
### Interpretation
- The middle value in a dataset when it is ordered from smallest to largest
- It is less sensitive to extreme values than the mean
### Calculation
#### Population median
- Refer to [[Quantile#Definition]]
#### Sample median
For an ordered sets of values $x_{1}, x_{2}, ..., x_{n}$,
- If $n$ is odd, 
	$$
	\text{Median} = x_{\frac{n+1}{2}}
	$$
- If $n$ is even, 
	$$
	\text{Median} = \frac{1}{2}(x_{\frac{n}{2}} + x_{\frac{n}{2}+1})
	$$

### When
- The data is skewed or has outliers. 
- You want a measure of central tendency that is not influenced by extreme values.
- The data is ordinal or skewed, and you want a more robust measure.
### Caution
- The median may not be suitable if you are interested in the average value and the distribution of data is not skewed. *Reason:* If the distribution is roughly symmetric and free of outliers, the mean is usually preferred because it uses every observation and has better theoretical properties for inference
- If you delete the largest and smallest values, the sample median will be unchanged.