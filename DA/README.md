


# DS and AI

- [Gate Syllabus](https://gate2024.iisc.ac.in/wp-content/uploads/2023/08/GATE2024DataScienceAIsyllabus.pdf)

Topics:
- [Probability](#probability)
- [Statistics](#statistics)

## Probability

### Counting (Permutations and Combinations)

To calculate permutations and combinations, you can use the following formulas:

- Permutations: The number of ways to arrange a set of objects in a specific order.
    - Formula:  
    - $$nPr = \frac{n!}{(n-r)!}$$
    - Example: If you have 5 objects and you want to arrange them in groups of 3, the number of permutations would be $(5P3 = \frac{5!}{(5 - 3)!} = 60)$.

- Combinations: The number of ways to select a subset of objects from a larger set, without considering the order.
    - Formula: 
    - $$ nCr = \frac{n!}{r! \cdot (n - r)!} $$
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

### Theorems

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

### Laws

#### De Morgan's Law

$$
    P(A^c\cup B^c) = P((A\cap B)^c) = 1 - P(A\cap B)  
$$
$$
    P(A^c\cap B^c) = P((A\cup B)^c) = 1 - P(A\cup B)
$$


#### Conditional Probability:
**let A and B be two events, then probability of event A given event B is denoted by $P(A | B)$ :**

$$P(A|B) = \frac{P(A\cap B)}{P(B)},\text{ for }P(B) > 0$$

#### Independence:

Two events A and B are independent if occurence of one event has no effect on the probability of other event. Thus,

$$ P(A|B) = P(A) $$

equivalently,
$$ P(B|A) = P(B) $$

*`Derivation`* 

$$ P(A|B) = P(A)$$
$$P(A|B) = \frac{P(A\cap B)}{P(B)}$$
$$P(A) = \frac{P(A\cap B)}{P(B)}$$
$$P(A\cap B)= P(A)*P(B)$$


#### Total Probabilities

let $B_1,B_2,...,B_k,...,B_n$ be mutually disjoint events, satisfying $S=\bigcup_{i=1}^{n}B_i\text{, and }P(B_i)>0$ for every i = 1,2,...,n then for every A we have that:

$$P(A) = \sum_{i=1}^{n}P(A|B_i) P(B_i)$$

>Let B satisfy 0 < P(B) < 1;  then for evey event A:
>$$P(A) = P(A|B) P(B) + P(A|B^c) P(B^c)$$

#### Bayes’ Theorem

let $B_1,B_2,...,B_k,...,B_n$ be mutually disjoint events, satisfying $S=\bigcup_{i=1}^{n}B_i\text{, and }P(B_i)>0$ for every i = 1,2,...,n then for every event A for which P(A)>0, we have:

$$P(B_k|A) = \frac{P(A|B_k)P(B_k)}{\sum_{i=1}^{n}P(A|B_i) P(B_i)}$$

>Note: this implies
>$$P(A|B) P(B) = P(B|A) P(A)$$


## Statistics

### Expectation and variance

#### Expectaions

The **mean**, **expected value** or **expectation** of a random variable X is written as E(X) or $\mu_x$. If we observe N random values of X, then mean of N values will be approximately equal to E(X) for large N.

> It is defined differently for continuous and discrete random variables.

*Defination for continuous*: Let X be a **`continiuous`** random variable with p.d.f $f_X(x)$. The expected value of X is:

$$E(X) = \int_{-\infty}^{\infty}x.f_X(x)dx$$

*Defination for discrete*: Let X be **`discrete`** random variable with probability function $f_X(x)$. The expected value of X is:

$$E(X) = \sum_x xf_X(x) = \sum_xxP(X=x)$$


> Similarly `Expectation of g(X)` we define `E(g(x))` <br>
> Continuous:
> $$E(g(X)) = \int_{-\infty}^{\infty}g(x).f_X(x)dx$$
> Discrete:
> $$E(g(X)) = \sum_x g(x)f_X(x) = \sum_xg(x)P(X=x)$$

**Expextation of E(XY)**

Suppose random variables X and Y are dependent on each other, and observing number of pairs $(x_1,y_1),(x_2,y_2),...,(x_N,y_N)$. As X and Y are dependent value of $x_i$ might affect $y_i$ and vice-versa.

As number of pairs N tends to infinity the average:

$$\frac{1}{N}\sum_{i=1}^Nx_i\text{ x }y_i$$

approaches to expectation E(XY).

#### Properties of Expectation

To Be Continued......
