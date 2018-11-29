---
title: Quantal phase for general cyclic evolution
category: Physics
tags:
  - Topology
  - Berry phase
  - Cyclic evolution
---

## Aharonov-Aanandan phase

### State space and projection space

---

The general evolution of the parameter $R (t)$ is

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

\path: R (0) \rightarrow R (t) \rightarrow R(\tau)
$$

The time evolution of every pure physical state defines a curve in the space $P(\mathcal{H})$ of all such states. 

$$
\mathcal{C}: W (0) \rightarrow W (t) = \ket{\psi (t)} \bra{\psi (t)} \rightarrow W (\tau) = W (0)
$$

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-27-General-Cyclic-Evolution/assets/manifold.png" width="100%">

The general relation between the solution of the Schrodinger equation $\ket{\psi (t)}$, the closed lift $\ket{\phi (t)}$ and the A-A lift $\ket{\tilde{\psi} (t)}$.

$$
\begin{align*}
\ket{\psi (t)} = \e ^ {- \ii \alpha} \ket{\tilde{\psi} (t)} = \e ^ {- \ii \int _ 0 ^ t \bra{\psi (t ^ \prime)} h (t ^ \prime) \ket{\psi (t ^ \prime)} \dd t ^ \prime} \ket{\tilde{\psi} (t)} \\
\ket{\phi (t)} = \e ^ {- \ii \gamma} \ket{\tilde{\psi} (t)} = \e ^ {- \ii \int _ 0 ^ t \bra{\phi (t ^ \prime)} \frac{\dd}{\dd t ^ \prime} \ket{\phi (t ^ \prime)} \dd t ^ \prime} \ket{\tilde{\psi} (t)} \\
\end{align*}
$$

The three curves project onto the closed curve $\mathcal{C}$.

$$
\ket{\psi (t)} \bra{\psi (t)} = \ket{\phi (t)} \bra{\phi (t)} = \ket{\tilde{\psi} (t)} \bra{\tilde{\psi} (t)} = W (t)
$$

>$$
>\begin{align*}
>\ket{\psi (t)} \bra{\psi (t)} & = \e ^ {- \ii \alpha} \ket{\tilde{\psi} (t)} \bra{\tilde{\psi} (t)} \e ^ {\ii \alpha} = \ket{\tilde{\psi} (t)} \bra{\tilde{\psi} (t)} \\
>\ket{\phi (t)} \bra{\phi (t)} & = \e ^ {- \ii \gamma} \ket{\tilde{\psi} (t)} \bra{\tilde{\psi} (t)} \e ^ {\ii \gamma} = \ket{\tilde{\psi} (t)} \bra{\tilde{\psi} (t)} \\
>\end{align*}
>$$
>

The phase angle $\gamma (\tau)$ is independent of the choice of the time parameterization of $\phi (t)$ and the Hamiltonian as long as these Hamiltonian describe the same closed path $\mathcal{C}$ in $P(\mathcal{H})$. It is considered as a geometric property of $\mathcal{C}$.

The one-form appearing in the integrand of $\gamma (\tau)$, namely

$$
\mathcal{A} \defas \ii \bra{\phi} \dd \ket{\phi}
$$

is called the A-A connection one-form. It is invariant under the transformation $\phi(t) \rightarrow \phi ^ \prime (t) = \e ^ {\ii \zeta (t)} \phi (t)$.

$$
\begin{align*}
\mathcal{A} = \ii \bra{\phi} \dd \ket{\phi} \rightarrow \mathcal{A} ^ \prime = \ii \bra{\phi ^ \prime} \dd \ket{\phi ^ \prime} \\
\end{align*}
$$

### The uniqueness of A-A lift

---

The non-uniqueness of the closed lift is due to the fact that the single-valued state vectors $\ket{\phi(R(t))}$ are only defined up to the gauge transformations:

$$
\ket{\phi(R(t))} \rightarrow \ket{\phi ^ \prime (R(t))} = \e ^ {\ii \zeta (R (t))} \ket{\phi(R(t))} \text{, with } \e ^ {\ii \zeta (R (\tau))} = \e ^ {\ii \zeta (0)}
$$

Then discuss the non-uniqueness of the dynamic lift and the uniqueness of the A-A lift directly. The A-A lift satisfies the following equation and initial condition:

$$
\ii \frac{\dd}{\dd t} \ket{\tilde{\psi} (t)} = [h (t) - \bra{\psi (t)} h (t) \ket{\psi (t)} \id] \ket{\tilde{\psi} (t)} \\
\ket{\tilde{\psi} (0)} = \ket{\psi (0)}
$$

>$\ket{\psi(t)}$ is solution of the Schrödinger equation $\ii \frac{\dd \ket{\psi (t)}}{\dd t} = h (t) \ket{\psi (t)}$.
>
>$$
>\begin{align*}
>\ii \frac{\dd \ket{\psi (t)}}{\dd t} & = h (R) \ket{\psi (t)} \\
>\ii \frac{\dd \left(\e ^ {- \ii \int _ 0 ^ t \bra{\psi (t ^ \prime)} h (t ^ \prime) \ket{\psi (t ^ \prime)} \dd t ^ \prime}  \ket{\tilde{\psi} (t)}\right)}{\dd t} &  = h (t) \left(\e ^ {- \ii \int _ 0 ^ t \bra{\psi (t ^ \prime)} h (t ^ \prime) \ket{\psi (t ^ \prime)} \dd t ^ \prime}  \ket{\tilde{\psi} (t)}\right) \\
>\e ^ {- \ii \int _ 0 ^ t \bra{\psi (t ^ \prime)} h (t ^ \prime) \ket{\psi (t ^ \prime)} \dd t ^ \prime} \bra{\psi (t)} h (t) \ket{\psi (t)} \ket{\tilde{\psi} (t)} + \ii \e ^ {- \ii \int _ 0 ^ t \bra{\psi (t ^ \prime)} h (t ^ \prime) \ket{\psi (t ^ \prime)} \dd t ^ \prime} &  \frac{\dd \ket{\tilde{\psi} (t)}}{\dd t}  = h (t) \e ^ {- \ii \int _ 0 ^ t \bra{\psi (t ^ \prime)} h (t ^ \prime) \ket{\psi (t ^ \prime)} \dd t ^ \prime}  \ket{\tilde{\psi} (t)}\\
> \bra{\psi (t)} h (t) \ket{\psi (t)} \ket{\tilde{\psi} (t)} + \ii   \frac{\dd \ket{\tilde{\psi} (t)}}{\dd t} &  = h (t) \ket{\tilde{\psi} (t)}\\
> \ii \frac{\dd}{\dd t} \ket{\tilde{\psi} (t)} &  = [h (t) - \bra{\psi (t)} h (t) \ket{\psi (t)} \id] \ket{\tilde{\psi} (t)}
>\end{align*}
>$$
>

The tangent vector $\frac{\dd \ket{\tilde{\psi} (t)}}{\dd t}$ of $\ket{\tilde{\psi} (t)}$ is orthogonal to both $\ket{\psi (t)}$ and $\ket{\tilde{\psi} (t)}$ in the Hilbert space.

$$
\bra{\tilde{\psi} (t)} \frac{\dd}{\dd t} \ket{\tilde{\psi} (t)} = \bra{\psi (t)} \frac{\dd}{\dd t} \ket{\tilde{\psi} (t)} = 0
$$

>$$
>\begin{align*}
>\ii \frac{\dd}{\dd t} \ket{\tilde{\psi} (t)} & = [h (t) - \bra{\psi (t)} h (t) \ket{\psi (t)} \id] \ket{\tilde{\psi} (t)} \\
>\bra{\tilde{\psi} (t)} \ii \frac{\dd}{\dd t} \ket{\tilde{\psi} (t)} & = \bra{\tilde{\psi} (t)} [h (t) - \bra{\psi (t)} h (t) \ket{\psi (t)} \id] \ket{\tilde{\psi} (t)} \\
>& = \bra{\tilde{\psi} (t)} h (t)  \ket{\tilde{\psi} (t)} - \bra{\psi (t)} h (t) \ket{\psi (t)}  \id \bra{\tilde{\psi} (t)}  \ket{\tilde{\psi} (t)}  \\
>& = \bra{\tilde{\psi} (t)} h (t)  \ket{\tilde{\psi} (t)} - \bra{\psi (t)} h (t) \ket{\psi (t)}  \\
>& = 0\\
>\bra{\psi (t)} \ii \frac{\dd}{\dd t} \ket{\tilde{\psi} (t)} & = \bra{\psi (t)} [h (t) - \bra{\psi (t)} h (t) \ket{\psi (t)} \id] \ket{\tilde{\psi} (t)} \\
>& = \bra{\psi (t)} h (t) \ket{\tilde{\psi} (t)} - \bra{\psi (t)} \bra{\psi (t)} h (t) \ket{\psi (t)} \id \ket{\tilde{\psi} (t)} \\
>& = \bra{\psi (t)} h (t) \e ^ {- \ii \alpha} \ket{\psi (t)} - \bra{\psi (t)} \bra{\psi (t)} h (t) \ket{\psi (t)} \id \e ^ {- \ii \alpha} \ket{\psi (t)}  \\
>& = \e ^ {- \ii \alpha} \bra{\psi (t)} h (t) \ket{\psi (t)} - \e ^ {- \ii \alpha} \bra{\psi (t)} h (t) \ket{\psi (t)} \id \bra{\psi (t)} \ket{\psi (t)}  \\
>& = \e ^ {- \ii \alpha} \bra{\psi (t)} h (t) \ket{\psi (t)} - \e ^ {- \ii \alpha} \bra{\psi (t)} h (t) \ket{\psi (t)}\\
>& = 0
>\end{align*}
>$$
>

Although the dynamical lift $C$ is uniquely determined by the Hamiltonian $h (t)$, it is not uniquely determined by the physical problem. 

$$
h (t) \rightarrow h ^ \prime = h(t) - \kappa(t) \id \text{, with } \kappa(t) \in \realset
$$

Both the Hamiltonian define the same curve $\mathcal{C}$ in $P(\mathcal{H})$,

$$
\ket{\psi ^ \prime (t)} \bra{\psi ^ \prime (t)} = \ket{\psi (t)} \bra{\psi (t)}
$$

>$$
>\begin{align*}
>\ii \frac{\dd \ket{\psi (t)}}{\dd t} & = h (t) \ket{\psi (t)} \\
>\ii \frac{\dd \ket{\psi ^ \prime (t)}}{\dd t} & = h (t) \ket{\psi ^ \prime (t)} \\
>\ii \frac{\dd (\ket{\psi (t)} \bra{\psi (t)})}{\dd t} & = \ii \frac{\dd \ket{\psi (t)}}{\dd t} \bra{\psi (t)} + \ii \ket{\psi (t)} \frac{\dd \bra{\psi (t)}}{\dd t} \\
>& = h (t) \ket{\psi (t)} \bra{\psi (t)} - \ket{\psi (t)} \bra{\psi (t)} h (t)\\
>\ii \frac{\dd (\ket{\psi ^ \prime (t)} \bra{\psi ^ \prime (t)})}{\dd t} & = \ii \frac{\dd \ket{\psi ^ \prime (t)}}{\dd t} \bra{\psi ^ \prime (t)} + \ii \ket{\psi ^ \prime (t)} \frac{\dd \bra{\psi ^ \prime (t)}}{\dd t} \\
>& = h (t) \ket{\psi ^ \prime (t)} \bra{\psi ^ \prime (t)} - \ket{\psi ^ \prime (t)} \bra{\psi ^ \prime (t)} h (t)\\
>\end{align*}
>$$
>
>They satisfies the same function $\frac{\dd \op{P}}{\dd t} = \ii[\op{P},h(t)]$, which can be uniquely solved.

But different Hamiltonian define different dynamical lifts $t \rightarrow \ket{\psi (t)}$ and $t \rightarrow \ket{\psi ^ \prime(t)}$.

$$
\ket{\psi ^ \prime (t)} = \e ^ {\ii \kappa t} \ket{\psi (t)}
$$

>$$
>\begin{align*}
>\ii \frac{\dd \braket{\psi (t)}{\psi ^ \prime (t)}}{\dd t} & = \ii \frac{\dd \bra{\psi (t)}}{\dd t} \ket{\psi ^ \prime (t)} + \ii  \bra{\psi (t)}\frac{\dd \ket{\psi ^ \prime (t)}}{\dd t} \\
>& = - \bra{\psi (t)} h (t) \ket{\psi ^ \prime (t)} +  \bra{\psi (t)} [h(t) - \kappa \id] \ket{\psi ^ \prime (t)} \\
>& = - \kappa \braket{\psi (t)}{\psi ^ \prime (t)} \\
>\braket{\psi (t)}{\psi ^ \prime (t)} & = \e ^ {\ii \kappa t} \\
>\ket{\psi ^ \prime (t)} & = \e ^ {\ii \kappa t} \ket{\psi (t)}
>\end{align*}
>$$
>

Thus the dynamical lift does not uniquely correspond to the physical problem. A lift that is uniquely associated with the closed curve $\mathcal{C}$ in $P(\mathcal{H})$, and therefore reflects the physical effects is A-A lift $\tilde{C}$.

$$
\ket{\tilde{\psi} (t)} = \ket{\tilde{\psi} ^ \prime (t)}
$$

>$$
>\begin{align*}
>\ii \frac{\dd}{\dd t} \ket{\tilde{\psi} (t)} & = [h (t) - \bra{\psi (t)} h (t) \ket{\psi (t)} \id] \ket{\tilde{\psi} (t)} \\
>\ii \frac{\dd}{\dd t} \ket{\tilde{\psi} ^ \prime (t)} & = [h ^ \prime (t) - \bra{\psi ^ \prime (t)} h (t) ^ \prime (t) \ket{\psi ^ \prime (t)} \id] \ket{\tilde{\psi} ^ \prime (t)} \\
>& = [h (t) - \kappa \id - \bra{\psi ^ \prime (t)} h (t) - \kappa \id \ket{\psi ^ \prime (t)} \id] \ket{\tilde{\psi} ^ \prime (t)} \\
>& = [h (t) - \kappa \id - \bra{\psi ^ \prime (t)} h (t) \ket{\psi ^ \prime (t)} \id + \kappa \braket{\psi ^ \prime (t)}{\psi ^ \prime (t)} \id] \ket{\tilde{\psi} ^ \prime (t)} \\
>& = [h (t) - \bra{\psi ^ \prime (t)} h (t) \ket{\psi ^ \prime (t)} \id] \ket{\tilde{\psi} ^ \prime (t)} \\
>& = [h (t) - \bra{\psi (t)} h (t) \ket{\psi (t)} \id] \ket{\tilde{\psi} ^ \prime (t)} \\
>\end{align*}
>$$
>
>They satisfies the same equation which can be uniquely solved.

### A-A connection one-form

---

### Special case for the spinning quantum system

---

The cyclic evolution of the parameter $R (\theta,\omega t)$ is

$$
\path: R (\theta,0) \rightarrow R (\theta,\omega t) \rightarrow R (\theta,\omega \tau)
$$

The time evolution of every pure physical state defines a curve in the space $P(\mathcal{H})$ of all such states. 

$$
\mathcal{C} _ k : W _ k(0) \rightarrow W _ k (t) = \ket{\psi _ k (t)} \bra{\psi _ k (t)} = \ket{\phi _ k (t)} \bra{\phi _ k (t)} \rightarrow W _ k (\tau) = W _ k (0)
$$

where $\ket{\psi(t)}$ and $\ket{\phi (k)}$ are given as

$$
\begin{align*}
& \ket{\psi(t)} = \e ^ {- \ii \omega t k} \e ^ {- \ii \Omega t k} \ket{\phi (k)} \\
& \ket{\phi (k)} = \ket{k , \theta , \omega t}
\end{align*}
$$

## Exact cyclic evolution for periodic Hamiltonian

### Construct the evolution operator

---

The periodic Hamiltonian is

$$
h (t + T) = h (t)
$$

We can use the results of Floquet theory in mathematics. Consider the unitary operator $V (t) \defas U ^ \dagger (t + T)$. It is not difficult to check that $V$ satisfies the following Schrodinger equation:

$$
\frac{\dd}{\dd t} V (t) = - \ii h (t) V (t) \\
V (0) = U ^ \dagger (T) \isdefas V _ 0
\label{unitary_Schrodinger}
$$

>$$
>\begin{align*}
>\frac{\dd}{\dd t} U ^ \dagger (t + a) & = - \ii h (t) U ^ \dagger (t + a) \\
>\frac{\dd}{\dd t} U (t + a) & = \ii U (t + a) h ^ \dagger (t) \\
>\frac{\dd}{\dd t} \left(U ^ \dagger (t + a) U (t + a)\right) & = \frac{\dd}{\dd t} U ^ \dagger (t + a) U (t + a) + U ^ \dagger (t + a) \frac{\dd}{\dd t} U (t + a) \\
>& = - \ii h (t) U ^ \dagger (t + a) U (t + a) + U ^ \dagger (t + a) \ii U  (t + a) h ^ \dagger (t) \\
>& = - \ii h (t) + \ii h (t) \\
>& = 0
>\end{align*}
>$$
>
>The unitary $V (t) \defas U ^ \dagger (t + T)$ satisfies the equation.

The operator $V ^ \prime (t) \defas U ^ \dagger (t) V _ 0$ also satisfies Eqn. ($\ref{unitary_Schrodinger}$). However we know from the uniqueness theorem for initial value linear differential equation that the solution is uniqueness.

$$
\frac{\dd}{\dd t} V ^ \prime (t) = - \ii h (t) V ^ \prime (t) \\
V ^ \prime (0) = U ^ \dagger (0) V _ 0
$$

>$$
>\begin{align*}
>\frac{\dd}{\dd t} U ^ \dagger (t) & = - \ii h (t) U ^ \dagger (t) \\
>\frac{\dd}{\dd t} U ^ \dagger (t) V _ 0 & = - \ii h (t) U ^ \dagger (t) V _ 0 \\
>\end{align*}
>$$
>

Therefore we have $V (t) = V ^ \prime (t)$.

$$
U ^ \dagger (t + T) = U ^ \dagger (t) V _ 0 = U ^ \dagger (t) U ^ \dagger (T)
$$

This implies that the unitary operator can be noted as 

$$
U ^ \dagger (t) = Z (t) \e ^ {- \ii t \tilde{h}} \\
U ^ \dagger (T) = \e ^ {- \ii T \tilde{h}}
$$

where $\tilde{h}$ is a time-independent Hermitian operator and $Z (t)$ is a T-periodic unitary operator with $Z(0) = 1$.

>Unitarity of $U(t)$:
>
>$$
>\begin{align*}
>U ^ \dagger (t) & = Z (t) \e ^ {- \ii t \tilde{h}} \\
>U (t) & = \e ^ {\ii t \tilde{h}} Z ^ \dagger (t) \\
>U ^ \dagger (t) U (t) & = Z (t) \e ^ {- \ii t \tilde{h}} \e ^ {\ii t \tilde{h}} Z ^ \dagger (t) = \id
>\end{align*}
>$$
>
>Periodicity of $Z(t)$:
>
>$$
>\begin{align*}
>U ^ \dagger (t + T) & = U ^ \dagger (t) \\
>Z (t + T) \e ^ {- \ii t \tilde{h}} & = Z (t) \e ^ {- \ii t \tilde{h}} \\
>Z (t + T) & = Z (t) \\
>\end{align*}
>$$
>
>$U ^ \dagger (0)$ and $Z (0)$:
>
>$$
>Z (0) = U ^ \dagger (0) = \id
>$$
>

### Geometrical phase

---

Consider the evolution of a cyclic state vector $\ket{\psi(0)}$. By definition $\ket{\psi(0)}$ is an eigenvector of the evolution operator:

$$
U ^ \dagger (\tau) \ket{\psi(0)} = Z (\tau) \e ^ {- \ii t \tilde{h}} \ket{\psi(0)} = \e ^ {- \ii \alpha (t)} \ket{\psi(0)}
$$

On the other hand the evolution of $\ket{\psi(0)}$is governed by the Schrodinger equation $\ii \frac{\dd}{\dd t} \ket{\psi (t)} = h (t) \ket{\psi (t)}$. In terms of the operators $Z(t)$ and $\tilde{h}$, these equations take the form

$$
\begin{align*}
\ket{\psi(t)} & = Z (t) \e ^ {- \ii t \tilde{h}} \ket{\psi(0)} \\
h (t) & = \ii \dot{Z} (t) Z ^ \dagger (t) + Z (t) \tilde{h} Z ^ \dagger (t) \\
\end{align*}
$$

>$$
>\begin{align*}
>\ii \frac{\dd}{\dd t} \ket{\psi (t)} & = h (t) \ket{\psi (t)} \\
>\text{LHS: } & \quad \ii \frac{\dd}{\dd t} \ket{\psi (t)} \\
>& = \ii \frac{\dd}{\dd t} \left( Z (t) \e ^ {- \ii t \tilde{h}} \ket{\psi(0)} \right) \\
>& = \ii \dot{Z} (t) \e ^ {- \ii t \tilde{h}} \ket{\psi(0)} + Z (t) \e ^ {- \ii t \tilde{h}} \tilde{h} \ket{\psi(0)} \\
>\text{RHS: } & \quad h (t) \ket{\psi (t)} \\
>& = \left(\ii \dot{Z} (t) Z ^ \dagger (t) + Z (t) \tilde{h} Z ^ \dagger (t)\right) \left( Z (t) \e ^ {- \ii t \tilde{h}} \ket{\psi(0)} \right) \\
>& = \ii \dot{Z} (t) \e ^ {- \ii t \tilde{h}} \ket{\psi(0)} + Z (t) \tilde{h} \e ^ {- \ii t \tilde{h}} \ket{\psi(0)} \\
>\end{align*}
>$$
>

Now compute the dynamical phase angle.

$$
\alpha ^ \text{dyn} (\tau) \defas \int ^ \tau _ 0 \bra{\psi (t ^ \prime)} h (t ^ \prime) \ket{\psi (t ^ \prime)} \dd t ^ \prime \mod{2 \pi}
$$

>$$
>\begin{align*}
>\alpha (\tau) & \defas \int ^ \tau _ 0 \bra{\psi (0)} \e ^ {\ii t ^ \prime \tilde{h}} Z ^ \dagger (t ^ \prime) \left(\ii \dot{Z} (t ^ \prime) Z ^ \dagger (t ^ \prime) + Z (t ^ \prime) \tilde{h} Z ^ \dagger (t ^ \prime)\right) Z (t ^ \prime) \e ^ {- \ii t ^ \prime \tilde{h}} \ket{\psi(0)} \dd t ^ \prime \mod{2 \pi} \\
>& = \int ^ \tau _ 0 \bra{\psi (0)} \e ^ {\ii t ^ \prime \tilde{h}} Z ^ \dagger (t ^ \prime) \ii \dot{Z} (t ^ \prime)  \e ^ {- \ii t ^ \prime \tilde{h}} + \e ^ {\ii t ^ \prime \tilde{h}} \tilde{h} \e ^ {- \ii t ^ \prime \tilde{h}}  \ket{\psi(0)} \dd t ^ \prime \mod{2 \pi} \\
>& = \ii \int ^ \tau _ 0 \bra{\psi (0)} \e ^ {\ii t ^ \prime \tilde{h}} Z ^ \dagger (t ^ \prime) \dot{Z} (t ^ \prime)  \e ^ {- \ii t ^ \prime \tilde{h}} \ket{\psi(0)} \dd t ^ \prime + \int ^ \tau _ 0 \bra{\psi (0)} \e ^ {\ii t ^ \prime \tilde{h}} \tilde{h} \e ^ {- \ii t ^ \prime \tilde{h}}  \ket{\psi(0)} \dd t ^ \prime \mod{2 \pi} \\
>& = \ii \int ^ \tau _ 0 \bra{\psi (0)} \e ^ {\ii t ^ \prime \tilde{h}} Z ^ \dagger (t ^ \prime) \dot{Z} (t ^ \prime)  \e ^ {- \ii t ^ \prime \tilde{h}} \ket{\psi(0)} \dd t ^ \prime + \tau \bra{\psi (0)} \tilde{h}  \ket{\psi(0)} \mod{2 \pi} \\
>\end{align*}
>$$
>

For a cyclic state with the same period as the Hamiltonian ($\tau = T$), the cyclic state vector $\ket{\psi(0)}$ is an eigenvector of the operator $\tilde{h}$. Hence the second term is precisely the total phase angle.

$$
\tau \bra{\psi (0)} \tilde{h}  \ket{\psi(0)} = \alpha (T)
$$

In view of this equation we can directly express the geometric phase in term of the operator $Z(t)$ and its time derivative:

$$
\begin{align*}
\gamma (T) & = \gamma (\mathcal{C}) \defas \alpha ^ \text{dyn} (T) - \alpha (T) \mod{2 \pi} \\
& = \int ^ T _ 0 \ii \bra{\psi (0)} Z ^ \dagger (t ^ \prime) \dot{Z} (t ^ \prime) \ket{\psi (0)} \dd t ^ \prime \mod{2 \pi}
\end{align*}
$$

The operator $Z(t)$ can be used to yield the single-valued vectors $\ket{\phi(t)}$.

$$
\ket{\phi(t)} = Z (t) \ket{\phi(0)}
$$

>$$
>\begin{align*}
>\gamma (T) & = \gamma (\mathcal{C}) \defas \alpha ^ \text{dyn} (T) - \alpha (T) \mod{2 \pi} \\
>& = \int ^ T _ 0 \ii \bra{\psi (0)} Z ^ \dagger (t ^ \prime) \dot{Z} (t ^ \prime) \ket{\psi (0)} \dd t ^ \prime \mod{2 \pi} \\
>& = \int ^ T _ 0 \ii \bra{\psi (0)} Z ^ \dagger (t ^ \prime) \frac{\dd}{\dd t ^ \prime} \left[Z (t ^ \prime) \ket{\psi (0)}\right] \dd t ^ \prime \mod{2 \pi} \\
>& = \int ^ T _ 0 \ii \bra{\phi (t ^ \prime)} \frac{\dd}{\dd t ^ \prime} \ket{\phi (t ^ \prime)} \dd t ^ \prime \mod{2 \pi} \\
>\end{align*}
>$$
>



to-do list:

- [ ] 

References

[1] Pascazio, S. "The geometric phase in quantum systems." (2003): 12345.