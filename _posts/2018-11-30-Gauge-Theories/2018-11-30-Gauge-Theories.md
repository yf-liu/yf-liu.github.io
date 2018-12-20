---
title: Gauge theories
category: Physics
tags:
  - Topology
  - Gauge theories
---

This note follows [The Geometric Phase in Quantum Systems: Foundations, Mathematical Concepts, and Applications in Molecular and Condensed Matter Physics](https://cds.cern.ch/record/737299/files/3540000313_TOC.pdf).

## Gauge theory of electromagnetism

We consider a non-relativistic (spinless) charged particle subject to an electromagnetic field in three-dimensional Euclidean space $\realset ^ 3$. In the position representation, the particle is described by a scalar wave function $\psi = \psi (\vec{x},t)$ where $\vec{x}\in \realset^3$. The dynamics of the wave function is determined by the Schrödinger equation,

$$
\newcommand{\Hilbert}[1]{\mathscr{#1}}
\newcommand{\dd}{\operatorname{d}}
\newcommand{\op}{\hat}
\newcommand{\id}{\mathbf{I}}
\newcommand{\Tr}[1]{\operatorname{Tr}\left\lbrace#1\right\rbrace}
\newcommand{\realset}{\mathbb{R}}
\newcommand{\intset}{\mathbb Z }
\newcommand{\comset }{\mathbb C }
\newcommand{\innerproduct}[1]{\left\langle #1 \right\rangle}
\renewcommand{\vec}{\mathbf}
\newcommand{\spl}[1]{\langle{#1}\rangle}
\newcommand{\inner}[2]{\left\langle{#1,#2}\right\rangle}
\newcommand{\form}{\tilde}
\newcommand{\abs}[1]{\left\vert{#1}\right\vert}
\newcommand{\bra}[1]{\left\langle{#1}\right\vert }
\newcommand{\ket}[1]{\left| {#1}\right\rangle}
\newcommand{\braket}[2]{\left\langle {#1} \; \middle|\;{#2} \right\rangle }
\newcommand{\mani}{\mathcal}
\newcommand{\field}{\mathscr}
\newcommand{\Tspace}[1]{T\! {#1}}
\newcommand{\D}[2]{\frac{\d {#1}}{\d {#2} }}
\newcommand{\Partial}[2]{\frac{\partial {#1} }{\partial {#2} }}
\newcommand{\op}{\hat}
\newcommand{\uvec}{\hat}
\newcommand{\defas}{: =}
\newcommand{\isdefas}{= :}
\newcommand{\Eqn}[1]{\text{(Eqn. }\ref{#1}\text{)}}
\newcommand{\dual}{\tilde}
\newcommand{\vard}{\mathfrak{d}}
\newcommand{\vare}{\mathfrak{e}}
\newcommand{\e}{\mathrm{e}}
\newcommand{\ii}{\mathrm{i}}
\newcommand{\blue}{\color{blue}}
\newcommand{\red}{\color{red}}
\newcommand{\norm}[1]{\left\|{#1}\right\|}
\newcommand{\set}[1]{\left\lbrace{#1}\right\rbrace}
\newcommand{\sgn}{\operatorname{sgn}}
\newcommand\myeq{\stackrel{\mbox{adiabatic}}{=}}
\newcommand{\avg}[1]{\left\langle {#1} \right\rangle}
\newcommand{\myodot}[1]{\stackrel{#1}{\odot}}
\newcommand{\path}{\mathbf{C}}
\begin{align*}
& \ii \frac{\partial \psi (\vec{x},t)}{\partial t}=H ^ {(el)}\psi(\vec{x},t)
\end{align*}
$$

Here $H ^ {(el)}$ is the Hamiltonian for the particle of the electric charge $e$, in an magnetic field

$$
\vec{E} ^ {(el)} = -\nabla A _ 0 ^ {(el)} - \frac{1}{c}\frac{\partial \vec{A} ^ {(el)}}{\partial t} , \vec{B} ^ {(el)} = \nabla \wedge \vec{A} ^ {(el)}
$$

It is given by 

$$
H ^ {(el)} = \frac{1}{2m} \left(\vec{p}-\frac{e\vec{A}^{(el)}}{c}\right)^2 + e A _ 0 ^ {(el)}
$$

The Hamiltonian contains, in place of the usual canonical momentum $\vec{p}$, the covariant momentum

$$
\pi \defas \vec{p} - \frac{e}{c}\vec{A}^{(el)}
$$

which fulfills the commutation relation

$$
[\pi _ a , \pi _ b]=\ii \frac{e}{c} \epsilon _ {abc}\left(B ^ {(el)}\right)^c
$$

The Schrödinger equation may also be written in the form

$$
(\ii\frac{\partial}{\partial t} - e A ^{(el)} _ 0) \psi = \frac{1}{2m} \left(\frac{1}{\ii}\nabla - \frac{e}{c} \vec{A}^{(el)}\right)^2 \psi
$$

As is well known, the electric field $\vec{E}^{(el)}$ and the magnetic field $\vec{B}^{(el)}$ are unaltered if the potentials are transformed in the following way

$$
\vec{A}^{(el)}\rightarrow\vec{A}^{\prime(el)}=\vec{A}^{(el)}+\nabla\alpha(\vec{x},t) \\
A _ 0 ^{(el)}\rightarrow A _ 0 ^{\prime(el)}=A _ 0 ^{(el)}-\frac{1}{c}\frac{\partial\alpha(\vec{x},t)}{\partial t} \\
$$

They can be viewed as a four-vector $(A ^ \mu)\defas (A ^ {(el)} _ 0, \vec{A}^{(el)})$ in the Minkowski space-time $M^4$ of special relativity. Alternatively they may be used to define a covariant vector field (a one-form),

$$
A ^ {(el)} =A ^ {(el)} _ \mu (x) \dd x ^ \mu
$$

where $x ^ 0 =ct$ and $A ^ {(el)} _ \mu (x)=\eta _ {\mu \nu}A ^ {(el)\nu} (x)$. The Minkowski metric is

$$
\eta = \text{diag}(1,-1,-1,-1)
$$

The transformations takes the form

$$
A ^ {(el)} \rightarrow A ^ {\prime(el)} = A ^ {(el)} - \dd \alpha
$$

where $\dd$ denotes the exterior derivative,

$$
\dd \alpha \defas \partial _ \mu \alpha \dd x ^ \mu = \frac{\partial \alpha}{\partial t} \dd t + \nabla \alpha \cdot \dd \vec{x}
$$

In order that the Schrodinger equation also remains unaltered, the wave function $\psi(\vec{x},t)$ has to undergo the phase transformation.

$$
\psi(\vec{x},t)\rightarrow \psi^\prime (\vec{x},t)=\e^{\ii\frac{e}{c}\alpha(\vec{x},t)}\psi(\vec{x},t)
$$

The combination of the two transformations is called a gauge transformation and the four-vector $(A ^ \mu)$ is called the gauge potential. 

>$$
>\begin{align*}
>& (\ii\frac{\partial}{\partial t} - e A ^{(el)} _ 0) \psi = \frac{1}{2m} \left(\frac{1}{\ii}\nabla - \frac{e}{c} \vec{A}^{(el)}\right)^2 \psi \\
>\text{LHS}& \rightarrow (\ii\frac{\partial}{\partial t} - e A ^{\prime(el)} _ 0) \psi ^ \prime \\
>& = \left(\ii\frac{\partial}{\partial t} - e \left( A ^{(el)} _ 0 - \frac{\partial \alpha}{\partial t} \dd t\right)\right) \e^{\ii\frac{e}{c}\alpha(\vec{x},t)}\psi \\
>& = \left(\ii\frac{\partial}{\partial t} - e A ^{(el)} _ 0 \right) \e^{\ii\frac{e}{c}\alpha(\vec{x},t)}\psi + e \frac{\partial \alpha}{\partial t} \dd t \e^{\ii\frac{e}{c}\alpha(\vec{x},t)}\psi \\
>& = \e^{\ii\frac{e}{c}\alpha(\vec{x},t)} \left(\ii\frac{\partial}{\partial t} - e A ^{(el)} _ 0 \right) \psi \\
>\text{RHS}& \rightarrow \frac{1}{2m} \left(\frac{1}{\ii}\nabla - \frac{e}{c} \vec{A}^{\prime(el)}\right)^2 \psi ^ \prime \\
>& = \frac{1}{2m} \left(\frac{1}{\ii}\nabla - \frac{e}{c}(\vec{A}^{(el)}-\nabla \alpha \cdot \dd \vec{x})\right)^2 \e^{\ii\frac{e}{c}\alpha(\vec{x},t)}\psi \\
>& = \frac{1}{2m} \left(\frac{1}{\ii}\nabla - \frac{e}{c}\vec{A}^{(el)} \right)^2 \e^{\ii\frac{e}{c}\alpha(\vec{x},t)}\psi \\
>& + \frac{1}{2m} \left(\left(\frac{e}{c} \nabla \alpha \cdot \dd \vec{x})\right)^2+ \left(\frac{1}{\ii}\nabla - \frac{e}{c}\vec{A}^{(el)} \right) \left(\frac{e}{c} \nabla \alpha \cdot \dd \vec{x})\right) + \left(\frac{e}{c} \nabla \alpha \cdot \dd \vec{x})\right) \left(\frac{1}{\ii}\nabla - \frac{e}{c}\vec{A}^{(el)} \right)\right) \e^{\ii\frac{e}{c}\alpha(\vec{x},t)}\psi \\
>& = \e^{\ii\frac{e}{c}\alpha(\vec{x},t)} \frac{1}{2m} \left(\frac{1}{\ii}\nabla - \frac{e}{c}\vec{A}^{(el)} \right)^2 \psi \\
>\end{align*}
>$$

If one defines in analogy to the covariant momentum the gauge covariant derivatives $\vec{D}$ and $D _ t$ by

$$
\frac{1}{\ii}\vec{D}=\frac{1}{\ii}\vec{D}(\vec{A}^ {(el)})\defas \frac{1}{\ii}\nabla-\frac{e}{c}\vec{A}^{(el)} \\
\ii D _ t=\frac{1}{\ii}D _ t(A _ 0^ {(el)})\defas \ii \frac{\partial}{\partial t}-e A _ 0^{(el)}
$$

then one can write the Schrodinger equation as 

$$
\ii D _ t \psi = \frac{-1}{2m} \vec{D} ^ 2 \psi
$$

The transformation can also be written in the terms of the covariant derivatives.
One may also define the covariant four-derivative $D (A^{(el)})$ with the components

$$
D _ \mu (A ^ {(el)}) \defas \partial _ \mu +\frac{\ii e}{c} A ^ {(el)} _ \mu \\
$$

where $D _ 0 = D _ t$. The transformation property is

$$

D _ \mu (A ^ {\prime (el)}) \e ^ {\ii \frac{e}{c} \alpha} \psi (\vec{x},t) = \e ^ {\ii \frac{e}{c} \alpha} D _ \mu (A ^ {(el)}) \psi (\vec{x},t) \\
D _ \mu (A ^ {\prime (el)}) \psi ^ \prime (\vec{x},t) = \e ^ {\ii \frac{e}{c} \alpha} D _ \mu (A ^ {(el)}) \psi (\vec{x},t) \\
D _ \mu (A ^ {\prime (el)}) = \e ^ {\ii \frac{e}{c} \alpha} D _ \mu (A ^ {(el)}) \e ^ {-\ii \frac{e}{c} \alpha}
$$

This equation indicates that the operators $D _ \mu$ transform covariantly under the gauge transformation, hence the name covariant derivative. They are directly linked to the electromagnetic field strengh $(\vec{E}^{(el)},\vec{B}^{(el)})$.

$$
[D _ \mu , D _ \nu] =\frac{\ii e}{c} (\partial _ \mu A _ \nu ^ {(el)} - \partial _ \nu A _ \mu ^ {(el)}) \isdefas \frac{\ii e}{c} F _ {\mu\nu} ^ {(el)} \\
F _ {0a} ^ {(el)} = (E^{(el)})^a,F _ {ab} ^ {(el)} =-\epsilon _ {abc} (B^{(el)})^c
$$

In order to generalize the above gauge theory we introduce the following notation

$$
\mathcal{U}(\alpha(\vec{x},t)) \defas \e ^ {\ii \frac{e}{c}\alpha(\vec{x},t)}
$$

Then the transformation is written as

$$
\begin{align*}
\psi(\vec{x},t) & \rightarrow\psi^\prime(\vec{x},t)=\mathcal{U}(\alpha(\vec{x},t)) \psi(\vec{x},t) \\
D _ \mu (A ^ {(el)}) \psi & \rightarrow D _ \mu (A ^ {\prime(el)}) \psi^\prime=\mathcal{U}(\alpha) (D _ \mu (A ^ {(el)}) \psi) \\
D _ \mu (A ^ {(el)}) & \rightarrow D _ \mu (A ^ {\prime(el)}) =\mathcal{U}(\alpha) (D _ \mu (A ^ {(el)}) \mathcal{U}^{-1}(\alpha)) \\
A ^ {(el)} & \rightarrow A ^ {\prime(el)}=\mathcal{U}(\alpha) A ^ {(el)} \mathcal{U}^{-1}(\alpha)-\frac{\ii c}{e}\mathcal{U}(\alpha) \dd \mathcal{U}^{-1}(\alpha)=A ^ {(el)} -\dd\alpha
\end{align*}
$$

>$$
>\begin{align*}
>A ^ {\prime(el)} & =\mathcal{U}(\alpha) A ^ {(el)} \mathcal{U}^{-1}(\alpha)-\frac{\ii c}{e}\mathcal{U}(\alpha) \dd \mathcal{U}^{-1}(\alpha)\\
>& =\e ^ {\ii \frac{e}{c}\alpha(\vec{x},t)} A ^ {(el)} \e ^ {-\ii \frac{e}{c}\alpha(\vec{x},t)}-\frac{\ii c}{e}\e ^ {\ii \frac{e}{c}\alpha(\vec{x},t)} \dd \e ^ {-\ii \frac{e}{c}\alpha(\vec{x},t)}\\
>& =A ^ {(el)}-\frac{\ii c}{e}\e ^ {\ii \frac{e}{c}\alpha(\vec{x},t)}  \e ^ {-\ii \frac{e}{c}\alpha(\vec{x},t)}(-\ii \frac{e}{c}\dd\alpha(\vec{x},t))\\
>& = A ^ {(el)} -\dd\alpha
>\end{align*}
>$$

A gauge transformation is associated with a function

$$
\mathcal{U}:M^4\rightarrow U(1)
$$

The set of all gauge transformations also form a Lie group. This is called the group of gauge transformation.

## General gauge theory





## References

[1] Bohm, Arno, et al. *The Geometric Phase in Quantum Systems: Foundations, Mathematical Concepts, and Applications in Molecular and Condensed Matter Physics*. Springer Science & Business Media, 2013.