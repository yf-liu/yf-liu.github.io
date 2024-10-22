---
title: The classical limit of Quantum Mechanics
category: Physics
tags:
  - Quantum Mechanics
  - Classical limit
---

## Ehrenfest's theorem

From time dependent Schrödinger equation, we get

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

\begin{align*}
\ket{\dot{\psi}} & = \frac{- \ii}{\hbar} H \ket{\psi}\\
\bra{\dot{\psi}} & = \frac{\ii}{\hbar} \bra{\psi} H ^ \dagger = \frac{\ii}{\hbar} \bra{\psi} H\\
\end{align*}
$$

Assume $\Omega$ has no explicit time dependence. The time evolution of the expectation values is

$$
\begin{align*}
\frac{\dd}{\dd t} \avg{\Omega} & = \frac{\dd}{\dd t} \bra{\psi} \Omega \ket{\psi} \\
& = \bra{\dot{\psi}} \Omega \ket{\psi} + \bra{\psi} \Omega \ket{\dot{\psi}} + \bra{\psi} \dot{\Omega} \ket{\psi} \\
& = \bra{\dot{\psi}} \Omega \ket{\psi} + \bra{\psi} \Omega \ket{\dot{\psi}} \\
& = \frac{\ii}{\hbar} \bra{\psi} H \Omega \ket{\psi} + \frac{- \ii}{\hbar} \bra{\psi} \Omega H \ket{\psi}\\
& = \frac{1}{\ii \hbar} \bra{\psi} [\Omega , H] \ket{\psi}\\
& = \frac{1}{\ii \hbar} \avg{[\Omega , H]}
\end{align*}
$$

## A particle in one dimension

Assume the Hamiltonian is

$$
H = \frac{P ^ 2}{2 m} + V (X)
$$

Consider $\Omega = X$.

$$
\begin{align*}
\frac{\dd}{\dd t} \avg{X} & = \frac{1}{\ii \hbar} \avg{[X , H]} \\
& = \frac{1}{\ii \hbar} \avg{\left[X , \frac{P ^ 2}{2 m} + V (X)\right]} \\
& = \frac{1}{\ii \hbar} \avg{\left[X , \frac{P ^ 2}{2 m} \right]} \\
& = \frac{1}{\ii \hbar} \frac{1}{2 m} \avg{ P \left[X , P \right] + \left[X , P \right] P } \\
& = \frac{1}{\ii \hbar} \frac{1}{2 m} \avg{ P \ii \hbar + \ii \hbar P } \\
& = \frac{\avg{ P } }{m} \\
& = \avg{\frac{\partial H}{\partial P}}
\end{align*}
$$

Consider $\Omega =P $.

$$
\begin{align*}
\frac{\dd}{\dd t} \avg{P} & = \frac{1}{\ii \hbar} \avg{[P , H]} \\
& = \frac{1}{\ii \hbar} \avg{\left[P , \frac{P ^ 2}{2 m} + V (X)\right]} \\
& = \frac{1}{\ii \hbar} \avg{\left[P , V (X) \right]} \\
& = \frac{1}{\ii \hbar} \frac{\hbar}{\ii } \avg{\frac{\dd V}{\dd X}} \\
& = - \avg{\frac{\dd V}{\dd X}} \\
& = \avg{-\frac{\partial H}{\partial X}}
\end{align*}
$$

>To find $[P,V(X)]$, we go to $X$ basis.
>
>$$
>\begin{align*}
>& P \rightarrow - \ii \hbar \frac{\dd}{\dd x} , \ V (X) \rightarrow V (x) , \ [P , V (X)] \rightarrow \left[- \ii \hbar \frac{\dd}{\dd x} , V (x) \right]\\
>& \quad \left[- \ii \hbar \frac{\dd}{\dd x} , V (x) \right] \psi (x) \\
>& = - \ii \hbar \frac{\dd}{\dd x} (V (x) \psi (x)) + \ii \hbar V (x) \frac{\dd}{\dd x} \psi (x)\\
>& = - \ii \hbar \frac{\dd V (x)}{\dd x} \psi (x) - \ii \hbar V (x) \frac{\dd \psi (x)}{\dd x}  + \ii \hbar V (x) \frac{\dd \psi (x)}{\dd x} \\
>& = - \ii \hbar \frac{\dd V (x)}{\dd x} \psi (x) \\
>& [P , V (X)] = - \ii \hbar \frac{\dd V}{\dd X} 
>\end{align*}
>$$
>

## How quantum equation reduce to Hamiltonian equation

Consider a initial state that resembles the states of classical mechanics, i.e., states with well-defined position and momentum, denoted as $\ket{x _ 0 p_ 0 \Delta}$, where $\avg{X} = x _ 0$ and $\avg{P} = p _ 0$, with uncertainties $\Delta X =\Delta$ and $\Delta P \approx \hbar / \Delta$.

>$$
>\ket{x _ 0 p_ 0 \Delta} = \left(\frac{1}{\pi \Delta ^ 2}\right) ^ \frac{1}{4} \e ^ {\ii p _ 0 x / h} \e ^ {- (x - x _ 0) ^ 2 / 2 \Delta ^ 2}\\
>\Delta X = \Delta \approx 10 ^ {-13} \text{cm, which is the size of a proton.} \\
>\Delta P \approx \frac{\hbar}{\Delta} \approx \frac{6.62 \times 10^{-34} \text{m}^2 \text{kg / s}}{ 10 ^ {-13} \text{cm}} = 6.62 \times 10 ^ {-14} \text{cm g / s} \\
>m = 1 \text{ g, which is the mass of a particle.}\\ 
>\Delta V \approx \frac{\Delta P}{m} = \frac{10 ^ {-14} \text{cm g / s}}{1 \text{g}} = 10 ^ {-14} \text{cm/s} \text{ , an uncertainty far below the experimentally detectable range.}
>$$
>

In the classical scale, such a state can be said to have well-defined values for $X$ and $P$, namely $x _ 0$ and $p _ 0$.

$$
\dot{x} _ 0 = \dot {\avg {X}} = \avg{\frac{\partial H}{\partial P}} \approx \left. \frac{\partial H}{\partial P} \right\vert _ {X = x _ 0 , P = p _ 0} = \frac{\partial H (x _ 0 , p _ 0)} {\partial p _ 0} \\
\dot{p} _ 0 = \dot {\avg {P}} = - \avg{\frac{\partial H}{\partial X}} \approx - \left. \frac{\partial H}{\partial X} \right\vert _ {X = x _ 0 , P = p _ 0} = - \frac{\partial H (x _ 0 , p _ 0)} {\partial x _ 0} \\
\label{classical_approxmation}
$$

If we consider some function of $X$ and $P$, we will find in the same approximation.

$$
\omega (x _ 0 , p _ 0) \approx \avg{\Omega (X , P)}
$$

## Is it a good approximation?

The good approximation requires the fluctuation is small. There is no approximation in the first equation in ($\ref{classical_approxmation}$).

$$
\avg{\frac{\partial H}{\partial P}} = \avg{\frac{P}{m}} = \frac{p _ 0}{m}
$$

In the second equation, we need the approximation

$$
\avg{\frac{\partial H}{\partial X}} = \avg{\frac{\dd V}{\dd X}} \approx \left. \frac{\dd V}{\dd x} \right\vert _ {x = x _ 0}
$$

To see when it's a good approximation, let us expand $\frac{\dd V}{\dd x}$ in a Taylor series around $x _ 0$.

$$
\begin{align*}
V ^ \prime (x) & = V ^ \prime (x _ 0) + (x - x _ 0) V ^ {\prime \prime} (x _ 0) + \frac{1}{2} (x - x _ 0) ^ 2 V ^ {\prime \prime \prime} (x _ 0) + \cdots \\
\avg{V ^ \prime (x)} & = \avg{V ^ \prime (x _ 0) + (x - x _ 0) V ^ {\prime \prime} (x _ 0) + \frac{1}{2} (x - x _ 0) ^ 2 V ^ {\prime \prime \prime} (x _ 0) + \cdots} \\
& = V ^ \prime (x _ 0) + \avg{(x - x _ 0)} V ^ {\prime \prime} (x _ 0) + \avg{\frac{1}{2} (x - x _ 0) ^ 2 V ^ {\prime \prime \prime} (x _ 0) + \cdots} \\
& = V ^ \prime (x _ 0) + \frac{1}{2} \avg{(x - x _ 0) ^ 2} V ^ {\prime \prime \prime} (x _ 0) + \avg{\cdots} \\
& = V ^ \prime (x _ 0) + \frac{1}{2} \avg{x ^ 2 - 2 x _ 0 x + x _ 0 ^ 2} V ^ {\prime \prime \prime} (x _ 0) + \avg{\cdots} \\
& = V ^ \prime (x _ 0) + \frac{1}{2} (\avg{x ^ 2} - 2 x _ 0 \avg{x} + x _ 0 ^ 2) V ^ {\prime \prime \prime} (x _ 0) + \avg{\cdots} \\
& = V ^ \prime (x _ 0) + \frac{1}{2} (\avg{x ^ 2} - x _ 0 ^ 2) V ^ {\prime \prime \prime} (x _ 0) + \avg{\cdots} \\
\end{align*}
$$

Each of the terms like $\frac{1}{2} (\avg{x ^ 2} - x _ 0 ^ 2) V ^ {\prime \prime \prime} (x _ 0)$ are products of 2 factors, $\avg{x ^ 2} - x _ 0 ^ 2$ measures the size or nonlocality of the wave packet and $V ^ {\prime \prime \prime} (x _ 0)$, the variation of the force with $x$. They represents that the quantum particle responds to the force at neighboring points as well. These terms are zero if the potential is at most quadratic in the variable $x$. They are negligible if the force varies very little over the size of the wave packet(in the present case, $\Delta \approx 10 ^ {-13} \text{cm}$).

## Apply to the angular momentum in the magnetic field

Hamiltonian

$$
\begin{align*}
H & = b \vec{R} \cdot \op{\vec{J}} \\
& = b \vec{R} \cdot (\op{\vec{X}} \times \op{\vec{P}}) \\
V (\vec{x}) & = b \vec{R} \cdot (\vec{x} \times \vec{p}) \\
\nabla V (\vec{x}) & = \nabla V (\vec{x} _ 0) + h (\vec{x} _ 0) (\vec{x} - \vec{x} _ 0) + \frac{1}{2} \vec{J} _ \vec{\nabla V} ^ 2 (\vec{x} _ 0) \myodot{2} (\vec{x} - \vec{x} _ 0) \otimes (\vec{x} - \vec{x} _ 0) + \cdots \\
\avg{\nabla V (\vec{x})} & = \avg{\nabla V (\vec{x} _ 0) + h (\vec{x} _ 0) (\vec{x} - \vec{x} _ 0) + \frac{1}{2} \vec{J} _ \vec{\nabla V} ^ 2 (\vec{x} _ 0) \myodot{2} (\vec{x} - \vec{x} _ 0) \otimes (\vec{x} - \vec{x} _ 0) + \cdots} \\
& = \nabla V (\vec{x} _ 0) + h (\vec{x} _ 0) \avg{\vec{x} - \vec{x} _ 0} + \frac{1}{2} \vec{J} _ \vec{\nabla V} ^ 2 (\vec{x} _ 0) \myodot{2} \avg{(\vec{x} - \vec{x} _ 0) \otimes (\vec{x} - \vec{x} _ 0)} + \avg{\cdots} \\
& = \nabla V (\vec{x} _ 0) \\
\end{align*}
$$

where $h (\vec{x} _ 0)$ is a $3 \times 3$ matrix whose components are second order derivatives of $V(\vec{x})$ and $3 \times 3 \times 3$ tensor $\vec{J} _ \vec{\nabla V} ^ 2 (\vec{x} _ 0)$ 's components are third order derivatives of $V(\vec{x})$. The third order derivatives of Hamiltonian are $0$.

>The operators performed on escalar, vectorial and tensorial function.
>
>$$
>\begin{align*}
>\text{Scalar } (f(\vec{x}) : \realset ^ M \rightarrow \realset)\text{ : } & \text{grad } f = \nabla f = \vec{e} ^ i \partial _ i \\
>\text{Vector } (\vec{u}(\vec{x}) : \realset ^ M \rightarrow \realset ^ N)\text{ : } & \text{grad } \vec{u} = (\nabla \vec{u}) ^ t = \vec{J} _ \vec{u} \\
>& \text{div } \vec{u} = \nabla \cdot \vec{u} =\partial _ i u ^ i \\
>\text{Tensor } (\vec{F} (\vec{x}) : \realset ^ M \rightarrow \realset ^ N \times \realset ^ N)\text{ : } & \text{grad } \vec{F} = (\nabla \vec{F}) ^ t = \vec{J} _ \vec{F} \\
>& \text{div } \vec{F} = \nabla \cdot \vec{F} ^ t = \vec{e} _ i \partial _ j F ^ {ij}
>\end{align*}
>$$
>
>The vectorial form of the Taylor series is
>
>$$
>\begin{align*}
>\vec{u} (\vec{x}) =\sum _ {k = 0} ^ n \frac{\vec{J} _ \vec{u} ^ k (\vec{x} _ 0)}{k !} \myodot{k} (\vec{x} - \vec{x} _ 0) ^ {k ^ \otimes} 
>\end{align*}
>$$
>

So we can use Ehrenfest's theorem to calculate the trajectory of magnetic momentum.



## References

[1] Shankar, Ramamurti. *Principles of quantum mechanics*. Springer Science & Business Media, 2012.

[2] de Sartenejas, Valle. "TAYLOR SERIES FOR MULTI-VARIABLE FUNCTIONS."