### Definition
Let $\Omega$ be the set containing all possible outcomes. It is called as **sample space**
- **Event** is defined as a subset of $\Omega$ 
- An event $E$ is said to **occur** if the outcome belongs to $E$
### Interpretation
- $A \cup B$ occurs if either $A$ or $B$ occurs
- $A \cap B$ occurs if both $A$ and $B$ occur
### Properties
- If $E=\phi$, we call the event **empty event**. Otherwise, it is called **non-empty event**
- A non-empty event that cannot be decomposed into a number of non-empty events is called an **elementary event**. Otherwise it is called a **compound event**
- Two events $A$ and $B$ are said to be **disjoint** if $A \cap B = \phi$ *i.e.* they have no common elements. 
	- It is impossible that both events occur
- A group of events $E_{1}, E_{2},..., E_{n}$ are said to be **mutually exclusive** if any two events are disjoint i.e. 
$$
E_{i} \cap E_{j} \neq \phi \; \forall i \neq j
$$
- A group of events $E_{1}, E_{2},..., E_{n}$ are said to be **exhaustive** if the union of them is the sample space  
$$
E_{1} \cup E_{2} \cup \dots \cup E_{n} = \Omega
$$
- A group of events $E_{1}, E_{2},..., E_{n}$ is called to be a **partition** if the events are **mutually exclusive and exhaustive**
- The **complement** of event $E$ is the collection of the outcomes not contained in $E$  $$E^{c} = \Omega \setminus E$$ 
### Interpretation
- **Exhaustive**: At least one of the events $E_{1}, E_{2},..., E_{n}$ will occur
- **Mutually exclusive and exhaustive**: Exactly one and only one of the events $E_{1}, ..., E_{n}$ occurs
- **Complement**: $E^{c}$ occurs if $E$  does not occur