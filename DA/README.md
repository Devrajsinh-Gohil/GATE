
# DS and AI

- [Gate Syllabus](https://gate2024.iisc.ac.in/wp-content/uploads/2023/08/GATE2024DataScienceAIsyllabus.pdf)

Topics:

- [Probability](#probability)
- [Statistics](#statistics)

# Probability

### Counting (Permutations and Combinations)

To calculate permutations and combinations, you can use the following formulas:

- Permutations: The number of ways to arrange a set of objects in a specific order.
  - Formula:  
  - $$nPr = \frac{n!}{(n-r)!}$$
  - Example: If you have 5 objects and you want to arrange them in groups of 3, the number of permutations would be $(5P3 = \frac{5!}{(5 - 3)!} = 60)$.

- Combinations: The number of ways to select a subset of objects from a larger set, without considering the order.
  - Formula: 
  - $$nCr = \frac{n!}{r!\cdot(n-r)!}$$
  - Example: If you have 5 objects and you want to select 3 of them, the number of combinations would be $(5C3 = \frac{5!}{3! \cdot (5 - 3)!} = 10)$.

### Probability Axioms

### [Reference](https://bookdown.org/tara_manon/MF_book/axioms.html)

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

#### Conditional Probability

**let A and B be two events, then probability of event A given event B is denoted by $P(A | B)$ :**

$$P(A|B) = \frac{P(A\cap B)}{P(B)},\text{ for }P(B) > 0$$

#### Independence

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

# Statistics

## Expectation and variance

### [Reference](https://www.stat.auckland.ac.nz/~fewster/325/notes/ch3.pdf)

### Expectaions

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

1. Let g and h be functions and, let a anb b be constants. For any random vriable X (discrete or continuous):

$$E[ag(X)+bh(X)] = aE[g(X)]+ bE[h(X)]$$

In particular:

$$E(aX+b)= aE(X) + b$$

2. Let X and Y be any random variables (disrete, continuous,independent, or non-independent). Then

$$E(X+Y) = E(X) + E(Y)$$

3. Let X and Y be `independent` random variables, and g anh be functions. Then

$$E(XY) = E(X)E(Y)$$
$$E(g(X)h(Y)) = E(g(X))E(h(Y))$$

> Note: if X and Y are independent, then $E(XY)=E(X)E(Y)$ is true. However converse is not generally true: it is possible that $E(XY)=E(X)E(Y)$ eventhough X and Y are dependent.

#### Probability as an Expectation

Let A be any event, we can write P(A) as an expectation as follows.

Define indeicator function:

$$I_A = \begin{cases}
   1 &\text{if event A occurs} \\
   0 &\text{otherwise } 
\end{cases}$$

Then $I_A$ is a random variable, and 

$$E(I_A) = \sum_{r=0}^{1}rP(I_A = r) \\ 
= 0 * P(I_A = 0) + 1 * P(I_A = 1) = P(I_A = 1) = P(A)
$$

Therefore,

$P(A) = E(I_A)$ for any event A


## Variance, covariance and correlaiton

### Variance

THe defoantion of variance for random variable X is a measure how spread out it is. Are vlues of X clustered tightly around the mean, or can be commonly observe values of X a long way from mean value? The *varicance* measures how far is the values of X are from mean, on average.

*Defination*: Let X be a random variable. The **variance ** of X is:

$$Var(X) = E((X-\mu_X)^2) = E(X^2) - (E(X))^2$$

> Note:  
> $$E(X^n) = \int_{-\infty}^{\infty}x^n\cdot f_X(x)dx$$

The variance is the ***mean squared deviation*** of random variable form its own mean.

- If X has *high variance* values of X are scttered long way from mean.
- If X has *low variance* values of X are tightly clusterd around the mean.
  
### Covariance

Covariance is a measure of he associtaion or the dependence two random variables X and Y. Covariance can either be positive or negative.

> Note: Variance is always positive.

*Defination*: Let X and Y be random varibles. The **covariance** between X and Y are given by

$$cov(X,Y) = E\{(X-\mu_X)(Y-\mu_Y)\}; \mu_X = E(X), \mu_Y = E(Y)$$

1. if **cov(X,Y)** is `positive` then large values of X tend to occur with large values of Y, and smaill values of X tend to occur with small values of Y.

2. if **cov(X,Y)** is `negative` then large values fo X tend to occur with small values of Y, adn small values of X tend to occur with large values of Y.

3. If X and Y are independent  there is no pattern between large values of X and large values of Y, so cov(X,Y) = 0. However, cov(X,Y) = 0 deos not imply that X and Y are independent, unsless X and Y are Noramlly distributed.

### Properties of variance

1. Let g be a function, and let a and b be constants. For any random variable X(discrete or continuous), 

$$Var(a\cdot g(X)+b) = a^2Var(g(X))$$

In particular:

$$Var(a\cdot X+b) = a^2Var(X)$$

2. If X and Y are `independent` random variables. Then,

$$Var(X+Y) = Var(X)+Var(Y)$$

3. If X and Y are `NOT independent` random variables, then,

$$Var(X+Y) = Var(X)+Var(Y)+2cov(X,Y)$$

### Correlation

The correalation coefficient of X and Y is a liner measure of association between X and Y. It is given by covariance, scaled by the overall variability in X and Y. As a result, correaltion coefficient is always between -1 and +1, so it ias easily compmared for different quantities.

>Note: Has same sign as that of covariance.

*Defination*: The `correlation` between X and Y, also called `correlation coefficient`, is given by

$$corr(X,Y) = \frac{cov(X,Y)}{\sqrt{Var(X)Var(Y)}}$$

The correlation is $\pm 1$ only if there is a perfect linear relationship between X and Y, i.e. $corr(X,Y)=1 \Longleftrightarrow Y = aX + b$

### Conditional expectation and conditional variance

*Defination*: Let X and Y be discrete random variables. the **condtional probability function** of X, given that Y = y, is:

$$P(X=x|Y=y) = \frac{P(X=x \text{ AND } Y=y)}{P(Y=y)} $$

we write conditional probability function as:

$$f_{X|Y}(x|y) = P(X=x|Y=y)$$

> Note: The conditional probabilities $f_{X|Y}(x|y)$ sum to 1, just like any other probability function: 
> $$\sum_x P(X=x|Y=y) = \sum_x P_{\{Y=y\}}(X=x) = 1$$

#### Condtional Expectation

*Defination*: Let X and Y be discrete random variables. The **conditional expectation of X, given that Y=y**, is:

$$\mu_{X|Y = y} = E(X|Y = y) = \sum_x xf_{X|Y}(x|y)$$

E(X|Y = y) is the mean of the value X, when Y is fixed at y.

#### Conditional Variance

*Defination*: Let X and Y be discrete random variables. The **conditional variance of X, given that Y=y**, is:

$$Var(X|Y) = E(X^2|Y) - \{E(X|Y)\}^2 = E\{(X-\mu_{X|Y})^2|Y\}$$

### Standard Deviation

*Defination*: it is square root of `Varaince`, denoted bt $\sigma$

$$\sigma = \sqrt{Var}$$

### The total law of expectation and variance:

1. ***Law of Total Expectation:***

$$E(X) = E_Y(E(X|Y))$$

2. ***Law of Total Variance:***

$$Var(X) = E_Y(Var(X|Y)) + Var_Y(E(X|Y))$$