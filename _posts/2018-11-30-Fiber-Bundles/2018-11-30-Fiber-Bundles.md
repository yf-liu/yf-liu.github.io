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

where $x \defas \pi (p _ 1)$ and $\bullet$ denotes the group multiplication in $G$. In this way the right action of $G$ moves the points of $P$ within individual fibers. The definition is independent of the choice of the local chart. There is a rather confusing but widely used notation:

$$
p _ 2 \defas R _ g (p _ 1) = p _ 1 \cdot g
$$

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-30-Fiber-Bundles/assets/right_action.png" width="90%">




## References

[1] Bohm, Arno, et al. *The Geometric Phase in Quantum Systems: Foundations, Mathematical Concepts, and Applications in Molecular and Condensed Matter Physics*. Springer Science & Business Media, 2013.