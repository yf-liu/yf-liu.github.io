---
title: Jordan-Wigner transformation
category: Physics
tags:
  - Quantum Theory
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



## One particle

| Spin                                                         | Fermion                           |                                                              |
| ------------------------------------------------------------ | --------------------------------- | ------------------------------------------------------------ |
| $\ket{\uparrow}$                                             | $\ket{1}$                         | $\begin{bmatrix} 1\newline 0\end{bmatrix}$                   |
| $\ket{\downarrow}$                                           | $\ket{0}$                         | $\begin{bmatrix}0\\1\end{bmatrix}$                           |
| $S^+$                                                        | $f^\dagger$                       | $\begin{bmatrix} 0& 1\\ 0&0\end{bmatrix}$                    |
| $S^-$                                                        | $f$                               | $\begin{bmatrix} 0&0\\1&0\\\end{bmatrix}$                    |
| $S_z=\frac{1}{2}(\ket{\uparrow}\bra{\uparrow}-\ket{\downarrow}\bra{\downarrow})$ | $f^\dagger f-\frac{1}{2}$         | $\frac{1}{2}\begin{bmatrix} 1&0\\0&-1\end{bmatrix}$          |
| $S_x=\frac{1}{2}(S^++S^-)$                                   | $\frac{1}{2}(f^\dagger +f)$       | $\frac{1}{2}\begin{bmatrix} 0&1\\1&0\end{bmatrix}$           |
| $S_y=\frac{1}{2\imath}(S^+-S^-)$                             | $\frac{1}{2\imath}(f^\dagger -f)$ | $\frac{1}{2}\begin{bmatrix} 0&-\imath\\\imath&0\end{bmatrix}$ |
| $\{S^+,S^-\}=1$                                              | $\{f^\dagger,f\}=1$               | $\begin{bmatrix} 1& 0\\ 0&1\end{bmatrix}$                    |
| $\left[S^+,S^-\right]=2S_z$                                  | $\left[f^\dagger,f\right]$        | $\begin{bmatrix} 1& 0\\ 0&-1\end{bmatrix}$                   |
| $S_z+\frac{1}{2}$                                            | $f^\dagger f$                     |                                                              |

>$$
>\{f^\dagger,f\}\ket{0}=f^\dagger f\ket{0}+f f^\dagger \ket{0}=\ket{0}\\
>\{f^\dagger,f\}\ket{1}=f^\dagger f\ket{1}+f f^\dagger \ket{1}=\ket{1}\\
>\{f^\dagger,f\}=\begin{bmatrix} 1& 0\\ 0&1\end{bmatrix}\\
>\left[f^\dagger,f\right]\ket{0}=f^\dagger f\ket{0}-f f^\dagger \ket{0}=-\ket{0}\\
>\left[f^\dagger,f\right]\ket{1}=f^\dagger f\ket{1}-f f^\dagger \ket{1}=\ket{1}\\
>\left[f^\dagger,f\right]=\begin{bmatrix} 1& 0\\ 0&-1\end{bmatrix}\\
>$$
>
>$$
>\{S_a,S_b\}=\frac{1}{2}\delta_{ab}\\
>\left[S_a,S_b\right]=\imath \epsilon_{abc}S_c\\
>\{S^+,S^-\}=\{S_x+\imath S_y,S_x-\imath S_y\}=\begin{bmatrix} 1& 0\\ 0&1\end{bmatrix}\\
>\left[S^+,S^-\right]=\left[S_x+\imath S_y,S_x-\imath S_y\right]=2S_z=\begin{bmatrix} 1& 0\\ 0&-1\end{bmatrix}
>$$
>
>

## 1-D chain

| Spin                                                         | Fermion                         |       |
| ------------------------------------------------------------ | ------------------------------- | ----- |
| $\ket{\downarrow\downarrow\downarrow\cdots}$                 | $\ket{ijk\cdots}$               | $2^n$ |
| ...                                                          | ...                             |       |
| $S^+_1=f^\dagger_1$                                          | $f_1^\dagger$                   | $n$   |
| $S_2^+=f_2^\dagger e^{\imath\pi n_1}$                        | $f_2^\dagger$                   |       |
| $S_j^+=f_j^\dagger e^{\imath \phi_j},\phi_j=\pi\sum_{i<j} n_i$ | $f_j^\dagger$                   |       |
| ...                                                          | ...                             |       |
| $S_1^-=f_1$                                                  | $f_1$                           | $n$   |
| $S_2^-=f_2 e^{-\imath\pi n_1}$                               | $f_2$                           |       |
| $S_j^-=f_j e^{-\imath \phi_j},\phi_j=\pi\sum_{i<j} n_i$      | $f_j$                           |       |
| ...                                                          | ...                             |       |
| $2S^z_j$                                                     | $2f^\dagger_jf_j-1$             | $n$   |
| ...                                                          | ...                             |       |
| $\left[S^-_k,S^-_j\right]=0$                                 | $\{f_k,f_j\}=0$                 |       |
| $\left[S^+_k,S^+_j\right]=0$                                 | $\{f^\dagger_k,f^\dagger_j\}=0$ |       |
| $\left[S^+_k,S^-_j\right]=0,k\ne j$                          | $\{f^\dagger_k,f_j\}=0,k\ne j$  |       |
| $M=\sum_n S^z_n+\frac{1}{2}$                                 | $N=\sum_nf_n^\dagger f_n$       |       |

>Pauli exclusive principle
>
>$$
>\ket{ijk\cdots}=-\ket{ikj\cdots}
>$$
>
>(relation between $\psi(x_1,x_2)$ and $\ket{12}$?)
>$$
>0=\ket{ijk\cdots}+\ket{ikj\cdots}=f^\dagger_i\{f^\dagger_k,f^\dagger_j\}\ket{\cdots},\ \{f^\dagger_k,f^\dagger_j\}=0\\
>\{f_k,f_j\}=f_kf_j+f_jf_k=\{f^\dagger_k,f^\dagger_j\}^\dagger=0\\
>$$
>
>$$
>\{f^\dagger_k,f_j\}\ket{\cdots k\cdots}=f^\dagger_k f_j\ket{\cdots k\cdots}+f_j f^\dagger_k\ket{\cdots k\cdots}=0+0=0\\
>\{f^\dagger_k,f_j\}\ket{\cdots j\cdots}=f^\dagger_k f_j\ket{\cdots j\cdots}+f_j f^\dagger_k\ket{\cdots j\cdots}=f_k^\dagger(\pm f_jf^\dagger_j)\ket{\cdots}+(\mp f_jf^\dagger_j)f^\dagger_k\ket{\cdots}\\=f_k^\dagger(\pm 1)\ket{\cdots}+(\mp 1)f^\dagger_k\ket{\cdots}=0\\
>\{f^\dagger_k,f_j\}=0
>$$
>
>
>
>$$
>\phi_j=\pi\sum_{i<j} n_i\\
>\{e^{-\imath\pi n_j},f_j\}\ket{\cdots}=e^{-\imath\pi n_j}f_j\ket{\cdots}+f_j e^{-\imath\pi n_j}\ket{\cdots}=0+0=0\\
>\{e^{-\imath\pi n_j},f_j\}\ket{\cdots j \cdots}=f_j(\pm f^\dagger_j)\ket{\cdots}+f_j (\mp f^\dagger_j)(-1)\ket{ \cdots}=\pm\ket{\cdots}\mp\ket{\cdots}=0\\
>\{e^{-\imath \phi_k},f_j\}=0,j<k;\left[e^{-\imath \phi_k},f_j\right]=0,k\le j
>$$
>
>
>
>
>$$
>\begin{align*}
>\left[S^-_k,S^-_j\right]&=\left[f_j e^{-\imath \phi_k},f_j e^{-\imath \phi_j}\right]\\
>&=f_k e^{-\imath \phi_k}f_j e^{-\imath \phi_j}-f_j e^{-\imath \phi_j}f_k e^{-\imath \phi_k}\\
>&=\pm f_k f_j e^{-\imath \phi_k}e^{-\imath \phi_j}-(\mp) f_j f_k e^{-\imath \phi_j} e^{-\imath \phi_k}\\
>&=\pm \{f_k, f_j\} e^{-\imath \phi_k}e^{-\imath \phi_j}\\
>&=0
>\end{align*}
>$$
>

>Remark
>
>fermion+string operator =boson

## Application

$$
S_j^+=f_j^\dagger e^{\imath \phi_j},\phi_j=\pi\sum_{i<j}n_i\\
S_j^-=f_je^{-\imath \phi_j},\phi_j=\pi\sum_{i<j}n_i\\
\\
S^x_n=\frac{1}{2}(S^+_n+S^-_n)\\
S^y_n=\frac{1}{2\imath}(S^+_n-S^-_n)\\
S^x_nS^x_{n+1}=\frac{1}{2}(S^+_n+S^-_n)\frac{1}{2}(S^+_{n+1}+S^-_{n+1})=\frac{1}{4}(S^+_n S^+_{n+1}+S^-_n S^+_{n+1}+S^+_n S^-_{n+1}+S^-_n S^-_{n+1})\\
S^y_nS^y_{n+1}=\frac{1}{2\imath}(S^+_n-S^-_n)\frac{1}{2\imath}(S^+_{n+1}-S^-_{n+1})=-\frac{1}{4}(S^+_n S^+_{n+1}-S^-_n S^+_{n+1}-S^+_n S^-_{n+1}+S^-_n S^-_{n+1})\\
S^x_nS^x_{n+1}+S^y_nS^y_{n+1}\\
=\frac{1}{2}(S^+_{n+1} S^-_n +S^+_n S^-_{n+1})\\
=\frac{1}{2}(f_{n+1}^\dagger e^{\imath \phi_{n+1}}f_ne^{-\imath \phi_n}+h.c.)\\
=\frac{1}{2}(f_{n+1}^\dagger e^{\imath \pi n_n}f_n+h.c.)\\
=\frac{1}{2}(f_{n+1}^\dagger f_n+f^\dagger_n f_{n+1})\\
S^z_n=f_n^\dagger f_n-\frac{1}{2}
$$



$$
\begin{align*}
H_S=&\sum_n J(d_n)(S_n^xS_{n+1}^x+S_n^yS_{n+1}^y)+\sum_n J_zS^z_nS_{n+1}^z\\
H_F=& \sum_n \frac{1}{2} J(d_n)(f_{n+1}^\dagger f_n+f^\dagger_n f_{n+1})+\sum_n J_z(f_n^\dagger f_n-\frac{1}{2})(f_{n+1}^\dagger f_{n+1}-\frac{1}{2})\\
\end{align*}
$$





