


# DS and AI

- [Gate Syllabus](https://gate2024.iisc.ac.in/wp-content/uploads/2023/08/GATE2024DataScienceAIsyllabus.pdf)

Topics:
- [Probability and Statistics](#probability-and-statistics)

## Probability and Statistics:

### Counting (Permutations and Combinations)

To calculate permutations and combinations, you can use the following formulas:

- Permutations: The number of ways to arrange a set of objects in a specific order.
    - Formula: $$(nPr = \frac{n!}{(n - r)!})$$
    - Example: If you have 5 objects and you want to arrange them in groups of 3, the number of permutations would be $(5P3 = \frac{5!}{(5 - 3)!} = 60)$.

- Combinations: The number of ways to select a subset of objects from a larger set, without considering the order.
    - Formula: $$(nCr = \frac{n!}{r! \cdot (n - r)!})$$
    - Example: If you have 5 objects and you want to select 3 of them, the number of combinations would be $(5C3 = \frac{5!}{3! \cdot (5 - 3)!} = 10)$.


### Probability Axioms

 - **Defination**: we define probability as a **`set function`** with values in $[1,2]$, which stisfies the following `axioms`:

    1. The probablity of event **A** in sample space **S** is a non-negative real number.
        
        $$P(A) \geq 0\text{, for every event }A \subset S$$

    2. Probability of Sample Space is !:

        $$P(S)=1$$

    3. if $A_1, A_2, ...$ is

        - sequence of **`mutually exclusive events`**, i.e.:

            $$A_i \cap A_j = \emptyset , \quad \text{for} \quad i \neq j , \quad \text{and} \quad i , j = 1 , 2 , \ldots ,$$

        - such that $A = \bigcup_{i=1 \text{ to } \infty} A_i$, then:

            $$P(A) = P\left(\bigcup_{i=1 \text{ to } \infty} A_i\right) = \sum_{i=1 \text{ to } \infty} P(A_i)$$

> These three `Axioms` are building blocks of other properties of Pobability.

#### Theorem 1 (Probability of Empty Set): *Probability of an Empty Set is 0*

$$P(\emptyset) = 0$$
---

#### Theorem 2 (The addition law of probability): *if $A_1,A_2,...$ are mutually exclusive events, then probability of their union is sum of their probabilities, i.e.*

$$P(\bigcup_{i=1\text{ to }n} A_i) = \sum_{i=1\text{ to }n}P(A_i)$$
---

#### Theorem 3 (The Complement Rule): *if $A$ is an event, then*

$$P(A^c) = 1 - P(A)$$
---

#### Theorem 4 (The Monotonocity Rule): *for any two event $A\text{ \& }B$ such that $B \subset A$, we have:*

$$P(A)\geq P(B)$$
---

#### Theorem 5 (Probability of Union): *for any two events $A,B$*

$$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$
---

#### Theorem 6 (Boole's inequality): *for the events $A_1,A_2,...,A_n$ :*

$$P(A_1\cup A_2\cup ... \cup A_n) \leq \sum_{i=1\text{ to }n} P(A_i)$$

#### De

