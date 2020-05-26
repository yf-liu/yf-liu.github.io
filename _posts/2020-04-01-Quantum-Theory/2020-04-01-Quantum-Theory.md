---
title: Quantum Theory
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

## Quantum Mechanics in Mathematical language

| Quantum mechanics                                            | mathematical language                                        |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Hilbert space $\mathcal{H}$                                  | Hilbert space $(\mathcal{H},+,\cdot,\braket{\cdot}{\cdot})$  |
| states of a system (density matrix $\rho$)                   | positive trace-class linear map $\rho:\mathcal{H}\rightarrow \mathcal{H}$ |
| observable $A$ of a system                                   | self-adjoint linear map $A:\mathcal{D}_A\rightarrow \mathcal{H}$ |
| The expectation value of the measurement a measurement of an observable $A$ on a system that is in the state of $\rho$ is $\operatorname{Tr}(\rho A)$ | the probability $\mu_\rho^A(E)$ of a measurement of an observable $A$ on a system that is in the state of $\rho$ yields a result in the Borel set $E\subseteq \reals$ is $\operatorname{Tr}(P_A(E)\circ \rho)$, where $P_A: \text{Borel}(\reals)\rightarrow \mathcal{L}(\mathcal{H})$ is the unique projection valued measure associated with a self-adjoint map $A$ according to the spectral theory. |
| unitary dynamics: $\rho(t_2)=U(t_2-t_1)\rho(t_1)U^{-1}(t_2-t_1)$, where unitary operator $U(t):=\exp(-\frac{\imath}{\hbar}Ht)$. | where $f:\reals\rightarrow\mathbb{C}$ and $f(A):=\int f(\lambda)\dd P_A(\lambda)$ according to the spectral theory. |
| projective dynamics: $\rho_\text{after}=\frac{P_A(E)\rho_\text{before}P_A(E)}{\text{Tr(numerator)}}$ | where $P_A: \text{Borel}(\reals)\rightarrow \mathcal{L}(\mathcal{H})$ is the unique projection valued measure associated with a self-adjoint map $A$ according to the spectral theory. |



## Banach space and Hilbert space

| normed space | Banach space | inner product space | Hilbert  space |
| ------------ | ------------ | ------------------- | -------------- |
| (1)          | (1)          | (1)                 | (1)            |
|              | complete     |                     | complete       |
|              |              | (2)                 | (2)            |

$$
\|f\|\ge0\\
\|\lambda f\|=|\lambda|\cdot \|f\|\\
\|f+g\|\le\|f\|+\|g\|
$$

$$
\left<f,g\right>=\overline{\left<g,f\right>}\\
\left<af_1+bf_2,g\right>=a\left<f_1,g\right>+b\left<f_2,g\right>\\
\left<f,f\right>\ge0\\
(|f,g|\le\|f\|\ \|g\|)
$$

<img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-03-20-C-algebra/assets/Completeness_in_Hilbert_space.png" width="40%">

>$f$ could be an operator and $||f||$ is operator norm.
>
>Example: The set $\mathcal{L}(V,W):=\{A:V\rightarrow W|A\text{ is linear and bounded operator}\}$ is a Banach space if equipped with the operator norm $||\cdot||_{\mathcal{L}(V,W)}$, where $V$ is a normed space and $W$ is a Banach space.

## Separable Hilbert space

Definition: A Hilbert space is separable if it has a Schauder basis $S$ which is (a) countable, (b) orthogonal.

Any $\infty$-dim complex separable Hilbert space ($\mathcal{H},+,\cdot,\left<\cdot,\cdot\right>$) is unitarily isomorphic to the separable Hilbert space $\ell^2(\mathbb{N})$ of all square-summable sequence in $\mathbb{C}$.

>Schauder basis
>
>

## Measure theory





## Self-adjoint operators



## Resolvent map and Spectrum





 ## Spectral theory







## References

[1] Davidson, Kenneth R. *C\*-algebras by example*. Vol. 6. American Mathematical Soc., 1996.