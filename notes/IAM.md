# Applied Mathematics Dense Sheet 

## 1. Part I Graphs

### 1.1. Graphs

## 2. Definition (Incidence Matrix)

Let $G$ be a graph with $n$ nodes and $m$ edges. The incidence matrix $A$ of $G$ is an $m \times n$ matrix, where the number of nodes is the number of columns and the number of edges is the number of rows.

## 3. Theorem (Rank nullity theorem)

For an $m \times n$ incidence matrix $A$, we have

- $\operatorname{dim}(\operatorname{right}$ null space) $+\operatorname{rank}(A)=n$ (the number of nodes)
- $\operatorname{dim}($ left null space) $+\operatorname{rank}(A)=m$ (the number of edges)


## 4. The geometric interpretation of the rank nullity theorem

- $\operatorname{dim}$ (right null space) is the number of connected components in the graph. Therefore, for a connected graph, dim (right null space) $=1$.
- $\operatorname{dim}$ (left null space) is the number of independent loops in the graph.


### 4.1. Circuits

The vector of potential differences

$\mathbf{e}=\mathbf{A x}$

The vector of edge fluxeslcurrents (Ohm's law) $\mathbf{w}=-C \mathbf{A} \mathbf{x}$, where $C$ is the diagonal matrix of edge conductances.

The vector of fluxes out of each node $\backslash$ divergence of fluxes at each node $\mathbf{f}=-\mathbf{A}^{\mathrm{T}} \mathbf{w}=\mathbf{A}^{\mathrm{T}} \mathbf{C A \mathbf { x }}$

## 5. If the conductance is unit

- $\mathrm{w}=-\mathrm{e}=-A \mathrm{x}$
- $\mathrm{f}=A^{T} A \mathrm{x}$


## 6. Laplacian matrix

$$
\begin{gathered}
\mathbf{K}=\mathbf{A}^{T} \mathbf{A} \\
\mathbf{K} \mathbf{x}=\mathbf{f}
\end{gathered}
$$

## 7. The linearity of the the voltage and current

If we change the voltage source from $V$ to $V^{\prime}$ propotionally, then the voltage and current change propotionally.

## 8. Definition (Effective conductance)

The divergence of fluxes at the node with unit voltage source.

## 9. Definition (Harmonic potential)

A harmonic potential is a potential at node $i$ that is the avarage of the potentials of its neighbors.

## 10. Remark

- The maximum and minimum possible values of the potentials in a connected graph occurs at the boundary node.
- The uniqueness principle for harmonic potentials: the harmonic potential is unique. Given the same potentials at boundary nodes, the harmonic potential is the same.


### 10.1. Random walks

## 11. Definition ( $p_{i}$ Hitting Probability )

$p_{i}$ is the probability that a random walk starting at node $i$ to reach the + node where $p_{+}=1$ before returning to node - where $p_{-}=0$.

$p_{i}$ can be regraded as the potential of node $i$ with the node + and - as the boundary nodes.

## 12. Definition ( Escape probability )

If the random walk starts at node $i, p_{e s c}$ is the probability that the random walk reaches the boundary node + before returning to node $i$. ( The nodes that he starts and the nodes that he don't want to return before reaching the target nodes )

$$
p_{e s c}=\frac{C_{e f f}}{n}
$$

where $C_{e f f}$ is the effective conductance of node + (where he starts ) to the boundary node -( where he wants to reach ).

$n$ is the total number of edges connected with the node he starts .

### 12.1. Spring mass systems

## 13. Theorem (Hook's law)

$$
\mathbf{T}=\mathbf{C A x}
$$

where $\mathbf{T}$ is the internal spring forces, $\mathbf{C}$ is the spring constant matrix $\mathbf{A}$ is the incidence matrix, $\mathbf{x}$ is the displacement.

## 14. Theorem (Newton's second law)

$$
\mathbf{f}-\mathbf{K} \mathbf{x}=\mathbf{M} \frac{d^{2} \mathbf{x}}{d t^{2}}
$$

where $\mathbf{M}$ is the mass matrix, $\mathbf{f}$ is the external forces, $\mathbf{K}$ is the Laplacian matrix. $\mathbf{x}$ is the displacement.

If the system is in equilibrium, then

$$
\mathbf{K} \mathbf{x}=\mathbf{f}
$$

## 15. Calculating the natural frequencies

Since it is in the equilibrium, we have to ignore the external forces $\mathbf{f}$. Therefore, we have

$$
-\mathbf{K} \mathbf{x}=\mathbf{M} \frac{d^{2} \mathbf{x}}{d t^{2}}
$$

Set $\mathbf{x}=\mathbf{x} e^{i \omega t}$, then we have

$$
\mathbf{K} \mathbf{x}=\omega^{2} \mathbf{M} \mathbf{x}
$$

where $\omega$ is the natural frequency and $\omega^{2}$ is the eigenvalues of $\mathbf{M}^{-1} \mathbf{K}$.

## 16. Part II Continuum

### 16.1. 1-D limit

$$
-\frac{d}{d x}\left(\mathbf{C}(\mathbf{x}) \frac{d \mathbf{\Phi}(\mathbf{x})}{d x}\right)=\mathbf{f}
$$

where $\mathbf{C}(\mathbf{x})$ is the conductivity, $\mathbf{\Phi}(\mathbf{x})$ is the voltage, $\mathbf{f}$ is the current source density.

### 16.2. 2-D limit

$$
\begin{gathered}
\phi(x, y)=\operatorname{Re}[h(z)] \\
h(z)=-\frac{m}{2 \pi} \log (f(z))
\end{gathered}
$$

$f(z)$ means the location of the current source. $m$ is the strength of the current source. $\phi$ is the voltage.

To show $\phi$ is harmonic, we have

$$
\phi=\frac{1}{2}(h(z)+\bar{h}(\bar{z}))
$$

we can just show $h(z)$ is harmonic.

$$
J^{(x)}-i J^{(y)}=-\hat{c} h^{\prime}(z)
$$

where $J^{(x)}$ and $J^{(y)}$ are the current density in $x$ and $y$ direction. $\hat{c}$ is the conductivity.

## 17. The total current passing across the boundary

$$
\int_{\text {boundary }} j \cdot n d s
$$

where $j$ is the current density and $n$ is the normal vector. $j . n$ is the normal componet of the current density to the boundary. $d s$ is the differential arclength along the boundary. i.e. $d s=\sqrt{d x^{2}+d y^{2}}$ To calculate $j . n$, we have the dot product in complex form

$$
a . b=\operatorname{Re}[\bar{a} b]=\operatorname{Re}[a \bar{b}]
$$

## 18. Remark

- If any complex potential can be written in the form $h(z)=-\frac{m}{2 \pi} \log \left(z-z_{0}\right)+\hat{h}(z)$, where $\hat{h}(z)$ is not singular at $z_{0}$, then there is a point source of current of strength $m$ at the point $z_{0}$
- A function $p$ is an analytic function if $\frac{\partial p}{\partial \bar{z}}=0$, and so $\frac{d p}{d z}=\frac{\partial p}{\partial z}$, and it is anti-analytic if $\frac{\partial q}{\partial z}=0$ and so $\frac{\partial q}{\partial \bar{z}}=\frac{\partial q}{\partial \bar{z}}$ For analytic functions, $p=p(z)$ and for anti-analytic functions, $q=q(\bar{z})$. If $h(z)$ is analytic then $\overline{h(z)}$ is anti-analytic


## 19. Important relation in complex analysis

- $\log (z)=\log |z|+i \arg (z)$
- $z \bar{z}=|z|^{2}$
