---
title: Fiber bundles
category: Physics
tags:
  - Topology
  - Berry phase
  - Cyclic evolution
---

This note follows [The Geometric Phase in Quantum Systems: Foundations, Mathematical Concepts, and Applications in Molecular and Condensed Matter Physics](https://cds.cern.ch/record/737299/files/3540000313_TOC.pdf).

## From quantal phases to fiber bundles

### Fiber bundles

---

Any fiber bundle consists of a base manifold $X$, a set of fibers and a total space $E$. All of the fibers are diffeomorphic copies of a smooth manifold $F$ of dimension $\mathcal{N}$ which is called the typical fiber. The integer $\mathcal{N}$ is called the fiber dimension or the rank of the bundle. Any point $p\in E$ projects on one of the fibers $F _ x$ through a projection map.

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
& \pi : E \rightarrow X \\
& \pi (p) \defas x \text{  if and only if  } p \in F _ x
\end{align*}
$$

| Property                                                     | Diagram                                                      |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Given two manifolds $M$ and $N$, a differentiable map $f : M → N$ is called a **diffeomorphism** if it is a bijection and its inverse $f ^ {−1} : N → M$ is differentiable as well. If these functions are $r$ times continuously differentiable, $f$ is called a $C _ r$-diffeomorphism. | <img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-30-Fiber-Bundles/assets/diffeomorphism.png" width="100%"> |
| The fiber $F _ x$ over $x$ as the inverse image of $x$ under $\pi$, $F _ x = \pi ^ {-1} (x)$. | <img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-30-Fiber-Bundles/assets/inverse_image.png" width="100%"> |
| The projection map is an onto function, so that there are fibers over all the points of $X$. |                                                              |
| The projection map is a smooth (continuous) function. A smooth curve in $E$ projects to smooth curve in $X$. | <img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-30-Fiber-Bundles/assets/smooth.png" width="100%"> |
| The fiber bundle is locally the Cartesian product of an open subset of the base manifold $X$ and the typical fiber $F$. For any point $x \in X$, there is an open neighborhood $U _ x$ of $x$, such that $\pi ^ {-1} (U _ x) \simeq U _ x \times F$. | <img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-30-Fiber-Bundles/assets/local.png" width="100%"> |

All the manifolds of the same finite dimension are locally identical, while the global structure distinguishes it from others of the same dimension. It depends on how to glue the open neighborhood to construct the manifold, which stored in transition or overlap functions. To see this, let us cover the manifold $X$ with a set of open patches. These are subsets $O _ \alpha$ of $X=\cup _ \alpha O _ \alpha$ each of which is diffeomorphic to $\realset ^ m$. Thus for each $O _ \alpha$, there is a diffeomorphism $\varphi _ \alpha : O _ \alpha \rightarrow \realset ^ m$ which identifies $O _ \alpha$ with its image $\varphi _ \alpha (O _ \alpha)$ in $\realset ^ m$:

$$
O _ \alpha \simeq \varphi _ \alpha (O _ \alpha) \subseteq \realset ^ m
$$

>Consider the sphere of unit radius in $\realset ^ 3$. We parametrize the surface of $S ^ 2$ by stereographic coordinates. Stereographic coordinates can be defined by the projection from the North or South Pole onto the equatorial plane.
>
>$$
>\begin{align*}
>& \varphi _ \alpha : O _ \alpha \rightarrow \realset ^ 2, \alpha = N , S\\
>& O _ S (P \ne N):  X _ S = \frac{x}{1 - z}, Y _ S =\frac{y}{1 - z} \\
>& O _ N (P \ne N):  X _ N = \frac{x}{1 + z}, Y _ N =\frac{y}{1 + z} \\
>\end{align*}
>$$
>
><img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-30-Fiber-Bundles/assets/Stereographic.png" width="80%">

On the overlap $O _ \alpha \cap O _ \beta$ of two patches, the image $\varphi _ \alpha (O _ \alpha \cap O _ \beta)$ and $\varphi _ \beta(O _ \alpha \cap O _ \beta)$ are related by overlap function. 

$$
g _ {\alpha \beta} \defas \varphi _ \alpha \circ \varphi _ \beta ^ {-1}
$$

>In the previous sphere, the transition function is
>
>$$
> g _ {SN} = \varphi _ S \circ \varphi _ N ^ {-1} = \begin{pmatrix}
> \frac{1 + z}{1 - z} & 0 \\
> 0 & \frac{1 + z}{1 - z} \\
> \end{pmatrix}\\
> \varphi _ S = g _ {SN} \varphi _ N \\
>  \begin{pmatrix}
> \frac{x}{1 - z} \\
> \frac{y}{1 - z} \\
> \end{pmatrix} = \begin{pmatrix}
> \frac{1 + z}{1 - z} & 0 \\
> 0 & \frac{1 + z}{1 - z} \\
> \end{pmatrix} \begin{pmatrix}
> \frac{x}{1 + z} \\
> \frac{y}{1 + z} \\
> \end{pmatrix}
>$$
>
><img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-30-Fiber-Bundles/assets/transformation_function.png" width="40%">

Since we divide the base manifold $X$ into a collection $\set{U _ \alpha}$ of its open subsets, there exist diffeomorphisms

$$
\Phi _ \alpha : \pi ^ {-1} (U _ \alpha) \rightarrow U _ \alpha \times F
$$

The pair $(U _ \alpha , \Phi _ \alpha)$ is called a chart or a local trivialization of the bundle $E$. If we restrict $\Phi _ \alpha$ to a point $x \in U _ \alpha$, we will obtain a diffeomorphism from the fiber $F _ x$ onto the typical fiber $F$.

$$
\Phi _ \alpha (x) \defas \Phi _ \alpha \vert _ \set{x} : F _ x \rightarrow \set{x} \times F \equiv F 
$$

The transition functions for the fiber bundle $E$ is

$$
G _ {\alpha \beta} (x) \defas \Phi _ \alpha (x) \circ \Phi _ \beta ^ {-1} (x) : F \rightarrow F
$$

The transition functions for the fiber bundle has two properties.

$$
G _ {\alpha \beta} (x) = G ^ {-1} _ {\beta \alpha} (x) \quad \forall x \in U _ \alpha \cap U _ \beta \\ 
G _ {\alpha \beta} (x) \circ G _ {\beta \gamma} (x) \circ G _ {\gamma \alpha} (x) = 1 \quad \forall x \in U _ \alpha \cap U _ \beta \cap U _ \gamma \\ 
$$

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-30-Fiber-Bundles/assets/transformation_function_fiber.png" width="90%">

The diffeomorphism preserving the bundle structure is a bundle map or a bundle morphism $\mathcal{F} : E _ 1 \rightarrow E _ 2$, which maps the fibers of $E _ 1$ into the fibers of $E _ 2$. Induce a smooth function $f : X _ 1 \rightarrow X _ 2$, there exists

$$
\begin{matrix}
E _ 1 & \stackrel{\mathcal{F}}{\rightarrow} & E _ 2\\
\left . \pi _ 1 \right \downarrow & \bigcirc & \left \downarrow \pi _ 2 \right . \\
X _ 1 & \stackrel{f}{\rightarrow} & X _ 2\\
\end{matrix}
$$

If a bundle morphism is also a diffeomorphism, then it is called a bundle isomorphism. The isomorphic bundles are then viewed as equivalent bundles.

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-30-Fiber-Bundles/assets/commutative_diagram.png" width="40%">

A trivial bundle is basically the product manifold of two smooth manifolds.

$$
E \simeq X \times F
$$

The sections of the fiber bundles are $s (x)$.

$$
\pi (s (x)) = x , \forall x \in U \subseteq X
$$

If the domain $U$ of such a function is not the entire base manifold, the section is local section, otherwise it is global section.

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-30-Fiber-Bundles/assets/section.png" width="30%">

### Vector bundles

A vector bundle $(E , X , \pi , G)$ is a fiber bundle whose fibers $V _ x$ and typical fiber $V= \comset ^ \mathcal{N} $(respectively $V= \realset ^ \mathcal{N} $) are complex(real) vector spaces and whose structure group $G$ is the general linear group $GL (\mathcal{N}, \comset)$(respectively $GL (\mathcal{N}, \realset)$).

Mobius strip is a nontrivial fiber bundle. We cover $S _ 1$ by two coordinate patches:

$$
U _ + \defas \set{\theta | - \epsilon < \theta < \pi + \epsilon} , U _ - \defas \set{\theta | \pi - \epsilon < \theta < \epsilon}
$$

Let the typical fiber be an interval of the real line $F \defas [- 1 , 1] \subset \realset$, parameterized by $t \in [- 1 , 1]$. We have to glue together two pieces, 

$$
U _ + \times F \text{, parametrized by } (\theta , t _ +) \\
U _ - \times F \text{, parametrized by } (\theta , t _ -)
$$

Take the two element group $\set{e , - e}$ as a structure group $G = \intset _ 2$.

$$
G _ {+ -} (x) \defas \begin{cases}
e , x \in A \\
- e , x \in B
\end{cases}
$$

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-30-Fiber-Bundles/assets/mobius.png" width="90%">

### Principle fiber bundle

A principle fiber bundle is a fiber bundle whose typical fiber and the structure group are identical, i.e., they are diffeomorphic as smooth manifolds. Consider a PFB $(P , X , \pi , G)$, with $\pi  ^ {-1} (x) = F _ x \simeq G, \forall x \in X$, and a complete set of local trivializations $\set{(U _ \alpha , \Phi _ \alpha)}$. The transition functions $G _ {\alpha \beta} (x) \in G$, act on the typical fiber $F = G$  by group multiplication from the left.

$$
g _ 1 \stackrel{G _ {\alpha \beta}}{\rightarrow} g _ 2 \defas G _ {\alpha \beta} (x) \bullet g _ 1 , \quad g _ 1 , g _ 2 \in F = G
$$

$G$ has a right action $R : G \times P \rightarrow P$,

$$
R (g , p _ 1) \isdefas R _ g (p _ 1), \quad \forall g \in G , \forall p _ 1 \in P
$$

on the total space $P$ that is defined by

$$
p _ 1 \stackrel{G _ {\alpha \beta}}{\rightarrow} p _ 2 = R _ g (p _ 1) \defas \Phi _ \alpha ^ {-1} (x) [\Phi _ \alpha (x)[p _ 1] \bullet g]
$$

where $x \defas \pi (p _ 1)$ and $\bullet$ denotes the group multiplication in $G$. In this way the right action of $G$ moves the points of $P$ within individual fibers. The definition is independent of the choice of the local chart. We can think of the group $G$ as being an action which pushes points in the bundle around the bundle along the fibers. There is a rather confusing but widely used notation:
$$
p _ 2 \defas R _ g (p _ 1) = p _ 1 \cdot g
$$

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-30-Fiber-Bundles/assets/right_action.png" width="80%">

>The definition of right action is independent of the choice of the local chart.
>
>$$
>\begin{align*}
>[p _ 1] \bullet g & = \Phi ^ {-1} _ \alpha (x) \Phi _ \alpha (x) \Phi _ \beta ^ {-1} (x) [\Phi _ \beta (x)[p _ 1] \bullet g] \\
>\Phi _ \alpha (x)[p _ 1] \bullet g & = \Phi _ \alpha (x) \Phi _ \beta ^ {-1} (x) [\Phi _ \beta (x)[p _ 1] \bullet g] \\
>\Phi _ \alpha ^ {-1} (x) [\Phi _ \alpha (x)[p _ 1] \bullet g] & =\Phi _ \beta ^ {-1} (x) [\Phi _ \beta (x)[p _ 1] \bullet g] \\
>\end{align*}
>$$
>

The action is both transitive and free.

- Transitivity: Every pair of points $p _ 1$ and $p _ 2$ of a fiber $F _ x$ can be connected via a group element $g$, there is some $g \in G$ such that $p _ 2 = p _ 1 \cdot g$.
- Freedom: There is no group element besides the identity element that leaves all the points of a fiber unchanged.

The simplest type of PFBs are the trivial principle fiber bundles. A typical example is the two-dimension torus $T ^ 2 = S ^ 1 \times S ^ 1$.

## Geometry of principal bundles and the concept of holonomy

### Tangent bundles

Aa tangent bundle $TM$ over an $m$-dimensional manifold $M$ is a collection of all the tangent spaces of $M$:

$$
TM \equiv \bigcup _ {p \in M} T _ p M
$$

The manifold $M$ is base space. If $x ^ \mu = \varphi _ i (p)$ is the coordinate on $U _ i$, an element of $T U _ i \equiv \bigcup _ {p \in U _ i} T _ p U _ i$ is specified by a point $p \in M$ and a vector $V = V ^ \mu _ p \left.\left( \frac{\partial}{\partial x ^ \mu} \right) \right\vert _ p \in T _ p M$. 

| Manifold  | Dimension | Coordinate            |
| --------- | --------- | --------------------- |
| $M$       | $m$       | $x ^ \mu$             |
| $T _ p M$ | $m$       | $V^ \mu$              |
| $T M$     | $2m$      | $(x ^ \mu , V ^ \mu)$ |

However, the tangent bundle itself is not always expressed as direct product $\realset ^ m \times \realset ^ m$ and the non-trivial structure of the tangent bundle measures the topological nontriviality of $M$. To see this, we have to look not only at a single chart $U _ i$ but also at another one. Take a vector $V \in T _ p M$ where $p \in U _ i \cap U _ j$. $V$ has two coordinate presentations,

$$
\begin{align*}
V ^ \mu \left. \frac{\partial}{\partial x ^ \mu} \right\vert _ p & = \tilde{V} ^ \nu \left. \frac{\partial}{\partial y ^ \nu} \right\vert _ p \\
\tilde{V} ^ \nu & = \left. \frac{\partial y ^ \nu}{\partial x ^ \mu} \right\vert _ p V ^ \mu \\
\tilde{V} ^ \nu & = G ^ \nu _ \mu V ^ \mu \\
\end{align*}
$$

where $G ^ \nu _ \mu \equiv \frac{\partial y ^ \nu}{\partial x ^ \mu} \in G$ is the element of structure group of $TM$.

> Let us work out $TS ^ 2$. Let the pair $O _ N \equiv S ^ 2 - \set{S}$ and $O _ S \equiv S ^ 2 - \set{N}$ be an open covering of $S ^ 2$. 
>
> $$
> \begin{align*}
> & O _ S (P \ne N):  X _ S = \frac{x}{1 - z}, Y _ S =\frac{y}{1 - z} \\
> & O _ N (P \ne N):  X _ N = \frac{x}{1 + z}, Y _ N =\frac{y}{1 + z} \\
> & X _ N = \frac{X _ S}{X ^ 2 _ S + Y ^ 2 _ S} , Y _ N = - \frac{Y _ S}{X ^ 2 _ S + Y ^ 2 _ S} \\
> & G ^ S _ N \equiv \frac{\partial (X _ N , Y _ N)}{\partial (X _ S , Y _ S)} = \begin{pmatrix}
> \frac{\partial X _ N}{\partial X _ S} & \frac{\partial X _ N}{\partial Y _ S} \\
> \frac{\partial Y _ N}{\partial X _ S} & \frac{\partial Y _ N}{\partial Y _ S} \\
> \end{pmatrix} \\
> & \quad = \begin{pmatrix}
> - \frac{X ^ 2 _ N - Y ^ 2 _ N}{(X ^ 2 _ N + Y ^ 2 _ N) ^ 2} & - \frac{2 X _ N Y _ N}{(X ^ 2 _ N + Y ^ 2 _ N) ^ 2} \\
> \frac{2 X _ N Y _ N}{(X ^ 2 _ N + Y ^ 2 _ N) ^ 2} & - \frac{X ^ 2 _ N - Y ^ 2 _ N}{(X ^ 2 _ N + Y ^ 2 _ N) ^ 2} \\
> \end{pmatrix} \\
> & \quad =
> \frac{1}{r ^ 2} \begin{pmatrix}
> - \cos 2 \varphi & - \sin 2 \varphi \\
> \sin 2 \varphi & - \cos 2 \varphi \\
> \end{pmatrix} \\
> \tilde{V} ^ S & = G ^ S _ N V ^ N =  \frac{1}{r ^ 2} \begin{pmatrix}
> - \cos 2 \varphi & - \sin 2 \varphi \\
> \sin 2 \varphi & - \cos 2 \varphi \\
> \end{pmatrix} V ^ N\\
> \end{align*}
> $$
>
><img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-30-Fiber-Bundles/assets/tangent_bundle.png" width="80%">

### Parallelism

The way to determine uniquely the parallel vector $v _ 1$ at the point of $x _ 1$ to $v _ 2$ at the point of $x _ 2$ :

- A path $C _ X$ connecting these two points, where $x _ 1 = C _ X (t = 0) , x _ 2 = C _ X (t = T)$.
- A point $x$ which is nearby $x _ 2$: $x \defas C _ X (t = T - \dd t)$.
- Imagine the manifold $TM$ is imbedded in a Euclidean space $\realset ^ d (T \realset ^ d = \realset ^ d)$ and view $C _ X$ as sitting inside $\realset ^ d$.
- Treat the vector $v _ 2$ as an element of $\realset ^d$ and find the parallel vector to $v _ 2$ at the point of $x$.
- Choose the component of it which is tangent to $T _ p M$ and discard the normal component.
- Repeat the process till the point $x _1$.

The above procedure ensures that:

- Reflexivity: Every vector is parallel to itself.
- Symmetry: If $v _ 1$ is parallel to $v _ 2$, $v _ 2$ is parallel to $v _ 1$.(same path)
- Transitivity: If $v _ 1$ is parallel to $v _ 2$ and $v _ 2$ is parallel to $v _ 3$, it results in that $v _ 1$ is parallel to $v _ 3$.

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-30-Fiber-Bundles/assets/parallelism.png" width="30%">

### Parallelism and principle fiber bundle

Consider a PFB $P: (P , X , \pi , G)$ and a smooth curve $C _ X$ in $X$ with parameter $t \in [0 , T]$. We will view the concept of parallel transportation on $P$ as a means to find a curve $C _ P$ in the total space $P$ that follows the curve $C_ X$, such that

- $C _ P$ projects onto $C _ X$ under the projection $\pi : P \rightarrow X$.
- The tangent vectors $\omega _ t \in T P$ to $C _ P$ project onto the tangent vectors $v _ t \in T X$ to $C _ X$ under the push-forward(differential) map $\pi _ * : T P \rightarrow T X$.

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-30-Fiber-Bundles/assets/Cp.png" width="80%">

The structure that enables one to determine the curve $C _ P : t \longrightarrow p(t) \in P$ uniquely for a given curve $C _ X : t \longrightarrow x(t) \in P$ and a initial condition $p (0) \in F _ {x(0)}$, is a geometry or a connection on the PFB $P$. The curve $C _ P$ is the horizon lift of $C _ X$ associated with this connection. The tangent vectors $\omega _ t$ to $C _ P$ are the horizontal vectors. 

At any point $q$, the tangent space $T _ p P$ to the bundle can be decomposed into two spaces, one parallel to the fiber, called the vertical subspace $V _ p P$, and one transverse to the fiber, called the horizontal space $H _ p P$.
$$
T _ p P = V _ p P \oplus H _ p P
$$
The vertical space is defined uniquely by 
$$
V _ p P = \ker (\pi _ *)
$$



## References

[1] Bohm, Arno, et al. *The Geometric Phase in Quantum Systems: Foundations, Mathematical Concepts, and Applications in Molecular and Condensed Matter Physics*. Springer Science & Business Media, 2013.