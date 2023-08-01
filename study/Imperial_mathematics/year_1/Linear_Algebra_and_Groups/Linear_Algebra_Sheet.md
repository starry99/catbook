---
layout: simple
title: Linear Algebra Memory Sheet
---

#### Based on the notes and lectures of [Dr. Charlotte Kestner](https://www.imperial.ac.uk/people/c.kestner/publications.html), [Prof. David Evans](https://www.ma.imperial.ac.uk/~dmevans/?_gl=1*770mhm*_ga*NTkyNDQ0MjkxLjE2OTA0NTE4MjA.*_ga_LME5ZDDFS0*MTY5MDc0NDkyOC4yOC4xLjE2OTA3NDY0NDYuNTguMC4w) and [Dr. Michele Zordan](https://mzordan.com).

## 1. Matrix

### The product of two matrices

 Let $$\mathrm{A}=\left(a_{i j}\right)_{p \times q}$$ and $$\mathrm{B}=\left(b_{i j}\right)_{q \times r}$$. Then the matrix product of $$\mathrm{A}$$ and $$\mathrm{B}$$,

$$
\mathrm{C}=\left(c_{i j}\right)_{p \times r}, \quad \text { where } \quad c_{i j}=\sum_{k=1}^{q} a_{i k} b_{k j}
$$

### Echelon form (ef)

We say a matrix is in echelon form (ef) if must satisify the following:

- All of the zero rows are at the bottom.

- The first non-zero entry in each row is 1.

- The first non-zero entry in row $$i$$ is strictly to the left of the first non-zero entry in row $$i+1$$.

We say a matrix is in row reduced echelon form (rref) if it is in echelon form and:

- The first non-zero entry in row $$i$$ appears in column $$j$$, then every other element in column $$j$$ is zero.
EF

$$
\left(\begin{array}{ccc|c}
1 & 1 & 2 & 2 \\
0 & 1 & 7 & 12 \\
0 & 0 & 1 & -10 \\
0 & 0 & 0 & 0
\end{array}\right)
$$

RREF

$$
\left(\begin{array}{ccc|c}
1 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1 \\
0 & 0 & 0 & 0
\end{array}\right)
$$

### Singular matrix

A matrix without an inverse is called a singular matrix.

### Inverse of a matrix

If $$\mathrm{A}=\left[a_{i j}\right]_{m \times n}$$, then the Transpose of $$A$$ is $$\mathrm{A}^{\top}=\left[a_{j i}\right]_{n \times m}$$.

### Orthogonal matrix preserves inner product

Let $$A \in M_{n \times n}(\mathbb{R})$$. The following are equivalent:

(i) $$A$$ is invertible with inverse $$A^{-1}=A^{T}$$

(ii) $$A^{T} A=I_{n}=A A^{T}$$.

(iii) $$A$$ preserves inner products (i.e. for all $$x, y \in \mathbb{R}^{n}(A x) \cdot(A y)=x \cdot y$$.

### Fields

Let $$\mathbb{F}_{p}=\{0,1, \ldots, p-1\}$$, consider $$\mathbb{F}_{p}$$ with addition defined by addition modulo $$p$$ and multiplication as multiplication modulo $$p$$. Then the structure $$\left(\mathbb{F}_{p},+{ }_{(\bmod p)}, \times{ }_{(\bmod p)}\right)$$ is a field.

## 2. Vector space

### Vector space must closure under addition and scalar multiplication and contain additive identity and scalar identity

Let $$F$$ be a field. A vector space over $$F$$ is a non-empty set $$V$$ together with the following maps:

Addition

$$
\oplus: \begin{aligned}
\oplus \times V & \mapsto V \\
\left(v_{1}, v_{2}\right) & \mapsto v_{1} \oplus v_{2}
\end{aligned}
$$

Scalar Multiplication

$$
\begin{aligned}
\odot: F \times V & \mapsto V \\
\left(f, v_{2}\right) & \mapsto f \odot v_{2}
\end{aligned}
$$

$$\oplus$$ and $$\odot$$ must satisfy the following Vector Space axioms:

For Vector Addition:

A1 Associative law: $$(\mathbf{u} \oplus \mathbf{v}) \oplus \mathbf{w}=\mathbf{u} \oplus(\mathbf{v} \oplus \mathbf{w})$$.

A2 Commutative law: $$\mathbf{v} \oplus \mathbf{w}=\mathbf{w} \oplus \mathbf{v}$$.

A3 Additive identity: $$0_{V} \oplus \mathbf{v}=\mathbf{v}$$, where $$0_{V}$$ is called the IDENTITY vector (or sometimes the zero vector).

A4 Additive inverse: $$\mathbf{v} \oplus(\ominus \mathbf{v})=0_{V}$$.

For scalar multiplication:

A5 Distributive law: $$r \odot(\mathbf{v} \oplus \mathbf{w})=(r \odot \mathbf{v}) \oplus(r \odot \mathbf{w})$$.

A6 Distributive law: $$(r+s) \odot \mathbf{v}=(r \odot \mathbf{v}) \oplus(s \odot \mathbf{v})$$.

A7 Associative law: $$r \odot(s \odot \mathbf{v})=(r s) \odot \mathbf{v}$$.

A8 Identity for scalar mult: $$1 \odot \mathbf{v}=\mathbf{v}$$.

### Subspace

 A subset $$W$$ of a vector space $$V$$ is a subspace of $$V$$ if

- $$W$$ is not empty (i.e. $$e \in W$$)

- for $$\mathbf{v}, \mathbf{w} \in W$$, then $$\mathbf{v} \oplus \mathbf{w} \in W$$ closed under vector addition

- $$\mathbf{v} \in W$$ and $$r \in \mathbb{R}$$, then $$r \odot \mathbf{v} \in W$$ closed under scalar multiplication.

### Theorem (The insertion of subspaces is still a subspace)

Let $$U, W$$ be subspaces of $$V$$. Then $$U \cap W$$ is a subspace of V. In general, the intersection of any set of subspaces of a vector space $$V$$ is a subspace of $$V$$.

### Example (The  union of subspaces may not be a subspace)

$$
U=\left\{\left(\begin{array}{l}
x \\
0
\end{array}\right): x \in \mathbb{R}\right\}, W=\left\{\left(\begin{array}{l}
0 \\
y
\end{array}\right): y \in \mathbb{R}\right\} \quad \text { and } \quad V=\mathbb{R}^{2}
$$

Then

$$
\left(\begin{array}{l}
1 \\
0
\end{array}\right),\left(\begin{array}{l}
0 \\
1
\end{array}\right) \in U \cup W
$$

but

$$
\left(\begin{array}{l}
1 \\
0
\end{array}\right) \oplus\left(\begin{array}{l}
0 \\
1
\end{array}\right)=\left(\begin{array}{l}
1 \\
1
\end{array}\right) \notin U \cup W
$$

### Spanning

The $$\operatorname{span}$$ of $$u_{1}, \ldots, u_{m}$$ is the set of linear combinations of $$u_{1}, \ldots, u_{m}$$. i.e. $$\operatorname{Span}\left(u_{1}, \ldots, u_{m}\right)=$$ $$\left\{\alpha_{1} u_{1}+\ldots+\alpha_{m} u_{m} \in V: \alpha_{1}, \ldots, \alpha_{m} \in F\right\}$$.

### Lemma

Let $$v_{1}, \ldots, v_{n}$$ be linearly independent in an $$F$$-vector space $$V$$. Let $$v_{n+1}$$ be such that $$v_{n+1} \notin \operatorname{Span}\left(v_{1}, \ldots, v_{n}\right)$$. Then $$v_{1}, \ldots, v_{n+1}$$ is linearly independent.

### Bases

Let $$V$$ be an $$F$$-vector space. A basis of $$V$$ is a linearly independent spanning set of $$V$$.

### Proposition (The coordinates of a vector are unique)

Let $$V$$ be an $$F$$-vector space, let $$S=\left\{u_{1}, \ldots, u_{m}\right\} \subseteq V$$. Then $$S$$ is a basis of $$V$$  if and only if every vector in $$V$$ has a unique expression as a linear combination of elements of $$S$$.

### Proposition  (Every spanning set contains a basis)

Proposition 3.5.6. Let $$V$$ be a non-trivial (i.e. not $$\{0\}$$) $$F$$-vector space and suppose $$V$$ has a finite spanning set $$S$$ then $$S$$ contains a linearly independent spanning set.

### Lemma (Steinitz Exchange Lemma)

Let $$V$$ be a vector space over $$F$$. Take $$X \subseteq V$$ and suppose $$u \in \operatorname{Span}(X)$$ but $$u \notin \operatorname{Span}(X \backslash\{v\})$$ for some $$v \in X$$. Let $$Y=(X \backslash\{v\}) \cup\{u\}$$ (i.e., we "exchange $$v$$ for $$u$$ "). Then $$\operatorname{Span}(X)=$$ $$\operatorname{Span}(Y)$$

Proof

Since $$u \in \operatorname{Span}(X)$$ we have $$\alpha_{1}, \ldots, \alpha_{n} \in F$$ such that $$v_{1}, \ldots, v_{n} \in X$$ such $$u=\alpha_{1} v_{1}+\ldots+\alpha_{n} v_{n}$$. Now there is a $$v \in X$$ such that $$u \notin \operatorname{Span}(X \backslash\{v\})$$ we may assume, WLOG, that $$v=v_{n}$$, thus $$\alpha_{n} \neq 0$$ so:

$$
v=v_{n}=\frac{1}{\alpha_{n}}\left(u-\alpha_{1} v_{1} \ldots-\alpha_{n-1} v_{n-1}\right)
$$

Now if $$w \in \operatorname{Span}(Y)$$ then for some $$\beta_{0}, \beta_{1}, \ldots, \beta_{m}$$ we have $$v_{1}, \ldots, v_{m} \in X \backslash\{v\}$$

$$
\begin{aligned}
w & =\beta_{0} u+\sum_{i=0}^{m} \beta_{i} v_{i} \\
& =\beta_{0}\left(\alpha_{1} v_{1}+\ldots+\alpha_{n} v_{n}\right)+\sum_{i=0}^{m} \beta_{i} v_{i} \in \operatorname{Span}(X \backslash\{v\} \cup\{v\})=\operatorname{Span}(X)
\end{aligned}
$$

So $$\operatorname{Span}(Y) \subseteq \operatorname{Span}(X)$$

Similarly we have that if $$w \in \operatorname{Span}(X)$$ the $$w$$ is a linear combination of elements of $$X$$, now we can replace $$v_{n}$$ with $$\frac{1}{\alpha_{n}}\left(u-\alpha_{1} v_{1} \ldots-\alpha_{n-1} v_{n-1}\right.$$ so we can express $$w$$ as a linear combination of elements of $$Y$$. So $$\operatorname{Span}(X) \subseteq \operatorname{Span}(Y)$$, thus $$\operatorname{Span}(Y)=\operatorname{Span}(X)$$.

### Theorem (Linear independent sets are at most as big as spanning sets)

Let $$V$$ be a finite dimensional vector space over $$F$$. Let $$S, T$$ be finte subsets of $$V$$. If $$S$$ is LI and $$T$$ spans $$V$$ then 

$$
|S| \leq|T|
$$

That is, LI sets are at most as big as spanning sets.

### Lemma

Suppose that $$\operatorname{dim} V=n$$ :

1. Any spanning set of size $$n$$ is a basis.

2. Any linearly independent set of size $$n$$ is a basis.

3. $$S$$ is a spanning set if and only if it contains a basis (as a subset).

4. $$S$$ is linearly independent if and only if it is contained in a basis (i.e. it's a subset of a basis).

5. Any subset of $$V$$ of size $$>n$$ is linearly dependent.

### Definition (Intersection and sum of subspaces)

Let $$V$$ be a vector space, $$U$$ and $$W$$ be subspaces of $$V$$.

- The intersection of $$U$$ and $$W$$ is:

$$
U \cap W=\{v \in V: v \in W \text { and } v \in U\}
$$

- The sum of $$U$$ and $$W$$ is:

$$
U+W=\{u+w: u \in U, w \in W\}
$$

and the sum and intersection are subspaces of $$V$$.

### Proposition

Let $$V$$ be a vector space over $$F$$. Let $$U$$ and $$W$$ be subspaces of $$V$$, suppose additionally:

- $$U=\operatorname{Span}\left\{u_{1}, \ldots, u_{s}\right\}$$

- $$W=\operatorname{Span}\left\{w_{1}, \ldots, w_{r}\right\}$$

Then $$U+W=\operatorname{Span}\left\{u_{1}, \ldots, u_{s}, w_{1}, \ldots, w_{r}\right\}$$.

### Proposition

 Let $$A$$ be an $$n \times n$$ matrix with entried in $$F$$, then the following statements are equivalent:

1. $$\operatorname{rank}(A)=n$$ (" $$A$$ has full rank").

2. The rows of $$A$$ form a basis for $$F^{n}$$.

3. The columns of $$A$$ form a basis for $$F^{n}$$.

4. $$A$$ is invertible (so $$\operatorname{det}(A) \neq 0$$, etc.).

## 3. Linear Transformations

### Definition (Image and Kernel)

Let $$T: V \rightarrow W$$ be a linear transformation:

- The Image of $$T$$ is the set $$\operatorname{Im} T=\{T(v) \in W: v \in V\} \subseteq W$$.

- The Kernel of $$T$$ is the set $$\operatorname{Ker} T=\left\{v \in V: T(v)=0_{W}\right\} \subseteq V$$.

### Proposition

Let $$T: V \rightarrow W$$ be a linear tranformation and let $$v_{1}, v_{2} \in V$$. Then

$$
T\left(v_{1}\right)=T\left(v_{2}\right) \text { iff } v_{1}-v_{2} \in \operatorname{Ker} T .
$$

### Proposition

Let $$A$$ be an $$m \times n$$ matrix. Let $$T: F^{n} \rightarrow F^{m}$$ be given by $$T(v)=A v$$. Then:

1. $$\operatorname{Ker} T$$ is the solution space to $$A v=0$$.

2. $$\operatorname{Im} T$$ is the column space of $$A$$.

3. $$\operatorname{dim}(\operatorname{Im} T)=\operatorname{rankA}$$.

### Theorem (The rank-nulity theorem)

We've seen that when $$T v=A v, \operatorname{rank}(A)=$$ $$\operatorname{dim}(\operatorname{Im} T)$$. An old fashioned name for $$\operatorname{dim}(\operatorname{Ker} T)$$ is the nulity of $$A$$

Let $$T: V \rightarrow W$$ be a linear transformation. Then

$$
\operatorname{dim}(\operatorname{Im} T)+\operatorname{dim}(\operatorname{Ker} T)=\operatorname{dim}(V)
$$

Proof: Let $$\left\{u_{1}, \ldots u_{s}\right\}$$ be a basis for ker $$T$$, and let $$\left\{w_{1}, \ldots, w_{r}\right\}$$ be a basis for $$\operatorname{Im} T$$. For each $$w_{i} \in \operatorname{Im} T$$, and so $$\exists v_{i} \in V$$ with $$T v_{i}=w_{i}$$. We claim that $$B=\left\{u_{1}, \ldots, u_{s}\right\} \cup\left\{v_{1}, \ldots v_{r}\right\}$$ is a basis for $$V$$.

- Spanning set: Let $$v \in V$$ since $$T v \in \operatorname{Im} T$$ we can write $$T v=\lambda_{1} w_{1}+\ldots \lambda_{r} w_{r}$$ for scalars $$\lambda_{i}$$. So

$$
\begin{aligned}
\text { Tv } & =\lambda_{1} w_{1}+\ldots \lambda_{r} w_{r} \\
& =T\left(\lambda_{1} v_{1}+\ldots \lambda_{r} v_{r}\right)
\end{aligned}
$$

Now by proposition 4.2.5 $$v-\lambda_{1} v_{1}+\ldots \lambda_{r} v_{r} \in \operatorname{ker} T$$ so $$v-\lambda_{1} v_{1}+\ldots \lambda_{r} v_{r}=\mu_{1} u_{1}+\ldots+\mu_{s} u_{s}$$. Thus

$$
v=\mu_{1} u_{1}+\ldots+\mu_{s} u_{s}+\lambda_{1} v_{1}+\ldots \lambda_{r} v_{r} \in \operatorname{span}(B)
$$

- Linear independence Suppose:

$$
\lambda_{1} v_{1}+\ldots \lambda_{r} v_{r}+\mu_{1} u_{1}+\ldots+\mu_{s} u_{s}=0
$$

By applying $$T$$ we get:

$$
\begin{aligned}
0 & =T\left(\lambda_{1} v_{1}+\ldots \lambda_{r} v_{r}+\mu_{1} u_{1}+\ldots+\mu_{s} u_{s}\right) \\
& =\lambda_{1} T\left(v_{1}\right)+\ldots \lambda_{r} T\left(v_{r}\right)+\mu_{1} T\left(u_{1}\right)+\ldots+\mu_{s} T\left(u_{s}\right) \\
& =\lambda_{1} w_{1}+\ldots \lambda_{r} w_{r}
\end{aligned}
$$

Thus $$\lambda_{1}=\ldots=\lambda_{r}=0$$, so we get that $$\mu_{1} u_{1}+\ldots+\mu_{s} u_{s}=0$$, so $$\mu_{1}=\ldots=\mu_{s}=0$$.

### The relation of the coefficients matrix to the system of equations and the augmented matrix with the solution set

For a homogeneous system $$Ax=0$$, the solution set is the kernel of the linear transformation $$T: F^{n} \rightarrow F^{m}$$ given by $$T(x)=A x$$. So the solution set is the kernel of the matrix $$A$$.

Now the $$\operatorname{dim}(\operatorname{Im}(A))=\operatorname{rank}(A)$$ thus the we can work out how many solutions we have to a set of homogeneous equations with $$n$$ unknowns:

- If $$\operatorname{rank}(A) \geq n$$ we get one solution (the trivial one i.e. $$0_{V}$$)

- If $$\operatorname{rank}(A)<n$$ we get infinitely many solutions (assuming $$F$$ is infinite)

Let $$A$$ be an $$m \times n$$ matrix with entries in $$F$$ and let $$b \in F^{m}$$. Then the following statements are equivalent:

- $$
\rank(A) = \rank(A|b) =n \longrightarrow  \text{ the system } Ax=b \text{ has a unique solution }
$$

- $$
\rank(A) = \rank(A|b) < n \longrightarrow \text{ the system }Ax=b \text{ has infinitely many solutions }
$$

- $$
\rank(A) < \rank (A|b) \longrightarrow \text{ the system }Ax=b \text{ has no solutions }
$$

### Basis change matrix

Suppose $$T: V \to V$$, $$\mathbb{F}$$ isa field. 

$$
\dim(V) = n,\; n \in \mathbb{N}
$$

and $$B, C$$ are bases for $$V$$.

$$
B =  \{b_1, \ldots, b_n \}
$$

then $$[T]_B = (T(b_1), \ldots, T(b_n))$$.

$$
[T]_{C}={ }_{C}[i d]_{B} \cdot[T]_{B} \cdot{ }_{B}[i d]_{C}
$$

## 4. Determinants

### Definition

$$
\operatorname{det}(A)=\sum_{j=1}^{n}(-1)^{1+j} a_{1 j} \operatorname{det}\left(A_{1 j}\right)
$$

#### The properties of the determinant

- If $$A$$ has a row of zeros, then $$\operatorname{det}(A)=0$$.
- If $$A$$ is triangular, then $$\operatorname{det}(A)=a_{11} \ldots a_{n n}$$.
- Let $$B$$ be the matrix obtained from $$A$$ by multiplying the lth row of $$A$$ by $$\alpha$$. Then $$\operatorname{det}(B)=\alpha \operatorname{det}(A)$$.
- Suppose $$B$$ is obtained from $$A$$ by interchanging rows $$i$$ and $$i+1$$. Then $$\operatorname{det} B=-\operatorname{det} A$$.

- Suppose $$A$$ has two rows equal. Then $$\operatorname{det} A=0$$.

- Suppose $$B$$ is obtained from $$A$$ by interchanging two rows. Then $$\operatorname{det} B=-\operatorname{det} A$$.

- Suppose $$B$$ is obtained from $$A$$ by adding $$\alpha$$ times row $$i$$ to row $$j$$. Then $$\operatorname{det} B=\operatorname{det} A$$.
- If $$A$$ is invertible, then $$\operatorname{det}(A) \neq 0$$.
- If $$A$$ is invertible, then $$\operatorname{det}\left(A^{-1}\right)=\frac{1}{\operatorname{det}(A)}$$.
- If $$A$$ is invertible, then $$\operatorname{det}(A B)=\operatorname{det}(A) \operatorname{det}(B)$$.
- If $$A$$ is invertible, then $$\operatorname{det}\left(A^{T}\right)=\operatorname{det}(A)$$.

### Definiton (Sigular matrix)

A matrix $$A \in M_{n}(F)$$ is said to be singular if there is a non-zero $$v \in F^{n}$$ with $$A v=0$$. Otherwise, it is called non-singular.

### Theorem

Suppose $$A \in M_{n}(F)$$. Then the following are equivalent:

(1) A is invertible.

(2) $$A$$ is non-singular.

(3) The rows of $$A$$ are linearly independent.

(4) $$A$$ is row-equivalent to $$I_{n}$$.

(5) $$\operatorname{det}(A) \neq 0$$

(6) $$\rank(A) = n$$

### Vandermonde determinant

Let $$n \geq 2$$ and let $$x_{1}, \ldots, x_{n} \in F$$.

$$
\operatorname{det}\left(\begin{array}{ccccc}
1 & x_{1} & x_{1}^{2} & \cdots & x_{1}^{n-1} \\
1 & x_{2} & x_{2}^{2} & \cdots & x_{2}^{n-1} \\
\ddots & \ddots & \ddots & & \ddots \\
1 & x_{n} & x_{n}^{2} & \cdots & x_{n}^{n-1}
\end{array}\right)=\prod_{1 \leq i<j \leq n}\left(x_{j}-x_{i}\right)
$$

### Definition (Cofactor)

Let $$A=\left(a_{i j}\right) \in M_{n}(F)$$. If $$1 \leq i, j \leq n$$, the $$i j^{\text {th }}$$ cofactor of $$A$$ is

$$
c_{i j}=(-1)^{i+j} \operatorname{det}\left(A_{i j}\right)
$$

### Theorem (Cramer's Rule)

Let $$A=\left(a_{i j}\right) \in M_{n}(F)$$ and let $$C=\left(c_{i j}\right)$$ be the matrix of cofactors of $$A$$. Then $$C^{T} A=\operatorname{det}(A) I_{n}$$. In particular, if $$\operatorname{det}(A) \neq 0$$ then

$$
A^{-1}=\frac{1}{\operatorname{det}(A)} C^{T}
$$
Here, $$C^{T}$$ is sometimes called the adjugate matrix of $$A$$ and $$\operatorname{denoted} \operatorname{by} \operatorname{adj}(A)$$.

### Theorem

The determinant $$\operatorname{det}(T)$$ does not depend on the choice of the basis.)

## 5. Eigenvalues and Eigenvectors

### Proposition

Suppose $$V$$ is a finite dimensional vector space over a field $$F$$ and $$B$$ is a basis for $$V$$. Let $$T: V \rightarrow V$$ be a linear map.

(i) The eigenvalues of $$T$$ are the same as the eigenvalues of the matrix $$[T]_{B}$$.

(ii) A vector $$v \in V$$ is an eigenvector of $$T$$ with eigenvalue $$\lambda$$ if and only if the coordinate vector $$[v]_{B}$$ is an eigenvector of the matrix $$[T]_{B}$$ with eigenvalue $$\lambda$$.

$$
T(v)=\lambda v \Leftrightarrow[T(v)]_{B}=[\lambda v]_{B} \Leftrightarrow[T(v)]_{B}[v]_{B}=\lambda[v]_{B}
$$

### Definition (The characteristic polynomial)

(i) Suppose $$A \in M_{n}(F)$$ and let $$x$$ denote a variable (or 'indeterminate'). The characteristic polynomial of $$A$$ is $$\chi_{A}(x)=\operatorname{det}\left(x I_{n}-A\right)$$.
(ii) Suppose $$V$$ is a finite dimensional vector space over a field $$F$$ and $$B$$ is a basis for $$V$$. Let $$T: V \rightarrow V$$ be a linear map. We define the characteristic polynomial of $$T$$ to be $$\chi_{T}(x)=\operatorname{det}\left(x I_{n}-C\right)$$, where $$C=[T]_{B}$$.

### Theorem

(i) Suppose $$A \in M_{n}(F)$$ and $$\lambda \in F$$. Then $$\lambda$$ is an eigenvalue of $$A$$ if and only if $$\chi_{A}(\lambda)=0$$.

(ii) Suppose $$V$$ is a finite dimensional vector space over a field $$F$$ and $$T: V \rightarrow V$$ is a linear map. Then $$\lambda \in F$$ is an eigenvalue of $$T$$ if and only if $$\chi_{T}(\lambda)=0$$.

### Definition (Diagonalizable)

(1) A linear map $$T: V \rightarrow V$$ is diagonalisable if there is a basis of $$V$$ consisting of eigenvectors of $$T$$.

(2) A matrix $$A \in M_{n}(F)$$ is is diagonalisable if there is a basis of $$F^{n}$$ consisting of eigenvectors of $$T$$.

### Theorem

(1) Suppose $$V$$ is a finite dimensional vector space over a field $$F$$ and $$T: V \rightarrow V$$ is a linear map. Then $$T$$ is diagonalisable if and only if there is a basis $$B: v_{1}, \ldots, v_{n}$$ of $$V$$ such that $$D=[T]_{B}$$ is a diagonal matrix.

(2) $$A$$ matrix $$A \in M_{n}(F)$$ is diagonalisable iff there is an invertible matrix $$P \in M_{n}(F)$$ such that $$P^{-1} A P$$ is a diagonal matrix. In this case, the columns of $$P$$ consist of eigenvectors of $$A$$ and form a basis of $$F^{n}$$.

### Theorem

Suppose $$V$$ is a vector space over a field $$F$$ and $$T: V \rightarrow V$$ is a linear map. Suppose $$v_{1}, \ldots, v_{n}$$ are eigenvectors of $$T$$ with $$T\left(v_{i}\right)=\lambda_{i} v_{i}$$ for $$i \leq n$$. If the $$\lambda_{i}$$ are distinct then $$v_{1}, \ldots, v_{n}$$ are linearly independent.

### Summary

Suppose we are given:

- A finite dimensional vector space $$V$$ over a field $$F, \operatorname{dim}(V)=n$$;

- A linear map $$T: V \rightarrow V$$.

We want to answer the following questions:

- Is $$T$$ diagonalisable over $$F$$ ?

- If so, find a basis of $$V$$ consisting of eigenvalues of $$T$$.

The method to do this is:

(1) Compute the characteristic polynomial $$\chi_{T}(x)$$ and find the (distinct) eigenvalues $$\lambda_{1}, \ldots, \lambda_{r} \in$$ $$F$$

(2) For each $$i \leq r$$, find a basis $$B_{i}$$ for the eigenspace

$$
 E_{\lambda_{i}}={v \in V: T(v)=\lambda_{i} v}
$$

(3) If

$$
\sum_{i=1}^{r}|B_{i}|<\operatorname{dim}(V)
$$

then $$T$$ is not diagonalisable.

(4) If

$$
\sum_{i=1}^{r}\left|B_{i}\right|=\operatorname{dim}(V)
$$

then the union $$B=B_{1} \cup \ldots \cup B_{r}$$ is a basis of $$V$$ consisting of eigenvectors and so $$T$$ is diagonalisable.

As a special case, if $$T$$ has $$n$$ distinct eigenvalues, then it is diagonalisable.

### Definition (The inner product)

(1) The inner product of $$u$$ and $$v$$ is

$$
u \cdot v=u^{T} v=\sum_{i=1}^{n} \alpha_{i} \beta_{i}
$$

### Definition (norm)

$$
\|u\|=\sqrt{u \cdot u}=\left(\sum_{i=1}^{n} \alpha_{i}^{2}\right)^{1 / 2} \in \mathbb{R}^{\geq 0} .
$$

### Lemma

A matrix $$P \in M_{n}(\mathbb{R})$$ is an orthogonal matrix iff the columns of $$P$$ form an orthonormal set in $$\mathbb{R}^{n}$$.

### Theorem (Gram - Schmidt Process)
 Let $$v_{1}, \ldots, v_{r}$$ be linearly independent vectors in $$\mathbb{R}^{n}$$. Define inductively vectors $$w_{1}, \ldots, w_{r}$$ as follows $$($$ for $$i \leq r)$$ :

$$
\begin{aligned}
& w_{1}=v_{1} ; \\
& w_{2}=v_{2}-\frac{w_{1} \cdot v_{2}}{w_{1} \cdot w_{1}} w_{1} ; \\
& w_{3}=v_{3}-\left(\frac{w_{1} \cdot v_{3}}{w_{1} \cdot w_{1}} w_{1}+\frac{w_{2} \cdot v_{3}}{w_{2} \cdot w_{2}} w_{2}\right) ; \\
& \vdots \\
& w_{i}=v_{i}-\sum_{j=1}^{i-1}\left(\frac{w_{j} \cdot v_{i}}{w_{j} \cdot w_{j}}\right) w_{j} ;
\end{aligned}
$$

Then:

(i) The vectors $$w_{1}, \ldots, w_{r}$$ are an orthogonal set of vectors.

(ii) If $$u_{i}=w_{i} /\left\|w_{i}\right\|$$, then $$u_{1}, \ldots, u_{r}$$ is an orthonormal set of vectors.

(iii) For $$i \leq r$$ we have $$\operatorname{Span}\left(v_{1}, \ldots, v_{i}\right)=\operatorname{Span}\left(w_{1}, \ldots, w_{i}\right)=\operatorname{Span}\left(u_{1}, \ldots, u_{i}\right)$$.

## Theorem (Spectral Theorem)

If a matrix $$A \in M_{n}(\mathbb{R})$$ is symmetric (that is, $$A=A^{T}$$), then it is diagonalisable over $$\mathbb{R}$$ by two orthogonal matrix, which consists of its eigenvectors . Moreover, there is an orthogonal basis of $$\mathbb{R}^{n}$$ consisting of eigenvectors of $$A$$.

## Theorem

If $$A \in M_{n}(\mathbb{R})$$ is symmetric and $$u, v \in \mathbb{R}^{n}$$, then

$$
(A u) \cdot v=(A u)^{T} v=\left(u^{T} A^{T}\right) v=u^{T}(A v)=u \cdot(A v)
$$


