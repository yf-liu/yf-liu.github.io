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
| The expectation value of the measurement a measurement of an observable $A$ on a system that is in the state of $\rho$ is $\operatorname{Tr}(\rho A)$ | the probability $\mu_\rho^A(E)$ of a measurement of an observable $A$ on a system that is in the state of $\rho$ yields a result in the Borel set $E\subseteq \mathbb{R}$ is $\operatorname{Tr}(P_A(E)\circ \rho)$, where $P_A: B(\mathbb{R})\rightarrow \mathcal{L}(\mathcal{H})$ is the unique projection valued measure associated with a self-adjoint map $A$ according to the spectral theory. |
| unitary dynamics: $\rho(t_2)=U(t_2-t_1)\rho(t_1)U^{-1}(t_2-t_1)$, where unitary operator $U(t):=\exp(-\frac{\imath}{\hbar}Ht)$. | where $f:\mathbb{R}\rightarrow\mathbb{C}$ and $f(A):=\int f(\lambda)\dd P_A(\lambda)$ according to the spectral theory. |
| projective dynamics: $\rho_\text{after}=\frac{P_A(E)\rho_\text{before}P_A(E)}{\text{Tr(numerator)}}$ | where $P_A: B(\mathbb{R})\rightarrow \mathcal{L}(\mathcal{H})$ is the unique projection valued measure associated with a self-adjoint map $A$ according to the spectral theory. |



## Banach space and Hilbert space

| normed space | Banach space                                                 | inner product space | Hilbert  space |
| ------------ | ------------------------------------------------------------ | ------------------- | -------------- |
| (1)          | (1)                                                          | (1)                 | (1)            |
|              | complete<img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-03-20-C-algebra/assets/Completeness_in_Hilbert_space.png" width="40%"> |                     | complete       |
|              |                                                              | (2)                 | (2)            |

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



>$f$ could be an operator and $\|f\|$ is operator norm.
>
>Example: The set $\mathcal{L}(V,W):=\{A:V\rightarrow W|A\text{ is linear and bounded operator}\}$ is a Banach space if equipped with the operator norm $\|\cdot\|_{\mathcal{L}(V,W)}$, where $V$ is a normed space and $W$ is a Banach space.

## Separable Hilbert space

Definition: A Hilbert space is separable if it has a Schauder basis $S$ which is (a) countable, (b) orthogonal.

>Schauder basis is a set $S\subseteq\mathcal{H}$ which is
>
>(i) linearly independent,
>
>(ii) For any $\psi\in \mathcal{H}$, there exists countable subset $\{e_1,e_2,\cdots\}\subseteq S$ and a sequence $\{\psi^i\}_{i\in \mathbb{N}}\subseteq \mathbb{C}$ such that 
>
>$$
>\psi=\begin{cases}
>\sum_i^d\psi^ie_i, & \text{if }|S|<\infty \\
>\lim_{d\rightarrow \infty}\sum_i^d\psi^ie_i, & \mbox{else}
>\end{cases}
>$$
>
>Since Hilbert space is complete, $\lim_{d\rightarrow \infty}\sum_i^d\psi^ie_i$ must belong to Hilbert space. Note that $A(\lim_{d\rightarrow \infty}\sum_i^d\psi^ie_i)=\lim_{d\rightarrow \infty}\sum_i^dA\psi^ie_i$ only holds if it converges. $A$ should be a bounded linear operator.
>
>Since using the notion of Shauder basis, one has a more powerful means of generating a vector in a Hilbert space, approaching it by a sequence of $\{\psi^i\}_{i\in \mathbb{N}}$. One needs less resources, so it makes basis smaller. Hilbert space $\mathcal{H}$ is the topological closure of $\text{Span}(S)$, namely, $\overline{\text{Span}(S)}=\mathcal{H}$.

Any $\infty$-dim complex separable Hilbert space ($\mathcal{H},+,\cdot,\left<\cdot,\cdot\right>$) is unitarily isomorphic to the separable Hilbert space $(\ell^2(\mathbb{N}),+,\cdot,\braket{\cdot}{\cdot})$ of all square-summable sequence in $\mathbb{C}$.

## Resolvent map and Spectrum

Definition: Let $A$ be a closed operator. The resolvent map of $A$ is 

$$
\begin{align*}
R_A:\rho(A)&\rightarrow \mathcal{L}(\mathcal{H},\mathcal{H})\\
z&\mapsto (A-z \text{ id}_{\mathcal{D}_A})^{-1}
\end{align*}
$$

where resolvent set $\rho(A):=\{z\in \mathbb{C}|(A-z)^{-1}\in\mathcal{L}(\mathcal{H})\}$.

Definition: The spectrum $\sigma(A):=\mathbb{C}\backslash \rho(A)=\{\lambda\in \mathbb{C}|\exist\psi\in\mathcal{D}_A\backslash\{0\}: A\psi=\lambda\psi\}$.



## Spectral theory

For every self-adjoint operator $A:\mathcal{D}_A\rightarrow\mathcal{H}$, there is a projection-valued measure

$$
P_A:\sigma(\mathcal{O}_\mathbb{R})\rightarrow\mathcal{L}(\mathcal{H})
$$

such that $A=\int\text{id}_\mathbb{R}\dd P_A\equiv \int\lambda P_A(\dd\lambda)$.

### Construct projection-valued measure $P_A$

We could construct $P_A$ through the following steps.

Step 1: construct a real-valued Borel measure $\mu_\psi^A$ for each $\psi\in\mathcal{H}$ that

$$
\begin{align*}
\mu_\psi^A:\sigma(\mathcal{O}_\mathbb{R})&\rightarrow\mathbb{R}\\
\left( -\infty,\lambda\right] &\mapsto \lim_{\delta\rightarrow0}\lim_{\epsilon\rightarrow 0^+}\text{Im}\left<\psi,R_A(t+\imath\epsilon)\psi\right>
\end{align*}
$$

where $R_A$ is the resolvent map of $A$.

Step 2: construct a complex-valued Borel measure $\mu_{\psi,\varphi}^A$ from $\mu_\psi^A$ for all $\psi,\varphi\in\mathcal{H}$ that

$$
\begin{align*}
\mu_{\psi,\varphi}^A:\sigma(\mathcal{O}_\mathbb{R})&\rightarrow\mathbb{C}\\
\Omega &\mapsto \frac{1}{4} (\mu_{\psi+\varphi}^A(\Omega)-\mu_{\psi-\varphi}^A(\Omega)+\imath\mu_{\psi-\imath\varphi}^A(\Omega)-\imath\mu_{\psi+\imath\varphi}^A(\Omega))
\end{align*}
$$

Step 3: Define the projection-valued measure

$$
\begin{align*}
P_A:\sigma(\mathcal{O}_\mathbb{R})&\rightarrow\mathcal{L}(\mathcal{H})\\
\Omega &\mapsto P_A(\Omega) \text{ with }\left<\psi,P_A(\Omega)\varphi\right>:=\int\chi(\Omega)\dd \mu_{\psi,\varphi}^A
\end{align*}
$$

### Integration w.r.t a projection-valued measure $P_A$.

Then we consider the integration $\int f\dd P_A$ w.r.t a projection-valued measure. The whole integration could is an operator.

$$
\begin{align*}
\int f\dd P_A:\begin{cases}
\mathcal{H}\rightarrow\mathcal{H}, & \text{when } f \text{ is simple or bounded}\\
\mathcal{D}_{\int f\dd P_A}\rightarrow\mathcal{H}, & \text{when } f \text{ is unbounded}\\
\end{cases}
\end{align*}
$$

where $\mathcal{D}_{\int f\dd P_A}$ is a dense subset of $\mathcal{H}$. It's much complicated when $f$ is unbounded because the linearity, $\int (f+g)\dd P_A=\int f\dd P_A+\int g\dd P_A$ , does not necessarily hold.

| $f:\mathbb{R}\rightarrow\mathbb{C}$ | $\int f\dd P$                                                | sketch                                                       | $\int \dd P: \{f\}\rightarrow\mathcal{L}(\mathcal{H})$       |
| ------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| simple                          | $\int f\dd P=\sum_{n=1}^N f_n P(\text{preim}_f(\{f_n\}))$    | <img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-03-20-C-algebra/assets/integration1.png" width="40%"> | linear map $\int \dd P:S(\mathbb{R})(\text{norm space})\rightarrow \mathcal{L}(\mathcal{H})(\text{Banach space})$ |
| bounded                         | $\int f\dd P=\lim_{N\rightarrow \infty}\sum_{n=1}^N f_n P(\text{preim}_f(\{f_n\}))$ |                                                              | $C^*$ algebra homomorphism $\int \dd P:B(\mathbb{R})(C^* \text{algebra})\rightarrow \mathcal{L}(\mathcal{H})(C^* \text{algebra})$ |
| unbounded                       | $(\int f\dd P)\psi:=\lim_{n\rightarrow\infty}[(\int f_n\dd P)\psi]$ | <img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-03-20-C-algebra/assets/integration2.png" width="40%"> |                                                              |

Properties

- $(\int f\dd P)^*=\int \bar{f}\dd P$
- $\int(\alpha f+g)\dd P\supseteq\alpha\int f\dd P+\int g\dd P$
- $\int (f\cdot g)\dd P\supseteq (\int f\dd P)\circ(\int g\dd P)$

## Application

We could use spectral theory to calculate functions of unbounded operator. For example, we are familiar with $\exp(A)=\sum_n\frac{A^n}{n!}$, but that only holds when $A$ is bounded. When $A$ is unbounded, we could define
$$
\exp(A):=\int\exp\cdot\dd P_A
$$




## References

[1] Davidson, Kenneth R. *C\*-algebras by example*. Vol. 6. American Mathematical Soc., 1996.