---
layout: simple
title: An Introduction to Applied Mathematics Memory Sheet
---

#### Based on the notes and lectures of [Prof. Darren Crowdy](https://www.ma.ic.ac.uk/~dgcrowdy/).

## 1. Part I Graphs

### 1.1. Graphs

####  Definition (Incidence Matrix)

Let $$G$$ be a graph with $$n$$ nodes and $$$$m$$$$ edges. The incidence matrix $$A$$ of $$$$G$$$$ is an $$m \times n$$ matrix, where the number of nodes is the number of columns and the number of edges is the number of rows.

####  Theorem (Rank nullity theorem)

For an $$m \times n$$ incidence matrix $$A$$, we have

- $$\dim\text{(right null space)} + \text{rank} (A)=n \text{(the number of nodes)}$$
- $$\dim\text{(left null space)} + \text{rank} (A)=m \text{(the number of edges)}$$


####  The geometric interpretation of the rank nullity theorem

- $$\dim\text{(right null space)}$$ is the number of connected components in the graph. Therefore, for a connected graph, $$\dim\text{(right null space)}=1$$.
- $$\dim\text{(left null space)}$$ is the number of independent loops in the graph.


### 1.2 Circuits

The vector of potential differences

$$
\mathbf{e}=\mathbf{A x}
$$

The vector of edge fluxeslcurrents (Ohm's law)

$$
\mathbf{w}=-C \mathbf{A} \mathbf{x}
$$

where $$C$$ is the diagonal matrix of edge conductances.

The vector of fluxes out of each node(divergence) of fluxes at each node
 
$$
\mathbf{f}=-\mathbf{A}^{\mathrm{T}} \mathbf{w}=\mathbf{A}^{\mathrm{T}} \mathbf{C A \mathbf { x }}
$$

####  If the conductance is unit

$$
\mathrm{w}=-\mathrm{e}=-A \mathrm{x}
$$

$$
\mathrm{f}=A^{T} A \mathrm{x}
$$

#### Laplacian matrix

$$
\begin{gathered}
\mathbf{K}=\mathbf{A}^{T} \mathbf{A} \\
\mathbf{K} \mathbf{x}=\mathbf{f}
\end{gathered}
$$
#### The linearity of the the voltage and current

If we change the voltage source from $$V$$ to $$V^{\prime}$$ propotionally, then the voltage and current change propotionally.
#### Definition (Effective conductance)

The divergence of fluxes at the node with unit voltage source.

#### Definition (Harmonic potential)

A harmonic potential is a potential at node $$i$$ that is the avarage of the potentials of its neighbors.

#### Remark

- The maximum and minimum possible values of the potentials in a connected graph occurs at the boundary node.
- The uniqueness principle for harmonic potentials: the harmonic potential is unique. Given the same potentials at boundary nodes, the harmonic potential is the same.


### 1.3 Random walks

#### Definition ($$p_{i}$$ Hitting Probability)

$$p_{i}$$ is the probability that a random walk starting at node $$i$$ to reach the + node where $$p_{+}=1$$ before returning to node $$-$$ where $$p_{-}=0$$.

$$p_{i}$$ can be regraded as the potential of node $$i$$ with the node + and - as the boundary nodes.

#### Definition (Escape probability)

If the random walk starts at node $$i, p_{e s c}$$ is the probability that the random walk reaches the boundary node $$+$$ before returning to node $$i$$. (The nodes that he starts and the nodes that he don't want to return before reaching the target nodes)

$$
p_{e s c}=\frac{C_{e f f}}{n}
$$

where $$C_{e f f}$$ is the effective conductance of node $$+$$ (where he starts) to the boundary node $$-$$ (where he wants to reach).

$$n$$ is the total number of edges connected with the node he starts .

### 1.4 Spring mass systems

#### Theorem (Hook's law)

$$
\mathbf{T}=\mathbf{C A x}
$$

where $$\mathbf{T}$$ is the internal spring forces, $$\mathbf{C}$$ is the spring constant matrix $$\mathbf{A}$$ is the incidence matrix, $$\mathbf{x}$$ is the displacement.

#### Theorem (Newton's second law)

$$
\mathbf{f}-\mathbf{K} \mathbf{x}=\mathbf{M} \frac{d^{2} \mathbf{x}}{d t^{2}}
$$

where $$\mathbf{M}$$ is the mass matrix, $$\mathbf{f}$$ is the external forces, $$\mathbf{K}$$ is the Laplacian matrix. $$\mathbf{x}$$ is the displacement.

If the system is in equilibrium, then

$$
\mathbf{K} \mathbf{x}=\mathbf{f}
$$

#### Calculating the natural frequencies

Since it is in the equilibrium, we have to ignore the external forces $$\mathbf{f}$$. Therefore, we have

$$
-\mathbf{K} \mathbf{x}=\mathbf{M} \frac{d^{2} \mathbf{x}}{d t^{2}}
$$

Set $$\mathbf{x}=\mathbf{x} e^{i \omega t}$$, then we have

$$
\mathbf{K} \mathbf{x}=\omega^{2} \mathbf{M} \mathbf{x}
$$

where $$\omega$$ is the natural frequency and $$\omega^{2}$$ is the eigenvalues of $$\mathbf{M}^{-1} \mathbf{K}$$.

## Part II Continuum

### 2.1 1-D limit

$$
-\frac{d}{d x}\left(\mathbf{C}(\mathbf{x}) \frac{d \mathbf{\Phi}(\mathbf{x})}{d x}\right)=\mathbf{f}
$$

where $$\mathbf{C}(\mathbf{x})$$ is the conductivity, $$\mathbf{\Phi}(\mathbf{x})$$ is the voltage, $$\mathbf{f}$$ is the current source density.

### 2.2 2-D limit

$$
\begin{gathered}
\phi(x, y)=\operatorname{Re}[h(z)] \\
h(z)=-\frac{m}{2 \pi} \log (f(z))
\end{gathered}
$$

$$f(z)$$ means the location of the current source. $$m$$ is the strength of the current source. $$\phi$$ is the voltage.

To show $$\phi$$ is harmonic, we have

$$
\phi=\frac{1}{2}(h(z)+\bar{h}(\bar{z}))
$$

we can just show $$h(z)$$ is harmonic.

$$
J^{(x)}-i J^{(y)}=-\hat{c} h^{\prime}(z)
$$

where $$J^{(x)}$$ and $$J^{(y)}$$ are the current density in $$x$$ and $$y$$ direction. $$\hat{c}$$ is the conductivity.

#### The total current passing across the boundary

$$
\int_{\text {boundary }} j \cdot n d s
$$

where $$j$$ is the current density and $$n$$ is the normal vector. $$j . n$$ is the normal componet of the current density to the boundary. $$d s$$ is the differential arclength along the boundary. i.e. $$d s=\sqrt{d x^{2}+d y^{2}}$$ To calculate $$j . n$$, we have the dot product in complex form

$$
a . b=\operatorname{Re}[\bar{a} b]=\operatorname{Re}[a \bar{b}]
$$

#### Remark

- If any complex potential can be written in the form $$h(z)=-\frac{m}{2 \pi} \log \left(z-z_{0}\right)+\hat{h}(z)$$, where $$\hat{h}(z)$$ is not singular at $$z_{0}$$, then there is a point source of current of strength $$m$$ at the point $$z_{0}$$
- A function $$p$$ is an analytic function if $$\frac{\partial p}{\partial \bar{z}}=0$$, and so $$\frac{d p}{d z}=\frac{\partial p}{\partial z}$$, and it is anti-analytic if $$\frac{\partial q}{\partial z}=0$$ and so $$\frac{\partial q}{\partial \bar{z}}=\frac{\partial q}{\partial \bar{z}}$$ For analytic functions, $$p=p(z)$$ and for anti-analytic functions, $$q=q(\bar{z})$$. If $$h(z)$$ is analytic then $$\overline{h(z)}$$ is anti-analytic


#### Important relations in complex analysis

$$
\log (z)=\log |z|+i \arg (z)
$$

$$
z \bar{z}=|z|^2
$$
