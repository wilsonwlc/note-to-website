### Motivation
- *Problem:* In [[Parallel group design|parallel group design]], patients may vary so much in their initial disease status and in their response to therapy. Substantial groups of patients on each treatment are needed in order to average out the between patient variations in order to detect any treatment difference
- *Idea:* Give each patient a series of treatments over separate period of time. As a result, each patient can be regarded as own "control". Because comparisons are made within the same patient, variability due to differences between patients is largely removed. Consequently, the within-patient variability is often smaller than the between-patient variability, leading to greater statistical efficiency
### Concept
- *What is it:* a [[Clinical trial|clinical trial]] design in which each participant receives two or more treatments in sequence, with the order of treatments determined by randomisation to treatment sequences
- *What effects it has:*
	- Treatment effect: The primary effect of interest
	- **Period effect**: a systematic change in response attributable to the period in which the measurement is taken rather than to the treatment itself *e.g.* 
		- Disease progression: a patient's condition gradually worsens over time regardless of treatment
		- Recovery or natural improvement: a disease naturally improves over time
		- Seasonal effects: responses vary according to the season in which measurements are taken
		- Learning or training effects: participants become more experienced with repeated testing
		- Ageing or maturation: participants change biologically over time
	- **Carryover effect**: effect due to the persistence of previous treatment *i.e.* when the effect of Treatment A persists into the next period and influences the response under Treatment B
- *How to deal with period effect:* use balanced treatment sequences and randomise participants to sequences. Period effects are typically included as a factor in the statistical model. Without balancing and randomisation, treatment effects may become confounded with changes occurring over time
- *How to deal with carryout effect:* Include an adequate **washout period** between treatment periods so that the effects of the previous treatment have largely dissipated before the next treatment begins
	- *What is the washout period:* a treatment-free interval between treatment periods designed to minimise carryover effects from the previous treatment
- *How many periods it needs:* In a complete crossover trial comparing $n$ treatments, each participant typically receives all $n$ treatments and therefore $n$ periods are required *e.g.*
	- **Two-period crossover trial** for comparing 2 treatments
	- **Three-period crossover trial** for comparing 3 treatments
		- If a crossover trial has more than two periods, it is called a **multi-period crossover trial**
- *How many treatment sequences for a crossover trial has:* For $n$ treatments there are $n!$ possible treatment sequences.
- *In which phase is it common:* [[Clinical trial#Phase I|Phase 1]]
- *When we should use it:*
	- The condition being treated is chronic and relatively stable *e.g.* hypertension, chronic pain, or stable asthma
	- The condition is unlikely to change substantially between treatment periods.
	- The treatment effect occurs relatively quickly
	- The treatment effect is reversible and does not permanently alter the patient's condition
	- Any carryover effect can be minimised by an adequate washout period
- *When we should not use it:*
	- The conditions may resolve quickly, that is an acute condition, making the second period treatment unnecessary. (e.g. infections, trauma, and rehabilitation)
	- Patients are likely to withdraw from treatment or be lost to followup
	- The effect of the first treatment could plausibly contaminate the effect of second. Note for some treatments contamination can be prevented by having a "wash-out" period between treatments
### Interpretation
- Because each participant receives multiple treatments in sequence, each participant serves as their own control.
### Practice
- The duration of each period can vary. 
	- A short period may not allow the treatment effect to reach its full magnitude, and insufficient washout may increase carryover effects.
	- A long period may lead to patient withdrawals and unstable disease condition for some patients. 
- Hence one should consider these potential problems carefully in order to compromise the most appropriate durations