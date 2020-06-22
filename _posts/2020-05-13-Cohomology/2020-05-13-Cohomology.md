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



`Example`: $K=\set{\sigma,\sigma\le\sigma^2=\langle p_0 p_1 p_2\rangle}=\set{p_0,p_1,p_2,\langle p_0 p_1\rangle,\langle p_1 p_2\rangle,\langle p_2 p_0\rangle,\langle p_0 p_1 p_2\rangle}$. 

`Def`: An oriented r-simplex $\sigma_r=(p_0p_1\cdots p_r)$ is a r-simple $\sigma^r=\langle p_0p_1\cdots p_r\rangle$ with a prescribed orientation.  We define $(p_{i_0}p_{i_1}\cdots p_{i_r})=\sgn(P)(p_0p_1\cdots p_r)$ with a permutation $P=\left(\begin{matrix}0&1&\cdots &r\newline i_0 & i_1 & \cdots& i_r\end{matrix}\right)$.

### chain group, cycle group and boundary group

`Example`: $K=\set{\sigma, \sigma\le\langle p_0 p_1 p_2 p_3\rangle}$.

| r                                                  |           | 0                                                            | 1                                                            | 2                                                            | 3                                                            |
| -------------------------------------------------- | --------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| r-chain group $C_r(K)$                             | generator | 4*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/simplex0.png" width="50%"> | 6*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/oriented1.png" width="90%"> | 4*<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/oriented2.png" width="40%"> | <img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/oriented3.png" width="100%"> |
|                                                    | element   | $c_1p_0+c_2p_1+\cdots$                                       | $c_1 (p_0p_1)+c_2(p_1p_2)+\cdots$                            | $c_1 (p_0p_1p_2) +c_2(p_1p_2p_3)+\cdots$                     | $c_1 (p_0p_1p_2p_3)$                                         |
|                                                    |           | $C_0(K)=\mathbb{Z}^4$                                        | $C_1(K)=\mathbb{Z}^6$                                        | $C_2(K)=\mathbb{Z}^4$                                        | $C_3(K)=\mathbb{Z}$                                          |
| r-cycle group $Z_r(K)=\ker\partial_r$              | def       |                                                              | $\partial_1 c=0$                                             | $\partial_2 c=0$                                             |                                                              |
|                                                    | example   | $p_0$                                                        | $(p_0p_1)+(p_1p_2)+(p_2p_0)$                                 | $(p_0p_1p_2)-(p_1p_2p_3)+(p_2p_3p_0)-(p_3p_0p_1)$            |                                                              |
|                                                    |           | $Z_0(K)=\mathbb{Z}^4$                                        | $Z_1(K)=\mathbb{Z}^3$                                        | $Z_2(K)=\mathbb{Z}$                                          | $Z_3(K)=0$                                                   |
| r-boundary group $B_r(K)=\text{im} \partial_{r+1}$ | def       | $\exists d\in C_1(K), c=\partial_1 d$                        | $\exists d\in C_2(K), c=\partial_2 d$                        | $\exists d\in C_3(K), c=\partial_3 d$                        |                                                              |
|                                                    | example   | $p_0-p_1$                                                    | $(p_0p_1)+(p_1p_2)+(p_2p_0)$                                 | $-(p_0p_1p_2)+(p_1p_2p_3)-(p_2p_3p_0)+(p_3p_0p_1)$           |                                                              |
|                                                    |           | $B_0(K)=\mathbb{Z}^3$                                        | $B_1(K)=\mathbb{Z}^3$                                        | $B_2(K)=\mathbb{Z}$                                          | $B_3(K)=0$                                                   |



`Def`: chain complex $C(K)$ associated with $K$


$$
0\xrightarrow{i}C_n(K)\xrightarrow{\partial_n}C_{n-1}(K)\xrightarrow{\partial_{n-1}}\cdots\xrightarrow{\partial_2}C_1(K)\xrightarrow{\partial_1}C_0(K)\xrightarrow{\partial_0}0
$$

`Lemma`: The composite map $\partial_n\circ\partial_{n+1}:C_{n+1}(K)\rightarrow C_{n-1}(K)$ is a zero map; $B_n(K)\subset Z_r(K)$

>a boundary has no boundary.
>
>With this lemma, the homology group could be well defined.

### homology group

`Def`: the rth homology group $H_r(K)$ associated with $K$ is $H_r(K)\equiv Z_r(K)/B_r(K)$.

`Example`

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/examplehomology.png" width="90%">

homology groups are topological invariant. The most generaal form of $H_r(K)$ is

$$
\begin{matrix}H_r(K)\cong \underbrace{ \mathbb{Z}\oplus\cdots\oplus\mathbb{Z}}  \oplus\mathbb{Z}_{k_1}\oplus\cdots\oplus\mathbb{Z}_{k_p}\\f\quad\quad\quad\end{matrix}\\
$$

- $H_0(K)\cong\mathbb{Z}$ if $K$ is a connected simplicial complex.
- the number of generators of $H_r(K)$ counts the number of $r+1$-dimensional holes in $K$.
- the later $p$ factors detects the twisting in the polyhedron $K$.

`Def`: the generalized Euler characteristic of a general polyhedron $\chi(K)\equiv\sum_{r=0}^n(-1)^rI_r$.

## Cohomology

We could derive cohomology group from homology group. With cohomology, we could glue functions using cup product, which doesn't exist in homology.

### from homology to cohomology

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/cohomologygroup.png" width="80%">

Note that, we have the composite map $\dd ^n\circ\dd^{n-1}$ as zero map in cochain complex, which is a direct result from $\partial_n\circ\partial_{n+1}=0$ in chain complex.

## de Rham cohomology

Preparation

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-05-13-Cohomology/assets/derivative.png" width="50%">

### differential forms

`Def`: $M$ is a smooth manifold. A differential n-form is a $\left(\begin{matrix}0\newline n\end{matrix}\right)$-tensor field $\omega$ that is totally antisymmetric


$$
\omega (X_1,\cdots,X_n)=\sgn(\pi)\omega(X_{\pi_1},\cdots,X_{\pi_n})
$$

`Example`: electromagnetic field strength $F$ is a 2-form.

`Notation`: set of all n-forms be denoted $\Omega^n(M)$ which naturally becomes a $C^\infty(M)$-module. 

`Def`: The exterior derivative operator $\dd:\Omega^n(M)\rightarrow\Omega^{n+1}(M)$ is defined as


$$
(\dd\omega)(X_1,\cdots,X_{n+1})=\sum_{i=1}^{n+1}(-1)^{i+1}X_i(\omega(X_1,\cdots,\cancel{X_i},\cdots,X_{n+1}))+\sum_{i<j}(-1)^{i+j}X_i(\omega([X_i,X_j],X_1,\cdots,\cancel{X_i},\cdots,\cancel{X_j},\cdots,X_{n+1}))
$$

> Addition and $C^\infty(M)$-multiplication are closed in $\Omega^n(M)$. We could only get a form with wedge product of two forms because the antisymmetry should hold. The wedge product is just antisymmetrized tensor product defined as
> 
> $$
> (\omega\wedge\sigma)(X_1,\cdots,X_{n+m}):=\frac{1}{n!}\frac{1}{m!}\sum\sgn(\pi) (\omega\otimes\sigma)(X_{\pi_1},\cdots,X_{\pi_{n+m}})
> $$
> 
> `Example`: 
> 
> $$
> \begin{align*}
> \omega\wedge\sigma(X_1,X_2)&=\omega\otimes\sigma(X_1,X_2)-\omega\otimes\sigma(X_2,X_1)\\
> &=\omega\otimes\sigma(X_1,X_2)-\sigma\otimes\omega(X_1,X_2)\\
> &=(\omega\otimes\sigma-\sigma\otimes\omega)(X_1,X_2)\\
> \end{align*}
> $$
> 


### Grassmann algebra and de Rham cohomology

`Def`: The $C^\infty(M)$-module $\Omega(M):=\Omega^0(M)\oplus \Omega^1(M)\oplus \cdots\oplus\Omega^{\dim M}(M)$ with wedge product $\wedge$ is the Grassmann algebra on $M$.

Exterior derivative $\dd$ extends by linear continuity to $\Omega(M)$.

`Theorem`: $\dd^2=0$

`Proof`

This implies that we have a sequence of maps 


$$
0\xrightarrow{d}\Omega^0(M)\xrightarrow{d}\cdots\xrightarrow{d}\Omega^{n-1}(M)\xrightarrow{d}\Omega^n(M)\xrightarrow{d}\Omega^{n+1}(M)\xrightarrow{d}\cdots\xrightarrow{d}\Omega^{\dim M}(M)\xrightarrow{d}0
$$


`Def`: $\omega\in \Omega$ is called exact if $\omega\in\text{im}(d)$, closed if $\omega\in\text{ker}(d)$.

`Example`: electromagnetic field strength $F$ is closed.

`Def`: the n-th de Rham cohomology group $H^n(M)=Z^n(M)/B^n(M)$, where $B^n=\text{im}(d)\subseteq \Omega^n(M)$ and $Z^n=\text{ker}(d)\subseteq \Omega^n(M)$.

>de Rham cohomology group only depends on global topology of $M$.

### property (nakahara)



### Application in physics

 



## Cyclic cohomology

​                

### pairing cyclic cohomology with K theory





## References

[1] Prodan, Emil, and Hermann Schulz-Baldes. "Bulk and boundary invariants for complex topological insulators." *K* (2016).

[2] Nakahara, Mikio. *Geometry, topology and physics*. CRC Press, 2003.

[3] [Harpreet Bedi]. (2016, May 20). *Cohomology* [Video file]. Retrieved from https://www.youtube.com/playlist?list=PL01055907ED9ACA18

[4] [Aditya Bhandari]. (2016, March 12). *Lectures on the Geometric Anatomy of Theoretical Physics* [Video file]. Retrieved from https://www.youtube.com/playlist?list=PLPH7f_7ZlzxTi6kS4vCmv4ZKm9u8g5yic