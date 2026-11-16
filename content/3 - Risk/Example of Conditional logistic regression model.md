### Question
- A [[Matched case-control study|study]] was conducted in Greece ([Trichopoulous et al, 1976](https://www.floppybunny.org/robin/web/virtualclassroom/stats/statistics2/articles/cond_log_reg_trichopulos_1976.pdf)) to estimate the effect of spontaneous abortions (miscarriage) and induced abortions on subsequent risk of infertility.
### Data
#### Inclusion and exclusion criteria
- Cases: 100 women with secondary infertility (*i.e.* inability to become pregnant after previously giving birth)
- Controls: 2 healthy controls per case. They are from the same hospital as case and matched on age, parity (number of pregnancies carried to a viable gestational age), and level of education
#### Schema
| Variable       | Type             | Description / levels                                              |
| -------------- | ---------------- | ----------------------------------------------------------------- |
| education      | Factor (ordered) | Education level: "0-5yrs", "6-11yrs", "12+ yrs"                   |
| age            | Numeric          | Age in years of the case                                          |
| parity         | Numeric          | Number of prior pregnancies (count)                               |
| induced        | Numeric          | Number of prior induced abortions: 0, 1, or 2 (2 = 2 or more)     |
| case           | Numeric          | Case status: 1 = case (infertile), 0 = control                    |
| spontaneous    | Numeric          | Number of prior spontaneous abortions: 0, 1, or 2 (2 = 2 or more) |
| stratum        | Integer          | Matched set number (1–83)                                         |
| pooled.stratum | Numeric          | Pooled stratum number (1–63)                                      |
### Code
```R
library(dplyr)
library (survival)

data("infert")
df0 <- infert

# Data preparation
df1 <- df0 %>%
  mutate(induced = factor(induced),
         spontaneous = factor(spontaneous)) %>%
  select(-"pooled.stratum")

# Fit conditional logistic regression
m_condLR <- clogit(case ~ induced + spontaneous + strata (stratum),
                   data = df1)

# Show result
summary(m_condLR)
```
- [[Conditional logistic regression model|Conditional logistic regression model]] was fitted
### Output
![[Example of conditional logistic regression model - output.png]]