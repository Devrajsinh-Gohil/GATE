
# DS and AI

- [Gate Syllabus](https://gate2024.iisc.ac.in/wp-content/uploads/2023/08/GATE2024DataScienceAIsyllabus.pdf)

Topics:

- [Probability](#probability)
- [Statistics](#statistics)
- [Calculus and Optimaization](#calculus-and-optimiztiion)

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

## Distributions:
### [Reference](https://drive.google.com/file/d/1aoUqLYWbZORrzv-iI9rkfuQ4K1dt2ZSD/view?usp=sharing)
### [Reference Table](https://drive.google.com/file/d/12gl72N1Bs8o7Rfz9IosQ68PU2Vohz2NJ/view?usp=sharing)




# Calculus and Optimiztiion

## Functons of a single variable

**Defination 1.** 

*A function f from a set A to a set B is a rule that assigns to each element x in A one and only one element y in B.We denote it by f :A→B.*


The set A is called the `domain` of the function f. The elements y in B, called the values of f at x is denoted by f(x). The set of all values y = f(x), as x varies over the domain of f is called the `range` of f.



- Finding Domain of a function
  - If the domain of the function f is not specifically mentioned, we will adopt the convention that the domain of f is the set of all numbers x for which f(x) is a real number.
- Finding Range of a function
  - Invert the function and find the range w.r.t x.
- Vertical line test
  - A curve in the xy-plane is the graph of a function f defined by the equation y = f (x) if and only if the no vertical line intersect the curve at more than one point.
- Odd and Even functions
  - A function f that satisfies f(−x) = f(x) for every x in its do- main is called an even function. The graph of an even function is symmetric with respect to the x-axis. An example of an even function is $f(x) = (x)^2$.
  - A function f that satisfies f (−x) = −f (x) for every x in its domain is called an odd func- tion. The graph of an odd function is symmetric with respect to the origin. An example of an odd function is $f(x) = (x)^3$.
- Operations on Function
  - Let f and g be functions with domains A and B, respectively. Then their sum f+g, difference f−g, product fg,and quotient f/g are defined as follows:
    - (f+g)(x) = f(x) + g(x), with domain = A ∩ B
    - (f−g)(x) = f(x) − g(x), with domain = A ∩ B
    - (fg)(x) = f(x) . g(x), with domain = A ∩ B
    - ($\frac{f}{g}$)(x)= $\frac{f(x)}{g(x)}$, with domain ={ x| x ∈ A ∩ B and g(x) $\neq$ 0}

### Composite function

$(f\cdot g)(x) = f(g(x))$

### Function transformations

- Vertical Transformation:
  - The graph of the function defined by g(x) = f(x) + c , where c is a positive constant, is obtained by shifting the graph of f vertically upward by c units. Similarly, the graph of the function defined by g(x) = f(x) − c , where c is a positive constant, is obtained by shifting the graph of f vertically downward by c units.
  
![img](https://raw.githubusercontent.com/Devrajsinh-Gohil/GATE/main/img/vt.png)

- Horizontal Transformation
  - The graph of the function defined by g(x) = f (x + c) , where c is a positive constant, is obtained by shifting the graph of f horizontally to the left by c units. Similarly, the graph of the function defined by g(x) = f (x − c) , where c is a positive constant, is obtained by shifting the graph of f horizontally to the right by c units.

![img](https://raw.githubusercontent.com/Devrajsinh-Gohil/GATE/main/img/ht.png)

- Vertical Streching and Compressing
  - The graph of the function defined by g(x) = cf(x), where c is a constant with c > 1, is obtained from the graph of f by stretching the latter vertically by a factor of c. Similarly, if 0 < c < 1, then the graph of g is obtained from f by compressing the latter vertically by a factor of 1/c.

![img](https://raw.githubusercontent.com/Devrajsinh-Gohil/GATE/main/img/vsc.png)

- Horizontal Streching and Compressing
  -  The graph of the function defined by g(x) = f (cx) , where c is a constant with 0 < c < 1, is obtained from the graph of f by stretching the graph of the latter horizontally by a factor of 1/c. Similarly if c > 1 , then the graph of g is obtained by compressing the graph of f horizontally by a factor of c.

![img](https://raw.githubusercontent.com/Devrajsinh-Gohil/GATE/main/img/hsc.png)

- Reflection
  -  The graph of the function defined by g(x) = −f(x) is obtained by reflecting the graph of f with respect to the x-axis. The graph of g(x) = f(−x) is obtained by reflecting the graph of f with respect to the y-axis.

![img](https://raw.githubusercontent.com/Devrajsinh-Gohil/GATE/main/img/r.png)


## Limit

*Defination*: Let f(x) be be defined on an open interval 'a' except possiblity at 'a' itself. if f(x) get arbitarily close to L (a finite number) for all x sufficiently close to 'a' we say that f(x) approaches to limit L as x approaches to 'a' and we write

$$\lim_{x→a}f(x) = L$$

and say "the limit of f(x), as x approaches a, equals L"

### Left and Right hand limit of a function

Left hand limit (LHL) = 
$$\lim_{x\rightarrow a^-} f(x) = \lim_{h\rightarrow 0} f(a-h), h > 0$$

Right hand limit (RHL) = 
$$\lim_{x\rightarrow a^+} f(x) = \lim_{h\rightarrow 0} f(a+h), h > 0$$

> Note: 
> - limit of function is said to exist when LHL = RHL = finite and fixed quantity.
> - In $\lim_{x\rightarrow a}f(x), x\rightarrow a$ necessarily implies $x\not ={a}$

### Fundamental Theorems

Let $\lim_{x\rightarrow a} f(x) = l \text{ and } lim_{x\rightarrow a}g(x) = m$ it l and m exists then:

- Sum rule: $\lim_{x\rightarrow a}[f(x) + g(x)] = l + m$
- Difference rule : $\lim_{x\rightarrow a}[f(x) - g(x)] = l - m$
- Product rule: $$\lim_{x\rightarrow a}f(x) \cdot g(x) = l \cdot m$$
- Quotient rule: $\lim_{x\rightarrow a}\frac{f(x)}{g(x)}= \frac{l}{m}$ provided $m\not = 0$
- Constant multiple rule: $\lim_{x\rightarrow a}kf(x) = k\lim_{x\rightarrow a}f(x)$, where k is a constant.
- Power rule: $\lim_{x\rightarrow a}f(x) ^{g(x)} = l ^ m$ provided l > 0.
- $\lim_{x\rightarrow a}f[g(x)] = f\big(\lim_{x\rightarrow a}g(x)\big) = f(m)$; provided f(x) is continuous at x =m.
  
### Indeterminate forms

$\frac{0}{0}$, $\frac{\infty}{\infty}$, $\infty - \infty$, $0\cdot \infty$, $1^\infty$, $0^0$, $\infty^0$

### General method to solve limits

#### Factorization

Important factors:
- $$x^n-a^n = (x-a)(x^{n-1} + ax^{n-2} + ... + a^{n-1}), n \in N$$
- $$x^n+a^n = (x+a)(x^{n-1} - ax^{n-2} + ... + a^{n-1}), \text{n is odd}$$

> **Note**: 
> $$\lim_{x\rightarrow a} \frac{x^n-a^n}{x-a} = na^{n-1}$$

#### Rationalization or double rationalization

In this method we rationalize the factor containing square root and simplify

#### Limit when $x \rightarrow \infty$

- divide the greatest power of x in numerator and denominator
- put x = 1/y and apply $y\rightarrow 0$

#### Sandwich Theorem

if $f(x) \leq g(x) \leq h(x); \forall x$ and $\lim_{x\rightarrow a}f(x) = l = \lim_{x\rightarrow a}h(x)$ then $\lim_{x\rightarrow a}g(x) = l$ 