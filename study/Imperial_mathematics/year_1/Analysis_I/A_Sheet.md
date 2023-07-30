---
layout: simple
title: Analysis I Memory Sheet
---

#### Based on the notes and lectures of [Prof. Richard Thomas](https://www.ma.imperial.ac.uk/~rpwt/?_gl=1*4lska7*_ga*NTkyNDQ0MjkxLjE2OTA0NTE4MjA.*_ga_LME5ZDDFS0*MTY5MDcxMTMzNS4yNS4wLjE2OTA3MTEzMzUuNjAuMC4w), [Dr. Ajay Chandra](https://sites.google.com/view/ajaychandra/home) and [Dr. Marco Guaraco](https://www.imperial.ac.uk/people/guaraco).

## 1. Logic

#### Definition 1.1 (Injective)

A function $$f: A \rightarrow B$$ is injective if for all $$a_1, a_2 \in A$$, $$f(a_1) = f(a_2)$$ implies $$a_1 = a_2$$.

#### Definition 1.2 (Surjective)

A function $$f: A \rightarrow B$$ is surjective if for all $$b \in B$$, there exists $$a \in A$$ such that $$f(a) = b$$.

#### Definition 1.3 (Bijective)

A function $$f: A \rightarrow B$$ is bijective if it is both injective and surjective.

## 2. Numbers

### 2.1 Rational numbers

#### Axioms 2.1

1. $$a+b = b+a$$
2. $$a \times b = b \times a$$
3. $$a + (b + c) = (a + b) + c$$
4. $$a \times (b \times c) = (a \times b) \times c$$
5. $$a \times (b + c) = a \times b + a \times c$$
6. $$\exist 0 \in \mathbb{Q}: a+0 = a$$
7. $$\exist 1 \in \mathbb{Q}: 0 \neq 1, a \times 1 = a$$
8. $$\forall a \in \mathbb{Q}, \exist (-a) \in \mathbb{Q}$$ such that $$a+(-a) = 0$$
9. $$\forall a \in \mathbb{Q} \backslash\{0\} \exists a^{-1} \in \mathbb{Q}$$ such that $$a \times\left(a^{-1}\right)=1$$

#### Axioms 2.2

1. for each $$x \in \mathbb{Q}$$ precisely one of (a), (b), (c) holds:
(a) $$x>0$$ or (b) $$x=0$$ or (c) $$-x>0$$  (Trichotomy axiom)
1. $$x>0, y>0 \Longrightarrow x+y>0 \quad \forall x, y \in \mathbb{Q}$$
2. $$x>0, y>0 \Longrightarrow x y>0 \quad \forall x, y \in \mathbb{Q}$$
3. $$\forall x \in \mathbb{Q} \exists n \in \mathbb{N}$$ such that $$n>x$$ (Archimedean axiom)

### 2.2 Decimals

#### Theorem 2.8

Any $$x \in \mathbb{Q}$$ is equal to an eventually periodic decimal expansion:

$$x=a_{0} . a_{1} \ldots a_{i} \overline{a_{i+1} a_{i+2} \ldots a_{j}} \quad\left(a_{0} \in \mathbb{Z}, a_{\ell} \in\{0,1, \ldots, 9\}\right.$$ for $$\left.\ell \geq 1\right)$$.

#### Proposition 2.14

If $$x \in \mathbb{Q}$$ has two different decimal expansions then they are of the form

$$
\begin{aligned}
x & =a_{0} \cdot a_{1} a_{2} \ldots a_{n} \overline{9} \\
& =a_{0} \cdot a_{1} a_{2} \ldots\left(a_{n}+1\right) \quad \text { with } a_{n} \in\{0,1, \ldots, 8\} .
\end{aligned}
$$

#### Definiton 2.1 (Arbitrary decimals: the real numbers)

$$\mathbb{R}:=\left\{a_{0} \cdot a_{1} a_{2} \ldots: a_{0} \in \mathbb{Z}, a_{i \geq 1} \in\{0,1, \ldots, 9\}, \nexists N\right.$$ such that $$\left.a_{i}=9 \forall i \geq N\right\}$$

### 2.3 Countability

#### Definition 2.1 (Countable set)

A set $$S$$ is countably infinite if and only if there exists a bijection $$f: \mathbb{N}_{>0} \rightarrow S$$

A set that is finite, or countably infinite, is said to be countable.

#### Proposition 2.16

Suppose $$S \subset \mathbb{N}$$ is infinite. Then $$S$$ is countably infinite. (The subset of $$\mathbb{N}$$ is at most countable.)
In fact, any subset of a countable set is at most countable.

#### Proposition 2.17

$$\mathbb{Z}$$ is countable infinite.

![](https://cdn.mathpix.com/cropped/2023_05_01_eeb01ef285d7843830f2g-13.jpg?height=206&width=948&top_left_y=2230&top_left_x=540)
Proof : Formally, define a bijection $$f: \mathbb{N} \rightarrow \mathbb{Z}$$ by declaring, for $$k \geq 1$$,

$$
f(2 k-1)  :=-(k-1), \quad
f(2 k)  :=k
$$

#### Exercise 2.18

$$A, B$$ countable $$\Longrightarrow A \cup B$$ countable.

#### Theorem 2.19

$$\mathbb{Q}$$ is countable.

#### Theorem 2.21

$$\mathbb{R}$$ is uncountable.

Proof : (Cantor's Diagonal Argument)

### 2.4 The Completeness Axiom

#### Definition (Upper bound and lower bound)

$$\emptyset \neq S \subset \mathbb{R}$$ is bounded above if and only if

$$
\exists M \in \mathbb{R} \text { such that } \forall x \in S, x \leq M
$$

Such an $$M$$ is called an upper bound for $$S$$.
$$S$$ is bounded below if and only if

$$
\exists M \in \mathbb{R} \text { such that } \forall x \in S, M \leq x
$$

Such an $$M$$ is called a lower bound.
$$S$$ is bounded if and only if $$S$$ is bounded above and below.

#### Exercise 2.24

$$S$$ is bounded if and only if

$$
\exists R>0 \text { such that } \forall x \in S,-R \leq x \leq R
$$

or equivalently

$$
\exists R>0 \text { such that } \forall x \in S,|x| \leq R
$$

#### Definition (Supremum and infimum)

Suppose $$\emptyset \neq S \subset \mathbb{R}$$ is bounded above. We say $$x \in \mathbb{R}$$ is a least upper bound of $$S$$ or supremum of $$S$$ if and only if

- $$x$$ is an upper bound for $$S$$ (i.e. $$x \geq s \forall s \in S$$), and

- $$x \leq y$$ for any $$y$$ which is an upper bound for $$S(y \geq s \forall s \in S \Longrightarrow x \leq y)$$.

#### Theorem 2.31 (Completeness Axiom of $$\mathbb{R}$$)

Suppose $$\emptyset \neq S \subset \mathbb{R}$$ is bounded above. Then $$S$$ has a supremum.

Therefore, for any $$S \subset \mathbb{R}$$, if $$S$$ is bounded, then $$\sup S$$ and $$\inf S$$exists. Furthermore, $$\sup S$$ and $$\inf S$$ are unique. Besides, we can always find a sequence in $$S$$ converging to $$\sup S$$ or $$\inf S$$.

#### Proposition 2.38

 Suppose $$\emptyset \neq S \subset \mathbb{R}$$ and $$y$$ is an upper bound for $$S$$.

Then $$y=\sup S \Longleftrightarrow \forall \epsilon>0 \exists s \in S: s>y-\epsilon$$.

### 2.5 Dedekind cuts

#### Definition (Dedekind cut)

We say a nonempty subset $$S \subset \mathbb{Q}$$ is a Dedekind cut if it satisfies (i) and (ii) below.

(i) If $$s \in S$$ and $$s>t \in \mathbb{Q}$$ then $$t \in S$$ ($$S$$ is a semi-infinite interval to the left).

(ii) $$S$$ is bounded above but has no maximum.

#### Definition ($$\mathbb{R}$$ as Dedekind cuts)

$$
\mathbb{R}:=\{\text { Dedekind cuts } S \subset \mathbb{Q}\}
$$

### 2.6 Triangle inequalities

##### Theorem 2.44 (Triangle inequalities)

For all $$a, b \in \mathbb{R}$$ we have

$$
|a+b| \leq|a|+|b|
$$

$$ 
|x+y| \leq|x|+|y| 
$$

$$
|x| \leq|y|+|x-y| 
$$

$$
|x+y| \geq|x|-|y| 
$$

$$
|x| \geq|y|-|x-y|
$$

$$
|x+y| \geq|y|-|x|
$$

$$
|x-y| \leq|x-z|+|y-z|
$$

$$
|x-y| \geq|| x|-| y||$$

#### Exercise 2.46

$$
\forall \epsilon>0,|x-a|<\epsilon
$$

is equivalent to

$$
x = a
$$

## 3 Sequences

#### Definition (Sequence)

Definition. A sequence is a function $$a: \mathbb{N}_{>0} \rightarrow \mathbb{R}$$

#### Exercise 3.2

Any sequence $$\left(a_{n}\right)$$ can be written as a series $$a_{n}=\sum_{i=1}^{n} b_{i}$$  for an appropriate choice of sequence $$\left(b_{n}\right)$$.

### 3.1 Convergence of Sequences

We say that $$a_{n} \rightarrow a$$ as $$n \rightarrow \infty$$ if and only if

$$
\forall \epsilon>0 \exists N \in \mathbb{N} \text { such that } \forall n \geq N,\left|a_{n}-a\right|<\epsilon
$$

#### Remark 3.5

$$N$$ depends on $$\epsilon$$ ! For a while we will sometimes denote it $$N_{\epsilon}$$, as a reminder.

#### How to prove $$a_{n} \rightarrow a$$

$$
\forall \epsilon>0 \exists N_{\epsilon} \in \mathbb{N}_{>0} \text { such that }\left|a_{n}-a\right|<\epsilon \forall n \geq N
$$

(I) Fix $$\epsilon>0$$.

(II) Calculate

$$ 
|a_n - a| 
$$

(II') Find a good estimate of 

$$
|a_{n}-a| \leq b_{n}
$$

(III) Try to solve $$b_{n}<\epsilon$$

(IV) Find $$N_{\epsilon} \in \mathbb{N}_{>0}$$ such that $$(*)$$ holds whenever $$n \geq N_{\epsilon}$$.

(V) Put everything together into a logical proof.

#### Definition （ Convergence ）

We say that $$a_{n}$$ converges if and only if $$\exists a \in \mathbb{R}$$ such that $$ a_{n} \Longrightarrow a $$, i.e.

$$
\exists a \text{ such that } \forall \epsilon>0 \exists N \in \mathbb{N}_{>0} \text{ such that } n \geq N \rightarrow |a_{n}-a|<\epsilon
$$

#### Definition （ Divergence ）

We say that $$a_{n}$$ diverges if and only if $$a_{n}$$ does not converge(to any $$a \in \mathbb{R}$$),i.e.

$$
\forall a \exists \epsilon>0 \text { such that } \forall N \in \mathbb{N}_{>0}, \exists n \geq N \text { such that }\left|a_{n}-a\right| \geq \epsilon
$$

#### Definition （ Convergence for complex sequences ）

$$ a_{n} \in \mathbb{C}, \forall n \geq 1 $$. We say $$ a_n \to a \in \mathbb{C} $$ if and only if

$$
\forall \epsilon>0, \exists N \in \mathbb{N}_{>0} \text{ such that }  n \geq N \Longrightarrow |a_{n}-a|<\epsilon 
$$

##### Theorem 3.14 (Uniqueness of limits)

Limits are unique. If $$a_{n} \rightarrow a$$ and $$a_{n} \rightarrow b$$, then $$a=b$$

#### Propositon 3.16 (Convergent sequence must be bounded)

If $$\left(a_{n}\right)$$ is convergent, then it is bounded.

#### Theorem 3.19 (Algebra of limits)

If $$a_{n} \rightarrow a$$ and $$b_{n} \rightarrow b$$ then:

 - $$a_{n}+b_{n} \rightarrow a+b$$

 - $$a_{n} b_{n} \rightarrow a b$$

 - $$\frac{a_{n}}{b_n} \rightarrow \frac{a}{b}$$ if $$b \neq 0$$

#### Theorem 3.21 (Bounded and monotonic sequences must be convergent)

If $$\left(a_{n}\right)$$ is bounded above and monotonically increasing then $$a_{n}$$ converges to $$a:=\sup \left\{a_{i}: i \in \mathbb{N}_{>0}\right\}$$. We write $$a_{n} \uparrow a$$.

#### Example 3.22

Suppose that $$\left(a_{n}\right)$$ and $$\left(b_{n}\right)$$ are sequences of real numbers such that $$a_{n} \leq b_{n} \forall n$$ and $$a_{n} \rightarrow a, b_{n} \rightarrow b$$, then $$a \leq b$$.

#### Example 3.23

If

$$
\left|\frac{a_{n+1}}{a_{n}}\right| \rightarrow L<1
$$

then $$a_{n} \rightarrow 0$$

### 3.2 Cauchy Sequences

#### Definition (Cauchy sequence)

$$\left(a_{n}\right)_{n \geq 1}$$ is called a Cauchy sequence if and only if

$$
\forall \epsilon>0 \exists N \in \mathbb{N}_{>0} \text { such that } \forall n, m \geq N,\left|a_{n}-a_{m}\right|<\epsilon
$$

#### Proposition 3.25

If $$a_{n} \rightarrow$$ a then $$\left(a_{n}\right)$$ is Cauchy.

#### Lemma 3.26 (Cauchy sequences are bounded)

$$\left(a_{n}\right)$$ is Cauchy $$\Longrightarrow\left(a_{n}\right)$$ is bounded.

#### Theorem 3.27 (Cauchy sequences converge)

If $$\left(a_{n}\right)$$ is a Cauchy sequence of real numbers then $$a_{n}$$ converges.
It is not ture in $$\mathbb{Q}$$: there i s a Cauchy sequence $$(a_n)$$ with $$a_n \ in \mathbb{Q}$$ with no limit in $$\mathbb{Q}$$
Therefore, we can regard every real numbers as a limit of a Cauchy sequence of rational numbers.

#### Corollary 3.28

$$\left(a_{n}\right)$$ Cauchy $$\Longleftrightarrow\left(a_{n}\right)$$ convergent.

### 3.3 Subsequences

#### Definition (Subsequence)

A subsequence of $$\left(a_{n}\right)$$ is a new sequence $$b_{i}=a_{n(i)} \forall i \in \mathbb{N}_{>0}$$, where  $$n(1)<n(2)<\cdots<n(i)<\ldots \forall i$$.

Formally $$n(\cdot)$$ is a function $$\mathbb{N}_{>0} \rightarrow \mathbb{N}_{>0}$$ sending $$i \mapsto n(i)$$ which is strictly monotonically increasing.

#### Theorem 3.34 (Bolzano-Weierstrass)

If $$\left(a_{n}\right)$$ is a bounded sequence of real numbers then it has a convergent subsequence.

#### Proposition 3.39

If $$a_{n} \rightarrow a$$ then any subsequence $$a_{n(i)} \rightarrow a$$ as $$i \rightarrow \infty$$.

#### Lemma 3.40

Fix $$c>0$$. Then $$a_{n} \rightarrow a$$ if and only if 

$$
\forall \epsilon>0 \exists N_{\epsilon} \in \mathbb{N}_{>0} \text { such that } n \geq N_{\epsilon} \Longrightarrow\left|a_{n}-a\right|<c \epsilon
$$

#### Definition (Convergent to $$\pm \infty$$)

We say $$a_{n} \rightarrow+\infty$$ if and only if

$$
\forall R>0 \exists N \in \mathbb{N} \text { such that } a_{n}>R \forall n \geq N
$$

#### Exercise 3.42

Suppose $$a_{n}>0 \forall n$$.$$a_{n} \rightarrow 0 \Longleftrightarrow \frac{1}{a_{n}} \rightarrow+\infty$$.

## 4 Series

#### Definition (Series)

An (infinite) series is an expression

$$
\sum_{n=1}^{\infty} a_{n} \quad \text { or } a_{1}+a_{2}+a_{3}+\ldots
$$

where $$\left(a_{i}\right)_{i \geq 1}$$ is a sequence.

#### Definition (Partial sum)

Given a sequence $$a_{n}$$ we get a series (formal expression!) $$\sum_{n=1}^{\infty} a_{n}$$ and another sequence of partial sums

$$
s_{n}:=\sum_{i=1}^{n} a_{i}
$$

### 4.1 Convergence of Series

#### Definition (Convergence of series)

We say that the series $$\sum a_{n}$$ "converges to $$A \in \mathbb{R}$$ " if and only if the sequence of partial sums converges to $$A$$ :

$$
\sum_{n=1}^{\infty} a_{n}=A \Longleftrightarrow s_{n} \longrightarrow A .
$$

#### Theorem 4.2 (Convergence of series implies convergence of sequence)

$$
\sum_{n=0}^{\infty} a_{n} \text { is convergent } \Longrightarrow a_{n} \rightarrow 0
$$


#### Proposition 4.6

Suppose $$a_{n} \geq 0 \forall n\left(\Longleftrightarrow s_{n}=\sum_{i=1}^{n} a_{i}\right.$$ is monotonically increasing), Then the following two facts are true:

1. $$\sum_{n=1}^{\infty} a_{n}$$ converges if and only if $$\left(s_{n}\right)$$ is bounded above.

2. Similarly $$\sum_{n=1}^{\infty} a_{n}$$ diverges to $$+\infty$$ (i.e. $$\forall M>0 \exists N \in \mathbb{N}$$ such that $$s_{n}>$$ $$M \forall n \geq N)$$ if and only if $$\left(s_{n}\right)$$ is unbounded.

#### Theorem 4.7 (Comparison test)

If $$0 \leq a_{n} \leq b_{n}$$ and $$\sum b_{n}$$ converges, then $$\sum a_{n}$$ converges.

Moreover, $$0 \leq \sum_{n=1}^{\infty} a_{n} \leq \sum_{n=1}^{\infty} b_{n}$$.

 (Converse of Comparison Test.). If $$0 \leq a_{n} \leq b_{n}$$ then $$\sum a_{n}$$ diverges to $$+\infty \Longrightarrow \sum b_{n}$$ diverges to $$+\infty$$

#### Theorem 4.11 (Algebra of limits for series)

 If $$\sum a_{n}, \sum b_{n}$$ are convergent then so is $$\sum\left(\lambda a_{n}+\mu b_{n}\right)$$, to

$$
\sum_{n=1}^{\infty}\left(\lambda a_{n}+\mu b_{n}\right)=\lambda \sum_{n=1}^{\infty} a_{n}+\mu \sum_{n=1}^{\infty} b_{n}
$$

### 4.2 Absolute Convergence

#### Definition (Absolute convergence)

For $$ a_{n} \in \mathbb{R} $$ or $$ \mathbb{C} $$, we say the series $$ \sum_{n=1}^{\infty} a_{n} $$ is absolutely convergent if and only if the series 

$$ 
\sum_{n=1}^{\infty}|a_n|
$$

is convergent.

#### Definition

For $$a_{n} \in \mathbb{R}$$ or $$\mathbb{C}$$, we say the series $$\sum_{n=1}^{\infty} a_{n}$$ is conditionally convergent if and only if the series 

$$
\sum_{n=1}^{\infty} a_n
$$

is convergent but it is not absolutely convergent.

#### Theorem 4.14 (Absolute convergence implies convergence)

Let $$\{a_{n}_{n \geq 0}\}$$ be a real or complex sequence. If $$\sum a_n $$ is absolutely convergent, then it is convergent.

### 4.3 Test for convergence

#### Theorem 4.16 (Comparison test II: Sandwich Test)

Suppose $$c_{n} \leq a_{n} \leq b_{n} \forall n$$ and $$\sum c_{n}, \quad \sum b_{n}$$ are both convergent.

Then $$\sum a_{n}$$ is convergent.

#### Theorem 4.17 (Comparison test III: Limit test)

If $$\frac{a_{n}}{b_{n}} \rightarrow L \in \mathbb{R}$$ and $$\sum b_{n}$$ is absolutely convergent, then $$\sum a_{n}$$ is absolutely convergent.

#### Exercise 4.19

Fix $$N \in \mathbb{N}_{>0}$$. Then $$\sum_{n \geq N} c_{n}$$ is convergent if and only if $$\sum_{n \geq 1} c_{n}$$ is convergent.

#### Theorem 4.20 (Alternating series test)

Suppose $$ a_n $$ is alternating with

$$ 
|a_n| \to 0
$$

motonically. Then $$ \sum a_{n} $$ converges.

#### Exercise 4.22

The alternating sequence $$a_{n}=\left\{\begin{array}{cc}\frac{1}{n^{2}}+\frac{1}{n} & n \text { even, } \\ -\frac{1}{n^{2}} & n \text { odd, }\end{array}\right.$$ has sum $$\sum a_{n}$$ which is divergent to $$+\infty$$.
It is alternating but $$\left|a_{n}\right|$$ is not monotonically decreasing, so the alternating series test does not apply.

#### Theorem 4.23 (Ratio test)

If $$ a_n $$ is a sequence such that 

$$
|\frac{a_{n+1}}{a_n}| \rightarrow r<1
$$

then $$ \sum a_{n} $$ is absolutely convergent.

#### Theorem 4.24 (Root test)

If 

$$
|a_n|^{\frac{1}{n}} \rightarrow r<1
$$

then $$ \sum a_n $$ is absolutely convergent.

### 4.4 Rearrangement of Series

#### Definition(Rearrangement of a sequence) 

Given a bijection $$n: \mathbb{N}_{>0} \rightarrow \mathbb{N}_{>0}$$, define $$b_{i}:=a_{n(i)}$$. Then $$\left(b_{i}\right)_{i \geq 1}$$ is a rearrangement or reordering of $$\left(a_{n}\right)_{n \geq 1}$$.

#### Example 4.31

Rearrange $$\sum \frac{(-1)^{n+1}}{n}$$ to make it converge to your favourite number.

Pick your favourite number; call it $$\pi$$ say. Then reorder the sum as follows.

1. Take only odd terms $$a_{2 n+1}>0$$ until their sum is $$>\pi$$. We can do this as $$1+\frac{1}{3}+\ldots$$ diverges to $$\infty$$ !

2. Now take only even terms $$a_{2 n}<0$$ until sum gets $$<\pi$$.

3. Repeat 1 and 2 to fade.

We can do each step because $$\sum a_{2 n+1} \rightarrow+\infty$$ and $$\sum a_{2 n} \rightarrow-\infty$$.
Finally we sketch the proof that this reordered sum converges to $$\pi$$. Since $$a_{n} \rightarrow 0$$,

$$
\forall \epsilon>0 \exists N \in \mathbb{N}_{>0} \text { such that } n \geq N \Longrightarrow\left|a_{n}\right|<\epsilon
$$

Then the method of Example 4.31 shows that if $$\left(a_{n}\right)$$ is any sequence such that

- $$a_{n} \rightarrow 0$$

- $$\sum_{n: a_{n} \geq 0} a_{n} \rightarrow+\infty$$

- $$\sum_{n: a_{n}<0} a_{n} \rightarrow-\infty$$
then we can rearrange the series $$\sum a_{n}$$ to make it converge to any real number we like by the algorithm above.

#### Exercise 4.33

If $$\left(a_{n}\right)$$ is a sequence such that

- $$a_{n} \rightarrow 0$$

- $$\sum_{n: a_{n} \geq 0} a_{n} \rightarrow+\infty$$

- $$\sum_{n: a_{n}<0} a_{n}$$ converges,
then any reordering of $$\sum a_{n}$$ will diverge to $$+\infty$$.

#### Theorem 4.34 (Riemann's Rearrangement Theorem)

$$\sum a_{n}$$ is absolutely convergent $$\Longleftrightarrow(1)+(2) \Longrightarrow(3)+(4)$$, where

(1) $$\sum_{a_{n} \geq 0} a_{n}$$ is convergent (to $$A$$ say),

(2) $$\sum_{a_{n}<0} a_{n}$$ is convergent (to $$B$$ say),

(3) $$\sum a_{n}=A+B$$

(4) $$\sum b_{m}=A+B$$ where $$\left(b_{m}\right)$$ is any rearrangement of $$\left(a_{n}\right)$$.

### 4.5 Power Series

#### Theorem 4.35 (Radius of convergence)

Let $$[0, \infty]$$ denote the set $$ [0, \infty) \cup\{+\infty\} $$,
Fix a real or complex series $$\left(a_{n}\right)$$ and consider the series $$\sum a_{n} z^{n}$$ for $$z \in \mathbb{C}$$.

Then $$\exists R \in[0, \infty]$$ such that

  - $$ 
|z|<R \rightarrow \sum a_{n} z^{n}
$$ 

is absolutely convergent, and

  - $$
|z|>R \rightarrow \sum a_{n} z^{n}
$$

is divergent.
  
Proof. Let

$$
S=\{|z|: a_{n} z^{n} \rightarrow 0\}
$$

nonempty since $$0 \in S $$. Then define

$$
R= \begin{cases}\sup S & \text { if } S \text { bounded }, \\ \infty & \text { if } S \text { unbounded }\end{cases}
$$


### 4.5.1 Products of Power Series

#### Definition  (Cauchy product)

Given series $$\sum a_{n}, \sum b_{n}$$ their Cauchy Product is the series $$\sum c_{n}$$ where $$c_{n}:=\sum_{i=0}^{n} a_{i} b_{n-i}$$.

#### Theorem 4.39 (Cauchy product of power series)

If $$\sum a_{n}, \sum b_{n}$$ are absolutely convergent, then their Cauchy product $$\sum c_{n}$$ is  absolutely convergent to $$\left(\sum a_{n}\right) \cdot\left(\sum b_{n}\right)$$.

#### Corollary 4.40

If $$\sum a_{n} z^{n}$$ and $$\sum b_{n} z^{n}$$ have radius of convergence $$R_{A}$$ and $$R_{B}$$ respectively, then $$\sum c_{n} z^{n}$$ has radius of convergence $$R_{C} \geq \min \left\{R_{A}, R_{B}\right\}$$.

#### Exercise 4.41

Fix $$\alpha, \beta \in \mathbb{R}$$. Prove that if $$[x<\alpha \Longrightarrow x \leq \beta]$$ then $$\alpha \leq \beta$$.

## 5. Continuity

### 5.1 Limits

#### Definition (Limit of a function)

Given $$a<x_0<b$$ and $$f:(a,b)-\{x_0\} \rightarrow \mathbb{R}$$, we define

$$
\lim _{x \rightarrow x_{0}} f(x)=y \leftrightarrow \forall \epsilon>0 \exists \delta>0 \text { such that } 0<|x-x_{0}|<\delta \rightarrow|f(x)-y|<\epsilon
$$


#### Proposition (Limits keep sign)

If $$\lim _{x \to x_0} f(x) = y > 0$$, then there exists $$\delta > 0$$, such that $$x \in (x_0-\delta, x_0+\delta)-\{x_0\}$$ such that $$f(x) > 0$$.

#### Proposition (Limits mean bounded)

If $$\lim_{x \to x_0} f(x)$$ exists then there is an open interval $$I$$ containing $$x_0$$ such that $$f$$ is bounded in $$I-\{x_0\}$$.

#### Proposition (Uniqueness of limits)

If $$\lim _{x \to x_0} f(x) = a$$ and $$\lim_{x \to x_0} f(x) = b$$, then $$a = b$$.

#### Proposition (Squeeze theorem)

Let $$f, g$$ and $$h$$ be functions defined on
$$
(a, b)-\{x_{0}\}
$$
where $$a<x_{0}<b$$. Assume for all $$x \in (a,b)-\{x_0\}$$
$$
f(x) \leq g(x) \leq h(x)
$$
If the limits $$\lim_{x \to x_0} f(x)$$ and $$\lim{ x \to x_0} h(x)$$ exist and coincide, then $$\lim_{x \to x_0} g(x)$$ exists and
$$
\lim _{x \to x_0} f(x)=\lim_{x \to x_0} g(x)=\lim _{x \to x_0} h(x)
$$

#### Exercise (Limits of functions and sequences)

- $$\lim_{n \ to infty} x_n = x$$ if and only if for every open interval $$I \subset \mathbb{R}$$ containing $$x$$, the sequence $$x_n$$ is eventually contained in $$I$$.
- $$\lim {x \to x_0} f(x) = y$$ if and only if for every sequence $$x_n \in \mathbb{R}-\{x_0\}$$ such that $$x_n \to x_0$$ we also have $$f(x_n) \to y$$.

#### Proposition (Algebra of function limits)

- $$\lim_{x \to x_0} (f(x) + g(x)) = \lim_{x \to x_0} f(x) + \lim_{x \to x_0} g(x)$$
- $$\lim_{x \to x_0} (f(x) \cdot g(x)) = \lim_{x \to x_0} f(x) \cdot \lim_{x \to x_0} g(x)$$
- If $$\lim_{x \to x_0} {g(x)} \neq 0$$, then
 $$
 \lim_{x \to x_0}\frac{f(x)}{g(x)} = \frac{\lim_{x \to x_0}f(x)}{\lim_{x \to x_0}g(x)}
 $$.

### 5.2 Continuity

#### Definition (Continuous at a point)

We say that $$f: I \rightarrow \mathbb{R} $$ is continuous at $$x_0$$ if continous at $$a \in I$$ if
$$
\lim _{x \to a} f(x)=f(a)
$$

#### Theorem (Algebra of continuous functions)

If $$f, g: I \to \mathbb{R}$$ are continuous at $$a \in I$$, then

- $$f + g$$ is continuous at $$a$$.
- $$f \cdot g$$ is continuous at $$a$$.
- If $$g(a) \neq 0$$, then $$\frac{f}{g}$$ is continuous at $$a$$.
  
#### Theorem (Composition of continuous functions)

If $$g$$ is continous at $$a$$ and $$f$$ is continous at $$g(a)$$, then $$f \circ g$$ is continuous at $$a$$.

#### Theorem (Intermediate value theorem)

Let $$f: [a, b] \to \mathbb{R}$$ be continuous at every point of the closed interval $$[a,b]$$, then $$f$$ attains all the value between $$f(a)$$ and $$f(b)$$.
Let $$f: [a, b] \to \mathbb{R}$$ be continuous at every point of the closed interval $$[a,b]$$, then for every $$y$$ between $$f(a)$$ and $$f(b)$$, there exists $$x \in [a,b]$$ such that $$f(x) = y$$.

#### Theorem (Extreme value theorem)

Let $$f: [a, b] \to \mathbb{R}$$ be continuous at every point of the closed interval $$[a,b]$$, then $$f$$ attains a maximum and a minimum on $$[a,b]$$.

#### Exercise (Continuity keeps sign)

If $$f$$ is continous at $$a$$ and $$f(a) > 0$$, then $$f(x)>0$$ for all $$x$$ close to $$a$$.
Let $$f: I \to \mathbb{R}$$ be continuous at $$a \in I$$. If $$f(a) > 0$$, then there exists $$\delta > 0$$ such that $$f(x) > 0$$ for all $$x \in (a-\delta, a+\delta) \cap I$$.

#### Definition (Right and left limits)

We say that $$ f(x)$$ tends to $$L$$ as $$x$$ approaches $$a$$ from the right if


$$
\lim _{x \to a^{+}} f(x)=L
$$

Similarly, we say that $$f(x)$$ tends to $$L$$ as $$x$$ approaches $$a$$ from the left if


$$
\lim _{x \to a^{-}} f(x)=L
$$

#### Definition (Continuity on closed intervals)

We say that $$f: [a, b] \to \mathbb{R}$$ is continuous on $$[a,b]$$ if

- $$\lim_{x \to t} f(x) = f(t)$$,  $$\forall t \in (a,b)$$
- $$\lim_{x \to a^{+}} f(x) = f(a)$$
- $$\lim_{x \to b^{-}} f(x) = f(b)$$

#### Theorem (Bolzano's theorem)

Let $$f: [a, b] \to \mathbb{R}$$ be continuous on $$[a,b]$$ and assume
$$
f(a)<0<f(b)
$$
Then there exists $$x \in (a,b)$$ such that $$f(x) = 0$$.

#### Corollary (Intermediate value theorem)

Let $$f: [a, b] \to \mathbb{R}$$ be continuous on $$[a,b]$$ and assume $$f(a) < f(b)$$. Then, $$\forall y \in (g(a),g(b))$$, there is $$x \in (a,b)$$ such that $$g(x) = y$$.

### 5.3 Open and closed sets

#### Definition (Open sets)

A set $$A \subset \mathbb{R} $$ is called open if for every $$a \in A$$ there exists $$\epsilon > 0$$ such that $$(a - \epsilon, a + \epsilon) \subset A$$.

#### Definition (Closed sets)

A set $$A \subset \mathbb{R}$$ is called closed if its complement $$\mathbb{R} - A$$ is open.

#### Remark

The empty set $$\emptyset$$ and the whole set $$\mathbb{R}$$ are both open and closed.

#### Exercise

A set $$B$$ is closed if and only if
$$
\forall \{x_n\} \subset B \;\text{and}\; \lim_{n \to \infty} x_n = exists \implies \lim_{n \to \infty}x_n \in B
$$

#### Definition (Compact sets)

A set $$A \subset \mathbb{R}$$ is compact if and only if every sequence $$\{x_n\} \subset K$$ contains a convergent subsequence $$\{x_{n_i}\}$$ such that $$\lim_{i \to \infty} x_{n_k} \in K$$.

#### Exercise

A set $$K \subset \mathbb{R}$$ is compact if and only if it is closed and bounded.

### 5.4 The Extreme Value Theorem (Countiuity in cloed intervals means bounded)

Let $$f: [a, b] \to mathbb{R}$$ be continuous on $$[a,b]$$. Then $$f$$ is bounded above in $$[a,b]$$.

#### Corollary (Extreme value theorem)

Let $$f:[a,b] \to \mathbb{R}$$ be continous on $$[a,b]$$. Then there exists $$x \in [a,b]$$ such that
$$
f(x) \geq f(t) \quad \forall t \in [a,b]
$$

#### Exercise

If $$f: X \subset \mathbb{R} \to \mathbb{R}$$ is continous and $$X$$ is compact, then $$f$$ attains a maximum in $$X$$.

### 5.4 Uniform continuity

#### Definition (Uniform continuity)

We say that $$f: X \subset \mathbb{R} \to \mathbb{R}$$ is uniformly continuous on $$X$$ if
$$
\forall \epsilon > 0, \exists \delta > 0 \;\text{such that}\; \forall x,y \in X,\;|x-y| < \delta \implies |f(x) - f(y)| < \epsilon
$$

#### Exercise

Let $$f: X \subset \mathbb{R} \to \mathbb{R}$$ be continuous on $$X$$, then

- If $$X = [a,b]$$, then $$f$$ is uniformly continuous on $$X$$.
- If $$X$$ is compact, then $$f$$ is uniformly continuous on $$X$$.



## 6. Differentiation

### 6.1 The derivative

#### Definition (Derivative and differentiability)

We say that $$f$$ is differertiable at $$x_0$$ if $$\lim_{x \to x_0}\frac{f(x)-f(x_0)}{x-x_0}$$ exists. In this case we use the notation:
$$
f'(x_0) = \frac{df}{dx}(x_0) = \lim_{x \to x_0}\frac{f(x)-f(x_0)}{x-x_0} = \lim_{h \to 0}\frac{f(x_0+h)-f(x_0)}{h}
$$
and we call $$f'(x_0)$$ the derivative of $$f$$ at $$x_0$$.

#### Remark Differertiability is a stronger condition than continuity

#### Theorem: (Differentiability implies continuity)

If $$f$$ is differentiable at $$a \in \mathbb{R} $$, then $$f$$ is continuous at $$a$$.

### 6.2 Higher order derivatives

#### Definition (Higher order derivatives)

If $$f$$ is differentiable at $$x_0$$, then we can consider the derivative of $$f'$$ at $$x_0$$:
$$
f''(x_0) = \frac{d^2f}{dx^2}(x_0) = \frac{d}{dx}\left(\frac{df}{dx}(x_0)\right)
$$
and we call $$f''(x_0)$$ the second derivative of $$f$$ at $$x_0$$. We can continue this process and define the $$n$$-th derivative of $$f$$ at $$x_0$$ as

$$
f^{(k)}(x_0) = \frac{d^kf}{dx^k}(x_0)
$$

### 6.3 Properties of the derivative

#### Proposition (Linearity of the derivative)

If $$f$$ and $$g$$ are differentiable at $$x \in \mathbb{R}$$, then $$f+g$$ is differentiable at $$x$$ and
$$
(f+g)'(x) = f'(x) + g'(x)
$$

#### Proposition (Leibniz rule)

If $$f$$ and $$g$$ are differentiable at $$x \in \mathbb{R}$$, then $$fg$$ is differentiable at $$x$$ and
$$
(fg)'(x) = f'(x)g(x) + f(x)g'(x)
$$

#### Proposition

Assume $$g$$ is differential at $$a \in \mathbb{R}$$ and $$g(a) \neq 0$$. Then the function
$$
f(x) = \frac{1}{g(x)}
$$
is differentiable at $$a$$ and
$$
(\frac{d}{dx}\frac{1}{g})(a) = -\frac{g'(a)}{g(a)^2}
$$

#### Corollary

If $$f$$ and $$g$$ are differentiable at $$a \in \mathbb{R}$$, then $$\frac{f}{g}$$ is differentiable at $$a$$ with $$g(a) \neq 0$$, then

$$
(\frac{d}{dx}\frac{f(x)}{g(x)})'(a) = \frac{f'(a)g(a) - f(a)g'(a)}{g(a)^2}
$$

#### Corollary

If $$c$$ is a constant and $$f$$ is differentiable at $$a \in \mathbb{R}$$, then
$$
\frac{d}{dx}(cf)(a) = cf'(a)
$$

#### Remark

Let $$I = [a,b]$$. We denota by

- $$C^0(I): = \{f:[a,b] \to \mathbb{R}: f \;\text{is continous on} \;[a,b]\}$$
- $$C^1(I): = \{f:[a,b] \to \mathbb{R}: f \; \text{is differentiable on} \;(a,b)\; \text{and}\; f' \; \text{is continous on} \;[a,b]\}$$
Then, $$\frac{d}{dx}: C^1(I) \to C^0(I)$$ is a linear map. In fact, both $$C^0(I)$$ and $$C^1(I)$$ are real vector spaces.
- $$(f+g)(x) = f + g$$
- $$(cf)(x) = cf$$

#### Theorem (Chain rule)

If $$g$$ is differentiable at $$a \in \mathbb{R}$$ and $$f$$ is differentiable at $$g(a)$$, then $$f \circ g$$ is differentiable at $$a$$ and
$$
(f \circ g)'(a) = f'(g(a))g'(a)
$$

### 6.4 The Derivative of Elementary Functions

#### Definition (Logarithm)

We define the logarithm function $$x \longmapsto \log(x)$$ as the inverse of the exponential function $$x \longmapsto e^x$$.

### 6.5 The Significance of the Derivative

#### Proposition (Monotonicity)

If

- $$f(x)$$ is differentiable on $$(a,b)$$ and
- $$f'(t)>0$$ for all $$t \in (a,b)$$,
then $$f$$ is monotone increasing on $$(a,b)$$.

#### Definition (Local extremum)

We say that $$f$$ attains a local maximum at $$c$$ if $$f(c) \leq f(x)$$, for all $$x \in (c-\delta, c+\delta)$$, for some $$\delta > 0$$. Similarly, we say that $$f$$ attains a local minimum at $$c$$ if $$f(c) \geq f(x)$$, for all $$x \in (c-\delta, c+\delta)$$, for some $$\delta > 0$$.

#### Theorem (Fermat's theorem)

If $$f: [a,b] \to \mathbb{R}$$ attains an interior local maximum (or minimum) at c, i.e. $$a<t<b$$, and $$f$$ is differentiable at $$c$$, then $$f'(c) = 0$$.

Remark that the converse is not true.

#### Definition (Critical point)

$$c$$ is a critical point of $$f$$ if $$f'(c) = 0$$
$$Maximum \; ,\; minimum \;,\; saddle \Rightarrow \; critical \; point$$

### 6.6 Existence of Critical Points

#### Theorem (Rolle's theorem)

Let $$f:[a.b] \to \mathbb{R}$$ continous on $$[a.b]$$ and differentiable on $$(a,b)$$. If $$f(a) = f(b)$$, then there exists $$t \in (a,b)$$ such that $$f'(t) = 0$$.

#### Proposition

Let $$f:(a,b) \to \mathbb{R}$$ be differentiable on $$(a,b)$$. Assume $$x < y \in (a,b)$$ and $$f'(x) >0 > f'(y)$$. Then, there is a $$t \in (x,y)$$ such that $$f'(t) = 0$$.

### 6.7 Two Important Applications

#### Theorem (Cauchy's Mean value theorem)

Let $$f:[a,b] \to \mathbb{R}$$ be continous on $$[a,b]$$ and differentiable on $$(a,b)$$. Then, there exists $$t \in (a,b)$$ such that
$$
f'(t) = \frac{f(b) - f(a)}{b-a}
$$

Proof idea: Consider the function $$g(t) = \frac{f(b) - f(a)}{b-a}(t-a) +f(a) $$ and apply Rolle's theorem.

#### Corollary

If $$f'(t) > 0$$ on $$(a,b)$$, then $$f$$ is strictly monotone increasing on $$(a,b)$$.

#### Theorem (The Intermediate Value Theorem for Derivatives)

Let $$f:(a,b) \to \mathbb{R}$$ be differentiable on $$(a,b)$$. Then, $$f'(t)$$ satisfies the intermediate value property, i.e.
$$
\forall x<y \; \text{and any} \;c\;\text{between} \;f'(x) \; \text{and} \;f'(y), \; \exists t \in (x,y) \; \text{with} \; f'(t) = c
$$

Remark: This is true even when $$f'$$ is not continous.

Proof idea : Consider the function $$g(s) = cs - f(s)$$ and apply the intermediate value theorem.

#### Corollary

If $$f'(t) \leq 0$$ for all $$t \in (a,b)$$, implies that $$f$$ is strictly monotone on $$(a,b)$$.

#### Theorem (The extended mean value theorem)

If $$f$$ and $$g$$ are continous on $$[a,b]$$ and differentiable on $$(a,b)$$, then there exists $$x \in (a,b)$$ such that
$$
(f(b) - f(a))g'(x) = (g(b) - g(a))f'(x)
$$

Proof idea: Consider the function $$h(t) = (f(b) - f(a))g(t) - (g(b) - g(a))f(t)$$ and apply Rolle's theorem.

#### Theorem (L'Hospital's rule)

Assume that
$$
\lim_{x \to a} f(x) = \lim_{x \to a} g(x) = 0
$$
If $$\lim_{x \to a} \frac{f'(x)}{g'(x)}$$ exists, then $$\lim_{x \to a} \frac{f(x)}{g(x)}$$ also exists and both limits are equal.

Proof idea: Apply the extended mean value theorem to $$f$$ and $$g$$.

### 6.8 The Second Derivative

#### Definition (Second derivative)

When we say "$$f''(x)$$ exists", we are assuming:

- $$\lim_{y \to x} \frac{f'(y) - f'(x)}{y-x}$$ exists
- $$f'(y)$$ exists for all $$ y \in (x-\delta, x+\delta) $$, for some $$\delta > 0$$.

#### Theorem (The second derivative test)

Let $$a$$ be a critical point of $$f$$, i.e. $$f'(a) = 0$$. Then,

- If $$f''(a) > 0$$, then $$f$$ has a local minimum at $$a$$.
- If $$f''(a) < 0$$, then $$f$$ has a local maximum at $$a$$.

#### Theorem

Assume $$f''(a)$$ exists and $$f$$ has a local minimu at $$a$$. Then, $$f''(a) \leq 0$$.

### 6.9 Convexity

#### Definition (Convexity)

A set $$U \subset \mathbb{R}^n$$ is convex if for any two points $$p,q \in U$$, the straight line segment joining $$p$$ and $$q$$ is contained in $$U$$.

#### Definition (Convex function)

We say that a function $$f:(a,b) \to \mathbb{R}$$ is convex if the region above its graph is convex.

#### Definition (Strict convexity)

We say that $$f$$ is strictly convex on $$I$$ if: for all $$a, b \in I$$ and $$ t\in (0,1)$$, we have
$$
f((1-t)a + tb) < (1-t)f(a) + tf(b)
$$
or equivalently, for all $$a <x< b$$ and we have
$$
f(x) < \frac{f(b) - f(a)}{b-a}(x-a) + f(a)
$$

#### Theorem (The second derivative test for convexity)

If $$f$$ is differentiable om $$I$$ and $$f'$$ is strictly monotone increasing on $$I$$, then $$f$$ is strictly convex on $$I$$.
Which is equivalent to:

If $$f$$ is twice differentiable on $$I$$ and $$f''(x) > 0$$ for all $$x \in I$$, then $$f$$ is strictly convex on $$I$$.

#### Exercise

- If $$f$$ is convex on $$I$$, the $$f$$ is continous on $$I$$.
- If $$f$$ is strictly convex on $$I$$, then $$f$$ has most one critical point on $$I$$, which is a global minimum.


## 7. Integration

#### Definition (Partition)

A partition of an interval $$[a,b]$$ is a finite set of points in $$[a,b] and containing both $$a$$ and $$b$$, i.e. a partition of $$[a,b]$$ is

$$
a = t_0 < t_1 < \cdots < t_n = b
$$

We usually denote a partition $$P$$ as

$$
P = a = t_0 < t_1 < \cdots < t_n = b
$$

or

$$
P = \{t_0, t_1, \cdots, t_n\}
$$

#### Definition (Lower and upper sum)

Let $$f:[a,b] \to \mathbb{R}$$ be a bounded function and given a partition $$P$$ of $$[a,b]$$. Let:

- $$m_i = \inf\{f(x): x \in [t_{i-1},t_i] \}$$
- $$M_i = \sup\{f(x): x \in [t_{i-1},t_i] \}$$

- Then, the lower sum of $$f$$ for $$P$$ as

$$
L(f,P) = \sum_{i=1}^n m_i(t_i - t_{i-1})
$$

- Then, the upper sum of $$f$$ for $$P$$ as

$$
U(f,P) = \sum_{i=1}^n M_i(t_i - t_{i-1})
$$

#### Lemma

Given $$P$$ and $$Q$$ partitions of $$[a,b]$$, we have

$$
L(f,P) \leq U(f,Q)
$$

In particular:

$$
\sup\{L(f,P): P \text{ is a partition of } [a,b]\} \leq 
$$

$$
\inf\{U(f,P): P \text{ is a partition of } [a,b]\}
$$

#### Example

The function $$f:[0,1] \to \mathbb{R}$$ defined by

$$
f(x) = \begin{cases}
1 & \text{ if } x \in \mathbb{Q} \\
0 & \text{ if } x \notin \mathbb{Q}
\end{cases}
$$

is not Riemann integrable.

#### Definition (Riemann integrable)

We say that a bounded function $$f:[a,b] \to \mathbb{R}$$ is Riemann integrable if

$$
\sup\{L(f,P): P \text{ is a partition of } [a,b]\} =
$$

$$
 \inf\{U(f,P): P \text{ is a partition of } [a,b]\}
$$

and we denote this common value as

$$
\int_a^b f(x) dx
$$

#### Theorem

If f is bounded on $$[a,b]$$, then $$f$$ is Riemann integrable if and only if for all $$\epsilon > 0$$, there exists a partition $$P$$ of $$[a,b]$$ such that

$$
U(f,P) - L(f,P) < \epsilon
$$


#### Theorem (Continous implies Riemann integrable)

If $$f$$ is continous on $$[a,b]$$, then $$f$$ is Riemann integrable on $$[a,b]$$.

#### Theorem

Let $$a<b<c$$ and $$f:[a,c] \to \mathbb{R}$$ be a bounded function. If $$f$$ is Riemann integrable on $$[a,b]$$ and $$[b,c]$$, then $$f$$ is Riemann integrable on $$[a,c]$$. Moreover, in such a case

$$
\int_a^c f(x) dx = \int_a^b f(x) dx + \int_b^c f(x) dx
$$

#### Theorem

$$f$$ and $$g$$ are Riemann integrable on $$[a,b]$$, then $$f+g$$ is Riemann integrable on $$[a,b]$$. Moreover, in such a case:

$$
\int_a^b (f(x) + g(x)) dx = \int_a^b f(x) dx + \int_a^b g(x) dx
$$

#### Theorem

Let $$f$$ be integrable on $$[a,b]$$ and assume $$m \leq f(x) \leq M$$ for all $$x \in [a,b]$$. Then

$$
m(b-a) \leq \int_a^b f(x) dx \leq M(b-a)
$$

#### Theorem

If $$f(x) \geq g(x)$$ $$ \forall x \in [a,b]$$ and both functions are integrable on $$[a,b]$$, then

$$
\int_a^b f(x) dx \geq \int_a^b g(x) dx
$$

#### Question

If $$f$$ is continous on $$[a,b]$$ and $$f(x) \geq 0$$ for all $$x \in [a,b]$$, then $$\int_a^b f(x) dx = 0$$ implies $$f(x) = 0\; \forall x \in [a,b]$$.

### 7.1 New functions using integral

Assume $$f$$ is integrable on $$[a,b]$$ then it is also integrable on $$[a,x]\; \forall x\in [a,b]$$. Therefore, we can define a new function
$$
F(x) = \int_a^x f(t) dt
$$

#### Theorem

If $$f$$ is integrable on $$[a,b]$$, then $$F(x) = \int_a^xf(t)dt$$ is continous on $$[a,b]$$

#### Theorem (The Fundamental Theorem of Calculus) (Part 1)

Let $$f$$ be integrable on $$[a,b]$$ and define $$F(x) = \int_a^x f(t) dt$$. If $$f$$ is continous at $$c \in [a,b]$$, then $$F$$ is differentiable at $$c$$ and $$F'(c) = f(c)$$.

#### Corollary

If $$f$$ is continous on $$[a,b]$$ and $$f = g'$$ for some function $$g$$ on $$[a,b]$$, then

$$
\int_a^b f(x) dx = g(b) - g(a)
$$

#### Definition (Primitive function)

We say that $$F$$ is a primitive function for $$f$$ if $$F$$ is differentiable on $$[a,b]$$ and $$F' = f$$ on $$[a,b]$$.

#### Theorem (The Fundamental Theorem of Calculus) (Part 2)

If $$g'$$ is integrable on $$[a,b]$$, then

$$
\int_a^b g'(x) dx = g(b) - g(a)
$$

Remark: $$g'(x)$$ dose not need to be continous. Therefore, continutiy means intergrability but not vice versa.

#### Exercise (Integration by parts)

If $$f$$ and $$g$$ are continous on $$[a,b]$$, then

$$
\int_a^b f(x)g'(x) dx = f(b)g(b) - f(a)g(a) - \int_a^b f'(x)g(x) dx
$$

#### Exercise (Change of variable formula)

Let $$\phi:[a, b] \to \mathbb{R}$$ and $$f: \mathbb{R} \to \mathbb{R}$$. Assume $$f$$ and $$\phi
'$$ are continous, then

$$
\int_a^b f(\phi(t))\phi'(t) dt = \int_{\phi(a)}^{\phi(b)} f(x) dx
$$

#### Definition (Logarithmic and exponential function)

We define the logarithmic function as, for $$x > 0$$,

$$
\log(x) = \int_1^x \frac{1}{t} dt
$$

and $$exp(y) = \log^{-1} (y)$$  $$\forall y \in \mathbb{R}$$.

