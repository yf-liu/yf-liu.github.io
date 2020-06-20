---
title: Cohomology
category: Physics
tags:
  - C* algebra
---

$$
\begin{align*}
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
\end{align*}
$$

## Homology

The homology groups, refinements of the Euler characteristic, could classify the space. Our guiding principle is to find a region without boundaries, which is not itself a boundary of some region.

### simplexes and simplicial complexes

`Def`: r-simplex $\sigma$ is an r-dim object containing $r+1$ points $p_i$. It is expressed as 
$$
\sigma^r=\langle p_0p_1\cdots p_r\rangle=\{x\in \mathbb{R}^m| x=\sum_{i=0}^r c_i p_i, c_i\ge 0, \sum_{i=0}^r c_i=1\}
$$

| r    | r-simplex                                                    | 0-face                                                       | 1-face                                                       | 2-face                                                       |
| ---- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 0    | <img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex0.png" width="30%"> | 1*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex0.png" width="30%"> |                                                              |                                                              |
| 1    | <img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex1.png" width="30%"> | 2*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex0.png" width="30%"> | 1*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex1.png" width="30%"> |                                                              |
| 2    | <img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex2.png" width="30%"> | 3*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex0.png" width="30%"> | 3*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex1.png" width="30%"> | 1*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex2.png" width="30%"> |
| 3    | <img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex3.png" width="30%"> | 4*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex0.png" width="30%"> | 6*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex1.png" width="30%"> | 4*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex2.png" width="30%"> |

`Def`: A set of finite number of simplexes in $\mathbb{R}^m$ is called a simplicial complex $K$ if 

(i) $\sigma\in K,\sigma^\prime\le\sigma\Rightarrow \sigma^\prime\in K$, and 

(ii) $\sigma,\sigma^\prime\in K\Rightarrow \sigma\cap\sigma^\prime\le \sigma(^\prime) \text{ or } \sigma\cap\sigma^\prime=\emptyset$.



`Example`: $K=\{\sigma,\sigma\le\sigma^2=\langle p_0 p_1 p_2\rangle\}=\{p_0,p_1,p_2,\langle p_0 p_1\rangle,\langle p_1 p_2\rangle,\langle p_2 p_0\rangle,\langle p_0 p_1 p_2\rangle\}$. 

`Def`: An oriented r-simplex $\sigma_r=(p_0p_1\cdots p_r)$ is a r-simple $\sigma^r=\langle p_0p_1\cdots p_r\rangle$ with a prescribed orientation.  We define $(p_{i_0}p_{i_1}\cdots p_{i_r})=\sgn(P)(p_0p_1\cdots p_r)$ with a permutation $P=\left(\begin{matrix}0&1&\cdots &r\newline i_0 & i_1 & \cdots& i_r\end{matrix}\right)$.

### chain group, cycle group and boundary group

`Example`: $K=\{\sigma, \sigma\le\langle p_0 p_1 p_2 p_3\rangle\}$.

| r    | r-chain group $C_r(K)$                                                         |                                                          |                                                          | r-cycle group $Z_r(K)=\ker\partial_r$ |        |        | r-boundary group $B_r(K)=\text{im} \partial_{r+1}$ |        |        |
| ---- | ------------------------------------------------------------ | ---------------- | ---------------------- | ---- | ---- | ---- | ---- | ---- | ---- |
|      | generator                                          | element                          |                           | def | example |  | def | example |  |
| 0 | 4*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex0.png" width="50%"> | $c_1p_0+c_2p_1+\cdots$ | $C_0(K)=\mathbb{Z}^4$ |  | $p_0$ | $Z_0(K)=\mathbb{Z}^4$ | $\exists d\in C_1(K), c=\partial_1 d$ | $p_0-p_1$ | $B_0(K)=\mathbb{Z}^3$ |
| 1    | 6*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/oriented1.png" width="100%"> | $c_1 (p_0p_1)+c_2(p_1p_2)+\cdots$ | $C_1(K)=\mathbb{Z}^6$ | $\partial_1 c=0$ | $(p_0p_1)+(p_1p_2)+(p_2p_0)$ | $Z_1(K)=\mathbb{Z}^3$ | $\exists d\in C_2(K), c=\partial_2 d$ | $(p_0p_1)+(p_1p_2)+(p_2p_0)$ | $B_1(K)=\mathbb{Z}^3$ |
| 2    | 4*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/oriented2.png" width="100%"> | $c_1 (p_0p_1p_2)+c_2(p_1p_2p_3)+\cdots$ | $C_2(K)=\mathbb{Z}^4$ | $\partial_2 c=0$ | $(p_0p_1p_2)-(p_1p_2p_3)+(p_2p_3p_0)-(p_3p_0p_1)$ | $Z_1(K)=\mathbb{Z}$ | $\exists d\in C_3(K), c=\partial_3 d$ | $-(p_0p_1p_2)+(p_1p_2p_3)-(p_2p_3p_0)+(p_3p_0p_1)$ | $B_2(K)=\mathbb{Z}$ |
| 3    | <img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/oriented3.png" width="100%"> | $c_1 (p_0p_1p_2p_3)$ | $C_3(K)=\mathbb{Z}$ | $\partial_3 c=0$ |                  | $Z_3(K)=0$ |  |                        | $B_3(K)=0$ |

`Def`: chain complex $C(K)$ associated with $K$

$$
0\xrightarrow{i}C_n(K)\xrightarrow{\partial_n}C_{n-1}(K)\xrightarrow{\partial_{n-1}}\cdots\xrightarrow{\partial_2}C_1(K)\xrightarrow{\partial_1}C_0(K)\xrightarrow{\partial_0}0
$$

`Lemma`: The composite map $\partial_n\circ\partial_{n+1}:C_{n+1}(K)\rightarrow C_{n-1}(K)$ is a zero map; $B_n(K)\subset Z_r(K)$

>a boundary has no boundary.

### homology group

`Def`: the rth homology group $H_r(K)$ associated with $K$ is $H_r(K)\equiv Z_r(K)/B_r(K)$.

`Example`

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/examplehomology.png" width="60%">

homology groups are topological invariant. The most generaal form of $H_r(K)$ is

$$
\begin{matrix}H_r(K)\cong \underbrace{ \mathbb{Z}\oplus\cdots\oplus\mathbb{Z}}  \oplus\mathbb{Z}_{k_1}\oplus\cdots\oplus\mathbb{Z}_{k_p}\\f\quad\quad\quad\end{matrix}\\
$$

- $H_0(K)\cong\mathbb{Z}$ if $K$ is a connected simplicial complex.
- the number of generators of $H_r(K)$ counts the number of $r+1$-dimensional holes in $K$.
- the later $p$ factors detects the twisting in the polyhedron $K$.

`Def`: the generalized Euler characteristic of a general polyhedron $\chi(K)\equiv\sum_{r=0}^n(-1)^rI_r$.

## Cohomology

youtube



### homology VS cohomology





## de Rham cohomology

youtube lecture



### property (nakahara)



### Application in physics

 



## Cyclic cohomology

​                

### pairing cyclic cohomology with K theory





## References

[1] Prodan, Emil, and Hermann Schulz-Baldes. "Bulk and boundary invariants for complex topological insulators." *K* (2016).

[2] Nakahara, Mikio. *Geometry, topology and physics*. CRC Press, 2003.