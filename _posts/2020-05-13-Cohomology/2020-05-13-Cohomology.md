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
\sigma^r=\{x\in \mathbb{R}^m| x=\sum_{i=0}^r c_i p_i, c_i\ge 0, \sum_{i=0}^r c_i=1\}
$$

| r    | r-simplex                                                    | 0-face                                                       | 1-face                                                       | 2-face                                                       |      |
| ---- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---- |
| 0    | <img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex0.png" width="30%"> | 1*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex0.png" width="30%"> |                                                              |                                                              |      |
| 1    | <img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex1.png" width="30%"> | 2*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex0.png" width="30%"> | 1*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex1.png" width="30%"> |                                                              |      |
| 2    | <img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex2.png" width="30%"> | 3*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex0.png" width="30%"> | 3*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex1.png" width="30%"> | 1*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex2.png" width="100%"> |      |
| 3    | <img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex3.png" width="30%"> | 4*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex0.png" width="30%"> | 6*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex1.png" width="30%"> | 4*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex2.png" width="100%"> |      |

`Def`: A set of finite number of simplexes in $\mathbb{R}^m$ is called a simplicial complex $K$ if 

(i) $\sigma\in K,\sigma^\prime\le\sigma\Rightarrow \sigma^\prime\in K$, and 

(ii) $\sigma,\sigma^\prime\in K\Rightarrow \sigma\cap\sigma^\prime\le \sigma(^\prime) \text{ or } \sigma\cap\sigma^\prime=\empty$.

`Example`: $K=\{\sigma|\sigma\le\sigma^2=\langle p_0 p_1 p_2\rangle\}=\{p_0,p_1,p_2,\langle p_0 p_1\rangle,\langle p_1 p_2\rangle,\langle p_2 p_0\rangle,\langle p_0 p_1 p_2\rangle\}$.

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/complex.png" width="30%">

### chain group, cycle group and boundary group



### homology group



`Example`





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