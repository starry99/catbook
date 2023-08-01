---
layout: simple
title: Probability Part Memory Sheet
---

#### Based on the notes and lectures of [Prof. Almut Veraart](https://sites.google.com/view/almutveraart/home).
## 1. Sample Spaces and Probability

### Definition (Sample Space)

The sample space $$\Omega$$ is defined as the set of all possible outcomes of an experiment. The elements of $$\Omega$$ are typically denoted by $$\omega$$ and called sample points.

### Definition (Naive Definition of Probability)

 Suppose that the sample space $$\Omega$$ is finite, i.e. card $$(\Omega)<$$ $$\infty$$ and consider an event $$A \subseteq \Omega$$. Then the naive probability of $$A$$ is defined as

$$
\mathrm{P}_{\text {Naive }}(A)=\frac{\operatorname{card}(A)}{\operatorname{card}(\Omega)}
$$

## 2. Counting

### Theorem (The multiplication principle)

Consider two experiments: Experiment A has a possible outcomes, and Experiment $$B$$ has b possible outcomes. Then the compound experiment of performing Experiment $$A$$ and $$B$$ (in any order) has ab possible outcomes.

### Definition (Power Set)

 A power set of a set $$A$$, denoted as $$\mathcal{P}(A)$$ is defined as the set of all possible subsets of $$A$$ including $$\emptyset$$ and $$A$$.

### (Cardinality of the power set)

 Consider a sample space $$\Omega$$ with card $$(\Omega)<\infty$$. Then $$\operatorname{card}(\mathcal{P}(\Omega))=2^{\operatorname{card}(\Omega)}$$

### Theorem (Binomial coefficient)

 For any $$k, n \in \mathbb{N} \cup\{0\}$$, we have

$$
\left(\begin{array}{l}
n \\
k
\end{array}\right)=\frac{n(n-1) \cdots(n-(k-1))}{k !}=\frac{(n)_{k}}{k !}=\frac{n !}{(n-k) ! k !}
$$
for $$k \leq n$$, and $$\left(\begin{array}{l}n \\ k\end{array}\right)=0$$ for $$k>n$$.

## 3. Axiomatic Definition of Probability

### Definition (Event Space)

The sample space $$\Omega$$ is defined as the set of all possible outcomes of an experiment. In our previous discussion we assigned (naive) probabilities to events which were subsets of $$\Omega$$. We typically denote by $$\mathcal{F}$$ the event space, which contains the events we are allowed to consider. In fact, in probability theory, we always require that the event space $$\mathcal{F}$$ is a so-called $$\sigma$$-algebra (which is the same as a $$\sigma$$-field).

### Definition (Algebra and $$\sigma$$-algebra)

A collection of subsets of $$\Omega$$ denoted by $$\mathcal{F}$$ is called

1. an algebra (or a field) on $$\Omega$$ if
(a) $$\emptyset \in \mathcal{F}$$
(b) $$\mathcal{F}$$ is closed under complements, i.e. $$A \in \mathcal{F} \Rightarrow A^{c} \in \mathcal{F}$$, and
(c) $$\mathcal{F}$$ is closed under unions of pairs of members, i.e. $$A_{1}, A_{2} \in \mathcal{F} \Rightarrow A_{1} \cup A_{2} \in \mathcal{F}$$.

2. an $$\sigma$$-algebra (or a $$\sigma$$-field) on $$\Omega$$ if
(a) $$\emptyset \in \mathcal{F}$$
(b) $$\mathcal{F}$$ is closed under complements, i.e. $$A \in \mathcal{F} \Rightarrow A^{c} \in \mathcal{F}$$, and
(c) $$\mathcal{F}$$ is closed under countable union, i.e. for any countable $${ }^{1}$$ index set $$\mathcal{I}$$, we have $$A_{i} \in \mathcal{F}$$, for all $$i \in \mathcal{I} \Rightarrow \cup_{i \in \mathcal{I}} A_{i} \in \mathcal{F}$$.

### Definition (Probability Measure)

A mapping $$\mathrm{P}: \mathcal{F} \rightarrow \mathbb{R}$$ is called a probability measure on $$(\Omega, \mathcal{F})$$ if it satisfies three conditions:

(i) $$\mathrm{P}(A) \geq 0$$ for all events $$A \in \mathcal{F}$$

(ii) $$\mathrm{P}(\Omega)=1$$

(iii) For any countable $${ }^{2}$$ sequence of disjoint events $$\left(A_{i}\right)_{i \in \mathcal{I}}$$ with $$A_{i} \in \mathcal{F}$$, for all $$i \in \mathcal{I}$$, we have

$$
\mathrm{P}\left(\bigcup_{i \in \mathcal{I}} A_{i}\right)=\sum_{i \in \mathcal{I}} \mathrm{P}\left(A_{i}\right) .
$$

[Note that by "disjoint events" we mean that $$A_{i} \cap A_{j}=\emptyset$$ for all $$i \neq j$$. ]

### Definition (Probability space)

We define a probability space as the triplet $$(\Omega, \mathcal{F}, \mathrm{P})$$, where $$\Omega$$ is a set (the sample space), $$\mathcal{F}$$ is a $$\sigma$$-algebra (the event space) consisting of subsets of $$\Omega$$ and $$\mathrm{P}$$ is a probability measure on $$(\Omega, \mathcal{F})$$.

### Theorem

- $$\mathrm{P}\left(A^{c}\right)=1-\mathrm{P}(A)$$

- If $$A \subseteq B$$, then $$\mathrm{P}(A) \leq \mathrm{P}(B)$$.

- $$\mathrm{P}(A \cup B)=\mathrm{P}(A)+\mathrm{P}(B)-\mathrm{P}(A \cap B)$$. (Inclusion-exclusion principle)

## 4. Conditional Probability

### Definition (Conditional probability)

 Consider a probability space $$(\Omega, \mathcal{F}, \mathrm{P})$$. Consider events $$A, B \in$$ $$\mathcal{F}$$ with $$\mathrm{P}(B)>0$$. Then the conditional probability of $$A$$ given $$B$$, denoted by $$\mathrm{P}(A \mid B)$$, is defined as

$$
\mathrm{P}(A \mid B)=\frac{\mathrm{P}(A \cap B)}{\mathrm{P}(B)} \text {. }
$$

### Theorem (Multiplication rule)

 Let $$n \in \mathbb{N}$$, then for any events $$A_{1}, \ldots, A_{n}$$ with $$\mathrm{P}\left(A_{2} \cap \cdots \cap A_{n}\right)>0$$, we have

$$
\begin{array}{r}
\mathrm{P}\left(A_{1} \cap \cdots \cap A_{n}\right)=\mathrm{P}\left(A_{1} \mid A_{2} \cap \cdots \cap A_{n}\right) \mathrm{P}\left(A_{2} \mid A_{3} \cap \cdots \cap A_{n}\right) \cdots \\
\mathrm{P}\left(A_{n-2} \mid A_{n-1} \cap A_{n}\right) \mathrm{P}\left(A_{n-1} \mid A_{n}\right) \mathrm{P}\left(A_{n}\right)
\end{array}
$$

where the right hand side is a product of $$n$$ terms.

### Theorem(Bayes' rule)

Let $$A, B \in \mathcal{F}$$ with $$\mathrm{P}(A)>0, \mathrm{P}(B)>0$$. Then

$$
\mathrm{P}(A \mid B)=\frac{\mathrm{P}(B \mid A) \mathrm{P}(A)}{\mathrm{P}(B)}
$$

### Definition (Partition)

A partition of the sample space $$\Omega$$ is a collection $$\left\{B_{i}: i \in \mathcal{I}\right\}$$ (for a countable index set $$\mathcal{I}$$) of disjoint events (meaning that $$B_{i} \in \mathcal{F}$$ and $$B_{i} \cap B_{j}=\emptyset$$ for $$i \neq j$$) such that $$\Omega=\bigcup_{i \in \mathcal{I}} B_{i}$$.

### Theorem (Law of total probability)

 Let $$\left\{B_{i}: i \in \mathcal{I}\right\}$$ denote a partition of $$\Omega$$, with $$\mathrm{P}\left(B_{i}\right)>0$$ for all $$i \in \mathcal{I}$$. Then, for all $$A \in \mathcal{F}$$,

$$
\mathrm{P}(A)=\sum_{i \in \mathcal{I}} \mathrm{P}\left(A \cap B_{i}\right)=\sum_{i \in \mathcal{I}} \mathrm{P}\left(A \mid B_{i}\right) \mathrm{P}\left(B_{i}\right)
$$

### Theorem(Bayes' rule with extra conditioning)

 For events $$A, B, E$$ with $$\mathrm{P}(A \cap E)>0, \mathrm{P}(B \cap E)>$$ 0 , we have

$$
\mathrm{P}(A \mid B \cap E)=\frac{\mathrm{P}(B \mid A \cap E) \mathrm{P}(A \mid E)}{\mathrm{P}(B \mid E)}
$$

### Theorem (Law of total probability with additional conditioning)

 Consider events $$A, E$$ with $$\mathrm{P}(E)>$$ 0 and let $$\left\{B_{i}: i \in \mathcal{I}\right\}$$ denote a partition of $$\Omega$$, with $$\mathrm{P}\left(B_{i} \cap E\right)>0$$ for all $$i \in \mathcal{I}$$. Then,

$$
\mathrm{P}(A \mid E)=\sum_{i \in \mathcal{I}} \frac{\mathrm{P}\left(A \cap B_{i} \cap E\right)}{\mathrm{P}(E)}=\sum_{i \in \mathcal{I}} \mathrm{P}\left(A \mid B_{i} \cap E\right) \mathrm{P}\left(B_{i} \mid E\right)
$$

## 5. Independence

### Definition (Independent events)

The events $$A, B$$ are called independent if

$$
\mathrm{P}(A \cap B)=\mathrm{P}(A) \mathrm{P}(B)
$$

and dependent otherwise.

### Definition (Independence of events (general case))

 1. A finite collection of events $$A_{1}, \ldots, A_{n}$$ is defined to be independent if

$$
\mathrm{P}\left(A_{i_{1}} \cap A_{i_{2}} \cap \cdots \cap A_{i_{k}}\right)=\mathrm{P}\left(A_{i_{1}}\right) \mathrm{P}\left(A_{i_{2}}\right) \cdots \mathrm{P}\left(A_{i_{k}}\right)
$$

for every subcollection $$\left\{i_{1}, \ldots, i_{k}\right\}$$ of $$\{1, \ldots, n\}, k=1, \ldots, n$$.

2. A countable or uncountably infinite collection of events is defined to be independent if each finite subcollection is independent.

### Definition(Conditional independence of events)

Consider events $$A, B, C \in \mathcal{F}$$ with $$\mathrm{P}(C)>0$$. Then we say that $$A$$ and $$B$$ are conditionally independent given $$C$$ if

$$
\mathrm{P}(A \cap B \mid C)=\mathrm{P}(A \mid C) \mathrm{P}(B \mid C)
$$

If we, in addition, assume that $$\mathrm{P}(B \cap C)>0$$, then equation (6.1.3) is equivalent to the condition

$$
\mathrm{P}(A \mid B \cap C)=\mathrm{P}(A \mid C)
$$

## 6. Discrete Random Variables

### Definition (Random variable)

We consider a probability space $$(\Omega, \mathcal{F}, \mathrm{P})$$ and we will think of a random variable (r.v.) as a function from the sample space to the real numbers $$\mathbb{R}$$, i.e.

$$
X: \Omega \rightarrow \mathbb{R}
$$

The function needs to satisfy some properties, which we introduce in the formal definition below. Note that

- Despite the name, a random variable is a function and not a variable.

- We typically use capital letters such as $$X, Y, Z$$ to denote random variables.

- The value of the random variable $$X$$ at the sample point $$\omega$$ is given by $$X(\omega)$$ and is called a realisation of $$X$$.

- The randomness stems from $$\omega \in \Omega$$ (we don't know which outcome $$\omega$$ appears in the random experiment), the mapping itself given by $$X$$ is deterministic.

### Definition (Discrete random variable)

 A discrete random variable on the probability space $$(\Omega, \mathcal{F}, \mathrm{P})$$ is defined as a mapping $$X: \Omega \rightarrow \mathbb{R}$$ such that

(i) the image/range of $$\Omega$$ under $$X$$ denoted by $$\operatorname{Im} X=\{X(\omega): \omega \in \Omega\}$$ is a countable subset of $$\mathbb{R}$$,

(ii) $$X^{-1}(x)=\{\omega \in \Omega: X(\omega)=x\} \in \mathcal{F}$$ for all $$x \in \mathbb{R}$$

### Definition (Probability mass function (pmf))

The probability mass function (pmf) of the discrete random variable $$X$$ is defined as the function $$p_{X}: \mathbb{R} \rightarrow[0,1]$$ given by

$$
p_{X}(x)=\mathrm{P}(\{\omega \in \Omega: X(\omega)=x\})=\mathrm{P}\left(X^{-1}(x)\right)
$$

Note that the definition of the pmf implies the following properties:

$$
p_{X}(x)=0 \quad \text { if } x \notin \operatorname{Im} X
$$

### Remark

Note that the definition of the pmf implies the following properties:

- $$p_{X}(x)=0 \quad \text { if } x \notin \operatorname{Im} X$$
- For $$x_{1}, x_{2} \in \operatorname{Im} X$$ with $$x_{1} \neq x_{2}$$, then
$$
X^{-1}\left(x_{1}\right) \cap X^{-1}\left(x_{2}\right)=\left\{\omega \in \Omega: X(\omega)=x_{1} \text { and } X(\omega)=x_{2}\right\}=\emptyset
$$

- $$
\sum_{x \in \mathbb{R}} p_{X}(x)=1
$$

## 7. Continuous Random Variables

### Definition (Continuous random variable)

 A random variable on the probability space $$(\Omega, \mathcal{F}, \mathrm{P})$$ is defined as the mapping $$X: \Omega \rightarrow \mathbb{R}$$ which satisfies

$$
X^{-1}((-\infty, x])=\{\omega \in \Omega: X(\omega) \leq x\} \in \mathcal{F} \quad \text { for all } x \in \mathbb{R} .
$$

Note that a discrete random variable (see Definition 7.3.1) satisfies the above definition of a random variable. To see this, we can write

$$
\{\omega \in \Omega: X(\omega) \leq x\}=\bigcup_{y \in \operatorname{Im} X: y \leq x}\{\omega: X(\omega)=y\} .
$$

The right hand side is a countable union of elements of $$\mathcal{F}$$ and (according the definition of the sigmaalgebra) hence also an element of $$\mathcal{F}$$.

### Definition (Cumulative distribution function (cdf))

 Suppose that $$X$$ is a random variable on $$(\Omega, \mathcal{F}, \mathrm{P})$$, then the cumulative distribution function (c.d.f.) of $$X$$ is defined as the mapping $$F_{X}: \mathbb{R} \rightarrow[0,1]$$ given by

$$
F_{X}(x)=\mathrm{P}(\{\omega \in \Omega: X(\omega) \leq x\})=\mathrm{P}\left(X^{-1}((-\infty, x])\right),
$$

which is typically abbreviated to $$F_{X}(x)=\mathrm{P}(X \leq x)$$.

### Theorem (Properties of the c.d.f.)

 1. $$F_{X}$$ is monotonically non-decreasing, i.e. for all $$x \leq y$$ we have $$F_{X}(x) \leq F_{X}(y)$$

 2. $$F_{X}$$ is right-continuous, i.e. if $$x_{n} \downarrow x$$ (which is short-hand notation for a sequence $$\left(x_{n}\right)_{n \in \mathbb{N}}$$, which is monotonically non-increasing, i.e. $$x_{1} \geq \cdots \geq x_{n} \geq x_{n+1} \geq \cdots \geq x$$ and converging to $$x$$, i.e. $$\left.\operatorname{~im}_{n \rightarrow \infty} x_{n}=x\right)$$, then $$F_{X}\left(x_{n}\right) \rightarrow F_{X}(x)$$ as $$n \rightarrow \infty$$.

 3. $$\lim _{x \rightarrow-\infty} F_{X}(x)=0$$ and $$\lim _{x \rightarrow \infty} F_{X}(x)=1$$.

### Theorem

For $$a<b$$, we have $$\mathrm{P}(a<X \leq b)=F_{X}(b)-F_{X}(a)$$.

### Definition (Continuous random variable and probability density function) 

A random variable $$X$$ is called continuous if its c.d.f. can be written as

$$
F_{X}(x)=\mathrm{P}(X \leq x)=\int_{-\infty}^{x} f_{X}(u) d u, \quad \text { for all } x \in \mathbb{R}
$$

where the function $$f_{X}: \mathbb{R} \rightarrow \mathbb{R}$$ satisfies

(i) $$f_{X}(u) \geq 0$$ for all $$u \in \mathbb{R}$$,
(ii) $$\int_{-\infty}^{\infty} f_{X}(u) d u=1$$

We call $$f_{X}$$ the probability density function (p.d.f.) of $$X$$ (or just the density). $${ }^{1}$$

### Theorem

For a continuous random variable $$X$$ with density $$f_{X}$$, we have

$$
\mathrm{P}(X=x)=0, \quad \text { for all } x \in \mathbb{R}
$$

### Example of a random variable which is neither discrete nor con- tinuous

We flip an unfair coin infinitely many times and assume that we obtain heads with probability $$p \in(0,1)$$. We denote the outcomes by $$X_{1}, X_{2}, \ldots$$ with $$X_{i}=0$$ if we obtain tails in the ith flip and $$X_{i}=1$$ if we obtain heads in the ith flip. Define a random number

$$
\begin{aligned}
& Y=0 . X_{1} X_{2} X_{3} \ldots \quad(\text { in base } 2), \text { i.e. } \\
& Y=X_{1} \cdot \frac{1}{2}+X_{2}\left(\frac{1}{2}\right)^{2}+X_{3} \cdot\left(\frac{1}{2}\right)^{3}+\cdots .
\end{aligned}
$$

Then

- $$X_{1}$$ determines whether $$Y$$ is in the first half $$\left[0, \frac{1}{2}\right)$$ (if $$X_{1}=0$$) or in the second half $$\left[\frac{1}{2}, 1\right]$$ (if $$\left.X_{1}=1\right)$$.

- $$X_{2}$$ determines whether $$Y$$ is in the first half (if $$X_{2}=0$$) (either in $$\left[0, \frac{1}{4}\right.$$) or in $$\left[\frac{1}{2}, \frac{3}{4}\right)$$) or in the second half (if $$X_{2}=1$$) (either in $$\left[\frac{1}{4}, \frac{1}{2}\right.$$) or in $$\left[\frac{3}{4}, 1\right]$$) of the previous half.

- etc.

We note that for any $$y=0 . x_{1} x_{2} x_{3} \ldots$$ in base 2 representation, we have

$$
\mathrm{P}(Y=y)=\mathrm{P}\left(X_{1}=x_{1}\right) \mathrm{P}\left(X_{2}=x_{2}\right) \cdots=0
$$

since each term in the product is either equal to $$p$$ or $$1-p$$ which are both smaller than 1 , so their infinite product will converge to 0 . Hence $$Y$$ cannot be a discrete random variable.

One (not we!) can show that for $$p \neq 0.5, Y$$ does not have a density, whereas if $$p=0.5$$, then $$Y$$ is uniformly distributed on $$[0,1]$$ and hence has a density.

## 8. Transformations of random variables

### Theorem (Discrete Case)

Let $$X$$ be a discrete random variable on $$(\Omega, \mathcal{F}, \mathrm{P})$$ and let $$g: \mathbb{R} \rightarrow \mathbb{R}$$ denote a deterministic function. Then $$Y=g(X)$$ is a discrete random variable with probability mass function given by

$$
p_{Y}(y)=\sum_{x \in \operatorname{Im} X: g(x)=y} \mathrm{P}(X=x)
$$

for all $$y \in \operatorname{Im} Y$$ and 0 otherwise.
In the special case when $$g$$ is invertible (i.e. bijective), then the pmf of $$Y$$ can be expressed as

$$
p_{Y}(y)=p_{X}\left(g^{-1}(y)\right) \quad \text { for all } y \in \operatorname{Im} Y
$$

### Theorem (Continuous Case)

Suppose that $$X$$ is a continuous random variable with density $$f_{X}$$ and $$g: \mathbb{R} \rightarrow \mathbb{R}$$ is strictly increasing/decreasing and differentiable with inverse function denoted by $$g^{-1}$$, then $$Y=g(X)$$ has density

$$
f_{Y}(y)=f_{X}\left(g^{-1}(y)\right)\left|\frac{d}{d y}\left[g^{-1}(y)\right]\right|, \quad \text { for all } y \in \mathbb{R}
$$

## 9. Expectation of random variables

### Definition (Expectation of discrete random variable)

 Let $$X$$ denote a discrete random variable, then the expectation of $$X$$ is defined as

$$
\mathrm{E}(X)=\sum_{x \in \operatorname{Im} X} x \mathrm{P}(X=x)
$$

As in the discrete case, we often refer to the expectation as mean or expected value.

### Definition (Expectation and variance of a continuous random variable)

For a continuous random variable $$X$$ with density $$f_{X}$$, we define the expectation of $$X$$ as

$$
\mathrm{E}(X)=\int_{-\infty}^{\infty} x f_{X}(x) d x
$$

provided that $$\int_{-\infty}^{\infty}|x| f_{X}(x) d x<\infty$$

### Theorem (LOTUS: Discrete case)

 Let $$X$$ be a discrete random variable and $$g: \mathbb{R} \rightarrow \mathbb{R}$$, then

$$
\mathrm{E}(g(X))=\sum_{x \in \operatorname{Im} X} g(x) \mathrm{P}(X=x)
$$

whenever the sum on the right hand side converges absolutely.

We will now state (without proof) the LOTUS for the continuous case:

### Theorem (LOTUS: Continuous case)

Let $$X$$ be a continuous random variable with density $$f_{X}$$, consider a function $${ }^{2} g: \mathbb{R} \rightarrow \mathbb{R}$$, then

$$
\mathrm{E}(g(X))=\int_{-\infty}^{\infty} g(x) f_{X}(x) d x
$$

provided that 

$$
\int_{-\infty}^{\infty}|g(x)| f_{X}(x) d x<\infty
$$

Theorem 10.2.6. Consider a discrete/continuous random variable $$X$$ with finite expectation.

1. If $$X$$ is non-negative, then $$\mathrm{E}(X) \geq 0$$.

2. If $$a, b \in \mathbb{R}$$, then $$\mathrm{E}(a X+b)=a \mathrm{E}(X)+b$$. In particular, $$\mathrm{E}(a)=a$$ for any $$a \in \mathbb{R}$$.

### Definition (Variance)

Let $$X$$ be a discrete/continuous random variable. Then its variance is defined as

$$
\operatorname{Var}(X)=\mathrm{E}\left[(X-\mathrm{E}(X))^{2}\right]
$$

provided that it exists. Often we write $$\sigma^{2}=\operatorname{Var}(X)$$.

### Theorem

For a discrete/continuous random variable with finite variance we have that

$$
\operatorname{Var}(X)=\mathrm{E}\left(X^{2}\right)-[\mathrm{E}(X)]^{2}
$$

### Theorem

Let $$X$$ be a discrete/continuous random variable with finite variance and consider deterministic constants $$a, b \in \mathbb{R}$$. Then

$$
\operatorname{Var}(a X+b)=a^{2} \operatorname{Var}(X)
$$

## 10. Multivariable Calculus

#### Change of variables in multiple integrals

Let $$f: \mathbb{R}^{2} \rightarrow \mathbb{R}$$. We define the mapping $$T: \mathbb{R}^{2} \rightarrow \mathbb{R}^{2}$$ by

$$
T(x, y)=(u(x, y), v(x, y))
$$
and assume that $$T$$ is a bijection from the domain $$D \subseteq \mathbb{R}^{2}$$ to some range $$S \subseteq \mathbb{R}^{2}$$. Then we can write $$T^{-1}: S \rightarrow D$$ for the inverse mapping of $$T$$, i.e. $$(x, y)=T^{-1}(u, v)$$. For the first component we write $$x=x(u, v)$$ and for the second $$y=y(u, v)$$. The Jacobian determinant of $$T^{-1}$$ is defined as the determinant

$$
J(u, v)=\operatorname{det}\left(\frac{\partial(x, y)}{\partial(u, v)}\right)=\operatorname{det}\left(\begin{array}{cc}
\frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} \\
\frac{\partial y}{\partial u} & \frac{\partial y}{\partial v}
\end{array}\right)=\frac{\partial x}{\partial u} \frac{\partial y}{\partial v}-\frac{\partial x}{\partial v} \frac{\partial y}{\partial u}
$$

The change of variable formula states that (under mild conditions $${ }^{1}$$)

$$
\iint_{D} f(x, y) d x d y=\iint_{S} f(x(u, v), y(u, v))|J(u, v)| d u d v
$$

## 11. Multivariable random variables

### Definition (Joint distribution function)

 The joint distribution function of the random vector $$(X, Y)$$ is defined as the mapping $$F_{X, Y}: \mathbb{R}^{2} \rightarrow[0,1]$$ given by

$$
F_{X, Y}(x, y)=\mathrm{P}(\{\omega \in \Omega: X(\omega) \leq x, Y(\omega) \leq y\}), \quad \text { for any } x, y \in \mathbb{R} .
$$

Using our shortened notation, we typically write

$$
F_{X, Y}(x, y)=\mathrm{P}(X \leq x, Y \leq y), \quad \text { for any } x, y \in \mathbb{R} .
$$

We can now list some of the key properties of joint distribution functions:

- $$F_{X, Y}$$ is non-decreasing in each variable, meaning that

$$
F_{X, Y}\left(x_{1}, y_{1}\right) \leq F_{X, Y}\left(x_{2}, y_{2}\right) \quad \text { if } x_{1} \leq x_{2} \text { and } y_{1} \leq y_{2} .
$$

- $$F_{X, Y}$$ is continuous from above (the multivariate version of right-continuity), i.e., for two sequences $$\left(x_{n}\right),\left(y_{n}\right)$$ which approach $$x$$ and $$y$$ from the right as $$n \rightarrow \infty$$ we get that $$F_{X, Y}\left(x_{n}, y_{n}\right) \rightarrow F_{X, Y}(x, y)$$.

- We have the following two limits:

$$
\lim _{x \rightarrow-\infty, y \rightarrow-\infty} F_{X, Y}(x, y)=0, \quad \lim _{x \rightarrow \infty, y \rightarrow \infty} F_{X, Y}(x, y)=1 .
$$

- They determine the marginal distributions uniquely, i.e.

$$
F_{X}(x)=\lim _{y \rightarrow \infty} F_{X, Y}(x, y), \quad F_{Y}(y)=\lim _{x \rightarrow \infty} F_{X, Y}(x, y) .
$$

### Definition (Independence of random variables)

 The random variables $$X$$ and $$Y$$ are independent if and only if

$$
\mathrm{P}(X \leq x, Y \leq y)=\mathrm{P}(X \leq x) \mathrm{P}(Y \leq y), \quad \text { for all } x, y \in \mathbb{R}
$$

which is equivalent to saying that the joint distribution function factorises as the product of the two marginal distribution functions:

$$
F_{X, Y}(x, y)=F_{X}(x) F_{Y}(y), \quad \text { for all } x, y \in \mathbb{R}
$$

We call the random variables $$X_{1}, \ldots, X_{n}$$ independent if

$$
\mathrm{P}\left(X_{1} \leq x_{1}, \ldots, X_{n} \leq x_{n}\right)=\mathrm{P}\left(X_{1} \leq x_{1}\right) \cdots \mathrm{P}\left(X_{n} \leq x_{n}\right), \quad \text { for all } \mathbf{x} \in \mathbb{R}^{n}
$$

or equivalently if

$$
F_{\mathbf{X}}(\mathbf{x})=F_{X_{1}}\left(x_{1}\right) \cdots F_{X_{n}}\left(x_{n}\right), \quad \text { for all } \mathbf{x} \in \mathbb{R}^{n}
$$

### Definition (Pairwise independence for $$n \in \mathbb{N}, n>2$$ random variables)

We call the random variables $$X_{1}, \ldots, X_{n}$$ pairwise independent if

$$
F_{X_{i}, X_{j}}\left(x_{i}, x_{j}\right)=F_{X_{i}}\left(x_{i}\right) F_{X_{j}}\left(x_{j}\right), \quad \text { for all } x_{i}, x_{j} \in \mathbb{R} \text { whenever } i \neq j
$$

Definition(Independence of a family of random variables)
Let $$\mathcal{I} \subset \mathbb{R}$$ denote an index set. A family of random variables $$\left\{X_{i}: i \in \mathcal{I}\right\}$$ is said to be independent if for all finite subsets $$\mathcal{J} \subseteq \mathcal{I}$$ and all $$x_{j} \in \mathbb{R}, j \in \mathcal{J}$$, the following product rule holds:

$$
\mathrm{P}\left(\cap_{j \in \mathcal{J}}\left\{X_{j} \leq x_{j}\right\}\right)=\prod_{j \in \mathcal{J}} \mathrm{P}\left(X_{j} \leq x_{j}\right) .
$$

### Definition (Joint probability mass function for discrete random variables)

Definition 12.3.1 (Joint probability mass function). Let $$X, Y$$ denote discrete random variables on $$(\Omega, \mathcal{F}, \mathrm{P})$$. Their joint probability mass function denoted by $$p_{X, Y}$$ is defined as the function $$p_{X, Y}: \mathbb{R}^{2} \rightarrow[0,1]$$ given by

$$
p_{X, Y}(x, y)=\mathrm{P}(\{\omega \in \Omega: X(\omega)=x, Y(\omega)=y\})
$$

which is typically shortened to

$$
p_{X, Y}(x, y)=\mathrm{P}(X=x, Y=y)
$$

We have that $$p_{X, Y}(x, y) \geq 0$$ for all $$x, y \in \mathbb{R}$$ and $$\sum_{x} \sum_{y} p_{X, Y}(x, y)=1$$.

The marginal probability mass functions of $$X$$ and $$Y$$ are then given by

$$
p_{X}(x)=\sum_{y} p_{X, Y}(x, y), \quad \text { and } p_{Y}(y)=\sum_{x} p_{X, Y}(x, y)
$$

It turns out that for any "nice" set $$A \subseteq \mathbb{R}^{2}$$, we obtain that

$$
\mathrm{P}((X, Y) \in A)=\sum \sum_{(x, y) \in A} \mathrm{P}(X=x, Y=y)
$$

### Definition (Independence of discrete random variables)

Suppose that $$X$$ and $$Y$$ are discrete random variables on a probability space $$(\Omega, \mathcal{F}, \mathrm{P}) . X$$ and $$Y$$ are said to be independent if the pair of events $$\{\omega \in \Omega: X(\omega)=x\}$$ and $$\{\omega \in \Omega: Y(\omega)=y\}$$ are independent for all $$x, y \in \mathbb{R}$$, i.e. if

$$
\mathrm{P}(X=x, Y=y)=\mathrm{P}(X=x) \mathrm{P}(Y=y), \quad \text { for all } x, y \in \mathbb{R}
$$

Condition (12.3.1) is equivalent to saying that

$$
p_{X, Y}(x, y)=p_{X}(x) p_{Y}(y), \quad \text { for all } x, y \in \mathbb{R}
$$

### Definition (Continuous random vector)

We call the random vector $$(X, Y)$$ on $$(\Omega, \mathcal{F}, \mathrm{P})$$ (jointly) continuous if

$$
F_{X, Y}(x, y)=\int_{u=-\infty}^{x} \int_{v=-\infty}^{y} f_{X, Y}(u, v) d v d u
$$

for a function $$f_{X, Y}: \mathbb{R}^{2} \rightarrow \mathbb{R}$$ satisfying

(i) $$f_{X, Y}(u, v) \geq 0$$ for all $$u, v \in \mathbb{R}$$,

(ii) $$\int_{-\infty}^{\infty} \int_{-\infty}^{\infty} f_{X, Y}(u, v) d v d u=1$$.

We call $$f_{X, Y}$$ the (joint) density function of $$(X, Y)$$

$$
f_{X, Y}(x, y)= \begin{cases}\frac{\partial^{2}}{\partial x \partial y} F_{X, Y}(x, y), & \text { if this derivative exists at }(x, y) \\ 0, & \text { otherwise. }\end{cases}
$$

$$
\mathrm{P}((X, Y) \in A)=\iint_{(x, y) \in A} f_{X, Y}(x, y) d x d y
$$

$$
\begin{aligned}
f_{X}(x) & =\frac{d}{d x} F_{X}(x)=\frac{d}{d x} \int_{u=-\infty}^{x} \int_{v=-\infty}^{\infty} f_{X, Y}(u, v) d v d u \\
& =\int_{v=-\infty}^{\infty} f_{X, Y}(x, v) d v
\end{aligned}
$$

$$
f_{Y}(y)=\int_{u=-\infty}^{\infty} f_{X, Y}(u, y) d u
$$

### Definition (Independence of continuous random variables)

The jointly continuous random variables $$X$$ and $$Y$$ are independent if and only if their joint density factorises:

$$
f_{X, Y}(x, y)=f_{X}(x) f_{Y}(y), \quad \text { for all } x, y \in \mathbb{R}
$$

### Transformations of random vectors: the bivariate case

Consider the case of jointly continuous random variables $$(X, Y)$$ with density $$f_{X, Y}$$. Let $$u, v: \mathbb{R}^{2} \rightarrow \mathbb{R}$$ denote deterministic functions and define a new pair of random variables by

$$
U=u(X, Y), \quad V=v(X, Y)
$$

We would like to find the joint density of $$(U, V)$$

We define the mapping $$T: \mathbb{R}^{2} \rightarrow \mathbb{R}^{2}$$ by

$$
T(x, y)=(u(x, y), v(x, y))
$$

and assume that $$T$$ is a bijection from the domain $$D=\left\{(x, y): f_{X, Y}(x, y)>0\right\} \subseteq \mathbb{R}^{2}$$ to some range $$S \subseteq \mathbb{R}^{2}$$. Then we can write $$T^{-1}: S \rightarrow D$$ for the inverse mapping of $$T$$, i.e. $$(x, y)=T^{-1}(u, v)$$. For the first component we write $$x=x(u, v)$$ and for the second $$y=y(u, v)$$. The Jacobian determinant of $$T^{-1}$$ is defined as the determinant

$$
J(u, v)=\operatorname{det}\left(\begin{array}{cc}
\frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} \\
\frac{\partial y}{\partial u} & \frac{\partial y}{\partial v}
\end{array}\right)=\frac{\partial x}{\partial u} \frac{\partial y}{\partial v}-\frac{\partial x}{\partial v} \frac{\partial y}{\partial u}
$$

Then the joint density of $$(U, V)$$ is given by

$$
f_{U, V}(u, v)=\left\{\begin{array}{cc}
f_{X, Y}(x(u, v), y(u, v))|J(u, v)|, & \text { if }(u, v) \in S \\
0, & \text { otherwise. }
\end{array}\right.
$$

### Theorem (2D LOTUS: discrete case)

Let $$X, Y$$ denote discrete random variables on $$(\Omega, \mathcal{F}, \mathrm{P})$$ and let $$g: \mathbb{R}^{2} \rightarrow \mathbb{R}$$. Then $$Z=g(X, Y)$$ is also a discrete random variable on $$(\Omega, \mathcal{F}, \mathrm{P})$$ and its expectation is given by

$$
\mathrm{E}(g(X, Y))=\sum_{x \in \operatorname{Im} X} \sum_{y \in \operatorname{Im} Y} g(x, y) \mathrm{P}(X=x, Y=y)
$$

### Theorem (2D LOTUS: continuous case)

Let $$X, Y$$ be jointly continuous random variables with density $$f_{X, Y}$$ and let $$h: \mathbb{R}^{2} \rightarrow \mathbb{R}$$. Then

$$
\mathrm{E}[h(X, Y)]=\int_{-\infty}^{\infty} \int_{-\infty}^{\infty} h(x, y) f_{X, Y}(x, y) d x d y
$$

### Theorem (Linearity of expectation)

 Let $$X, Y$$ denote jointly discretelcontinuous random variables on $$(\Omega, \mathcal{F}, \mathrm{P})$$, and $$a, b \in \mathbb{R}$$, then

$$
\mathrm{E}(a X+b Y)=a \mathrm{E}(X)+b \mathrm{E}(Y)
$$

provided that $$\mathrm{E}(X)$$ and $$\mathrm{E}(Y)$$ exist.

### Definition (Covariance and correlation)

Consider two (one-dimensional) random variables $$X$$ and $$Y$$ on the same sample space with expectations $$\mu_{X}=\mathrm{E}(X)$$ and $$\mu_{Y}=\mathrm{E}(Y)$$. The covariance of $$X$$ and $$Y$$ is defined as

$$
\operatorname{Cov}(X, Y)=\mathrm{E}\left[\left(X-\mu_{X}\right)\left(Y-\mu_{Y}\right)\right]
$$

if the expectation on the right hand side takes a finite value. Also, we define the correlation of $$X$$ and $$Y$$ as

$$
\operatorname{Cor}(X, Y)=\frac{\operatorname{Cov}(X, Y)}{\sqrt{\operatorname{Var}(X) \operatorname{Var}(Y)}} .
$$

When we set $$X=Y$$, then the covariance simplifies to the variance:

$$
\operatorname{Cov}(X, X)=\mathrm{E}\left[\left(X-\mu_{X}\right)^{2}\right]=\operatorname{Var}(X)
$$

### Theorem (Covariance)

For jointly discrete/continuous random variables $$X, Y$$ with finite expectations, we have

$$
\operatorname{Cov}(X, Y)=\mathrm{E}(X Y)-\mathrm{E}(X) \mathrm{E}(Y)
$$

### Theorem (Disjoint and independent)

Let $$X, Y$$ denote independent and jointly discretelcontinuous random variables with finite expectation, then

$$
\mathrm{E}(X Y)=\mathrm{E}(X) \mathrm{E}(Y)
$$

### Remark

It is important to note that if $$\mathrm{E}(X Y)=\mathrm{E}(X) \mathrm{E}(Y)$$, then this does not in general imply that $$X$$ and $$Y$$ are independent.

The results stated in Theorem 12.7 .5 can be extended to the $$n \in \mathbb{N}$$ dimensional case by induction: If $$X_{1}, \ldots, X_{n}$$ are independent, then

$$
\mathrm{E}\left(X_{1} \cdots X_{n}\right)=\mathrm{E}\left(X_{1}\right) \cdots \mathrm{E}\left(X_{n}\right)
$$

### Theorem (Variance of a sum of random variables)

Let $$X, Y$$ denote two jointly discrete/continuous random variables with finite variances. Then

$$
\operatorname{Var}(X+Y)=\operatorname{Var}(X)+\operatorname{Var}(Y)+2 \operatorname{Cov}(X, Y)
$$

## 12 Generating functions

### Definition (Probability generating function (p.g.f.))

Then the probability generating function $$(p g f)$$ of $$X$$ is defined as the function $$G_{X}: \mathcal{S}_{X} \rightarrow \mathbb{R}$$ given by

$$
G_{X}(s)=\mathrm{E}\left(s^{X}\right)=\sum_{x=0}^{\infty} s^{x} \mathrm{P}(X=x) .
$$

### Theorem

Let $$X, Y$$ denote discrete random variables with $$\operatorname{Im} X, \operatorname{Im} Y \subseteq \mathbb{N} \cup\{0\}$$. Their p.g.f.s are denoted by $$G_{X}$$ and $$G_{Y}$$, respectively. Then

$$
G_{X}(s)=G_{Y}(s), \text { for all } s \in \mathcal{S}_{X} \cap \mathcal{S}_{Y}
$$

if and only if

$$
\mathrm{P}(X=x)=\mathrm{P}(Y=x), \text { for all } x=0,1,2, \ldots
$$

### Theorem

Let $$X, Y$$ be independent discrete random variables with $$\operatorname{Im} X, \operatorname{Im} Y \subseteq \mathbb{N} \cup\{0\}$$. Then

$$
G_{X+Y}(s)=G_{X}(s) G_{Y}(s), \text { for all } s \in \mathcal{S}_{X} \cap \mathcal{S}_{Y} .
$$

### Theorem

Let $$X$$ be a discrete random variable with $$\operatorname{Im} X \in \mathbb{N} \cup\{0\}$$. Let $$k \in \mathbb{N}$$. Then the kth derivative of the pgf is given by

$$
\left.\frac{d^{k}}{d s^{k}} G_{X}(s)\right|_{s=1}=G^{(k)}(1)=\mathrm{E}[X(X-1) \cdots(X-k+1)]
$$
Hence,
$$
\left.\frac{d}{d s} G_{X}(s)\right|_{s=1}=\mathrm{E}(X)
$$
$$
\operatorname{Var}(X)=\mathrm{E}\left(X^{2}\right)-[\mathrm{E}(X)]^{2}=G_{X}^{\prime \prime}(1)+G_{X}^{\prime}(1)-\left(G_{X}^{\prime}(1)\right)^{2}
$$

### Definition (Moment generating functions)

 Let $$X$$ be a random variable. Then its moment generating function (m.g.f.) is defined as

$$
M_{X}(t)=\mathrm{E}\left(e^{t X}\right)
$$

provided the expectation exists in some neighbourhood of zero, i.e. the expectation exists for

$$ 
\forall |t|<\epsilon 
$$ 

but for some $$\epsilon>0$$.

We compute the m.g.f. as follows:

$$
M_{X}(t)=\mathrm{E}\left(e^{t X}\right)= \begin{cases}\sum_{x} e^{t x} p_{X}(x), & \text { if } X \text { is discrete } \\ \int_{-\infty}^{\infty} e^{t x} f_{X}(x) d x, & \text { if } X \text { is continuous }\end{cases}
$$

whenever the sum/integral is (absolutely) convergent.

### Theorem

 If $$X$$ has a m.g.f., then for $$k \in \mathbb{N}$$, the kth moment of $$X$$ is given by

$$
\mathrm{E}\left(X^{k}\right)=M_{X}^{(k)}(0)=\left.\frac{d^{k}}{d t^{k}} M_{X}(t)\right|_{t=0}
$$

Proof. We give a sketch proof of the theorem. Assuming we can interchange expectation and differentiation, we write

$$
\frac{d^{k}}{d t^{k}} M_{X}(t)=\frac{d^{k}}{d t^{k}} \mathrm{E}\left(e^{t X}\right)=\mathrm{E}\left(\frac{d^{k}}{d t^{k}} e^{t X}\right)=\mathrm{E}\left(X^{k} e^{t X}\right)
$$

and then plug in $$t=0$$

### Theorem

For $$a, b \in \mathbb{R}$$, we have $$M_{a X+b}(t)=e^{b t} M_{X}(a t)$$.

### Theorem

Let $$X_{1}, \ldots, X_{n}$$ denote a sequence of independent random variables with m.g.f.s $$M_{X_{1}}, \ldots, M_{X_{n}}$$. Then

$$
M_{\sum_{i=1}^{n} X_{i}}(t)=\prod_{i=1}^{n} M_{X_{i}}(t)
$$

## 13 Conditional distribution and conditional expectation

### Definition (Conditional distribution and conditional expectation)

 Let $$X$$ denote a discrete random variable on the probability space $$(\Omega, \mathcal{F}, \mathrm{P})$$. Consider an event $$B \in \mathcal{F}$$ such that $$\mathrm{P}(B)>0$$. The conditional distribution of $$X$$ given $$B$$ is defined as

$$
\mathrm{P}(X=x \mid B)=\frac{\mathrm{P}(\{X=x\} \cap B)}{\mathrm{P}(B)}, \text { for } x \in \mathbb{R} .
$$

Further, the conditional expectation of $$X$$ given $$B$$ is defined as

$$
\mathrm{E}(X \mid B)=\sum_{x \in \operatorname{Im} X} x \mathrm{P}(X=x \mid B)
$$

### Theorem (Law of total expectation)

Consider a partition $$\left\{B_{i}: i \in \mathcal{I}\right\}$$ of $$\Omega$$ with $$\mathrm{P}\left(B_{i}\right)>0$$ for all $$i \in \mathcal{I}$$. Let $$X$$ denote a discrete random variable with finite expectation. Then

$$
\mathrm{E}(X)=\sum_{i \in \mathcal{I}} \mathrm{E}\left(X \mid B_{i}\right) \mathrm{P}\left(B_{i}\right)
$$

### Conditional expectation of jointly discrete random variables

Suppose $$(X, Y)$$ are jointly discrete random variables, the conditional distribution/probability mass function of $$Y$$ given $$X=x$$ is given by

$$
p_{Y \mid X}(y \mid x)=\mathrm{P}(Y=y \mid X=x)=\frac{p_{X, Y}(x, y)}{p_{X}(x)}, \quad \text { for } y \in \mathbb{R} .
$$

Also, the conditional expectation of $$Y$$ given $$X=x$$ is given by

$$
\mathrm{E}(Y \mid X=x)=\sum_{y} y p_{Y \mid X}(y \mid x)
$$

provided the sum is absolutely convergent.

Also, the LOTUS for conditional expectations says that

$$
\mathrm{E}(g(Y) \mid X=x)=\sum_{y} g(y) p_{Y \mid X}(y \mid x)
$$

Discrete $$X$$ and $$Y$$ are independent if and only if

$$
\mathrm{P}(Y=y \mid X=x)=\mathrm{P}(Y=y)
$$

for all $$x, y$$ such that $$\mathrm{P}(X=x)>0$$.
Also, we get a Bayes' type result of the form
$$
p_{Y \mid X}(y \mid x) p_{X}(x)=p_{X, Y}(x, y)=p_{X \mid Y}(x \mid y) p_{Y}(y)
$$

for all $$x, y$$ for which $$p_{X}(x), p_{Y}(y)>0$$.

### Conditional expectation of jointly continuous random variables

### Definition (Conditional distribution and conditional density)

For two jointly continuous random variables $$X, Y$$, we define the conditional density of $$Y$$ given $$X=x$$ as

$$
f_{Y \mid X}(y \mid x)=\frac{f_{X, Y}(x, y)}{f_{X}(x)}
$$

for all $$y \in \mathbb{R}$$ and for all $$x \in \mathbb{R}$$ for which $$f_{X}(x)>0$$. The corresponding conditional distribution function of $$Y$$ given $$X=x$$ is then given by

$$
F_{Y \mid X=x}(y \mid x)=\frac{\int_{\infty}^{y} f_{X, Y}(x, v) d v}{f_{X}(x)}
$$

for all $$y \in \mathbb{R}$$ and for all $$x \in \mathbb{R}$$ for which $$f_{X}(x)>0$$.

Jointly continuous random variables $$X$$ and $$Y$$ are independent if and only if

$$
f_{Y \mid X}(y \mid x)=f_{Y}(y)
$$

for all $$x, y$$ such that $$f_{X}(x)>0$$.

Also, we get a Bayes' type result of the form
$$
f_{Y \mid X}(y \mid x) f_{X}(x)=f_{X, Y}(x, y)=f_{X \mid Y}(x \mid y) f_{Y}(y)
$$

### Proposition

Let $$(X, Y)$$ be two jointly continuous random variables with joint probability density function $$f_{X, Y}$$ and marginal probability densities denoted by $$f_{X}$$ and $$f_{Y}$$, respectively. Let $$F_{Y \mid X=x}$$ denote the conditional distribution function of $$Y$$ given $$X=x$$. Then

$$
\mathrm{P}(Y \leq y)=\int_{\left\{x: f_{X}(x)>0\right\}} F_{Y \mid X=x}(y \mid x) f_{X}(x) d x, \quad y \in \mathbb{R} .
$$

### Definition (Conditional expectation)

For two jointly continuous random variables $$X$$, $$Y$$, we define the conditional expectation of $$Y$$ given $$X=x$$ as

$$
\mathrm{E}(Y \mid X=x)=\int_{-\infty}^{\infty} y f_{Y \mid X}(y \mid x) d y=\int_{-\infty}^{\infty} y \frac{f_{X, Y}(x, y)}{f_{X}(x)} d y
$$

provided that $$f_{X}(x)>0$$

### Theorem (Law of total expectation)

 For jointly continuous random variable $$X, Y$$ with $$\mathrm{E}|Y|<\infty$$, we have

$$
\mathrm{E}(Y)=\int_{\left\{x: f_{X}(x)>0\right\}} \mathrm{E}(Y \mid X=x) f_{X}(x) d x .
$$
