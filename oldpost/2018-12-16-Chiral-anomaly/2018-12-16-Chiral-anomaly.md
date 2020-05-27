---
title: Chiral anomaly and Berry phase
category: Physics
tags:
  - Topology
  - Berry phase
  - Chiral anomaly
---

This note follows [Characteristics of chiral anomaly in view of various applications](https://journals.aps.org/prd/pdf/10.1103/PhysRevD.97.016018).

## Berry phase

We adopt the exact nonadiabatic phase in the manner of Aharonov and Anandan for the general Schrödinger problem, which contains enough freedom to describe a possible genuine monopole, as our definition of Berry's phase. To analyze the behavior of Berry's phase away from the precise adiabatic limit quantitatively, we discuss an exactly solvable model which is defined by

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
& H=-\hbar\mu\vec{B}(t)\cdot\vec{\sigma}
\end{align*}
$$

with
$$
\begin{align*}
& \vec{B}(t)=B(\sin\theta\cos\omega t,\sin\theta\sin\omega t,\cos\theta).
\end{align*}
$$
The exact solution of the Schrödinger equation, $\ii \hbar \partial _ t \psi(t)=H \psi(t)$, is given by
$$
\begin{align*}
& \psi _ \pm (t) = w _ \pm (t) \e ^ {-\frac{\ii}{\hbar}\int ^ t _ 0 \dd t ^ \prime w _ \pm ^ \dagger (t ^ \prime)(H-\ii\hbar\partial _ {t ^ \prime})w _ \pm (t ^ \prime)},
\end{align*}
$$
where
$$
\begin{align*}
& w _ + (t) = \begin{pmatrix}
\cos \frac{1}{2}(\theta - \alpha) \e ^ {-\ii\omega t} \\
\sin \frac{1}{2}(\theta-\alpha)
\end{pmatrix},
& w _ - (t) = \begin{pmatrix}
\sin \frac{1}{2}(\theta - \alpha) \e ^ {-\ii\omega t} \\
-\cos \frac{1}{2}(\theta-\alpha)
\end{pmatrix}.
\end{align*}
$$
This solution is confirmed by evaluating
$$
\begin{align*}
\ii \hbar \partial _ t \psi _ \pm(t) & = \ii \hbar \partial _ t \left(w _ \pm (t) \e ^ {-\frac{\ii}{\hbar}\int ^ t _ 0 \dd t ^ \prime w _ \pm ^ \dagger (t ^ \prime)(H-\ii\hbar\partial _ {t ^ \prime})w _ \pm (t ^ \prime)}\right) \\
& = \ii \hbar \partial _ t w _ \pm (t) \e ^ {-\frac{\ii}{\hbar}\int ^ t _ 0 \dd t ^ \prime w _ \pm ^ \dagger (t ^ \prime)(H-\ii\hbar\partial _ {t ^ \prime})w _ \pm (t ^ \prime)} + w _ \pm (t) \e ^ {-\frac{\ii}{\hbar}\int ^ t _ 0 \dd t ^ \prime w _ \pm ^ \dagger (t ^ \prime)(H-\ii\hbar\partial _ {t ^ \prime})w _ \pm (t ^ \prime)}   w _ \pm ^ \dagger (t)(H-\ii\hbar\partial _ {t})w _ \pm (t)\\
& = \left(\ii \hbar \partial _ t w _ \pm (t) + w _ \pm (t)  w _ \pm ^ \dagger (t)(H-\ii\hbar\partial _ {t})w _ \pm (t)\right) \e ^ {-\frac{\ii}{\hbar}\int ^ t _ 0 \dd t ^ \prime w _ \pm ^ \dagger (t ^ \prime)(H-\ii\hbar\partial _ {t ^ \prime})w _ \pm (t ^ \prime)} \\
& = \left(\ii \hbar \partial _ t w _ \pm (t) + w _ \pm (t)  w _ \pm ^ \dagger (t)(H-\ii\hbar\partial _ {t})w _ \pm (t) + w _ \mp (t)  w _ \mp ^ \dagger (t)(H-\ii\hbar\partial _ {t})w _ \pm (t)\right) \e ^ {-\frac{\ii}{\hbar}\int ^ t _ 0 \dd t ^ \prime w _ \pm ^ \dagger (t ^ \prime)(H-\ii\hbar\partial _ {t ^ \prime})w _ \pm (t ^ \prime)} \\
& = \left(\ii \hbar \partial _ t w _ \pm (t) + \left(w _ \pm (t)  w _ \pm ^ \dagger (t) + w _ \mp (t)  w _ \mp ^ \dagger (t)\right) (H-\ii\hbar\partial _ {t})w _ \pm (t) \right) \e ^ {-\frac{\ii}{\hbar}\int ^ t _ 0 \dd t ^ \prime w _ \pm ^ \dagger (t ^ \prime)(H-\ii\hbar\partial _ {t ^ \prime})w _ \pm (t ^ \prime)} \\
& = \left(\ii \hbar \partial _ t w _ \pm (t) + (H-\ii\hbar\partial _ {t})w _ \pm (t) \right) \e ^ {-\frac{\ii}{\hbar}\int ^ t _ 0 \dd t ^ \prime w _ \pm ^ \dagger (t ^ \prime)(H-\ii\hbar\partial _ {t ^ \prime})w _ \pm (t ^ \prime)} \\
& = H w _ \pm (t) \e ^ {-\frac{\ii}{\hbar}\int ^ t _ 0 \dd t ^ \prime w _ \pm ^ \dagger (t ^ \prime)(H-\ii\hbar\partial _ {t ^ \prime})w _ \pm (t ^ \prime)} \\
& = H \psi _ \pm(t) 
\end{align*}
$$
where we used $w _ \mp ^ \dagger [H - \ii \hbar \partial _ t] w _ \pm = 0$ and the completeness relation $w _ + w _ + ^ \dagger + w _ - w _ - ^ \dagger = 1$.

The parameter $\alpha$ is given by 
$$
\begin{align*}
\eta \sin \alpha = \sin (\theta -\alpha)
\end{align*}
$$
or, equivalently, $\tan \alpha = \sin \theta / (\eta + \cos \theta)$, with the parameter $\eta$ defined by
$$
\begin{align*}
& \eta = 2 \hbar \mu B / \hbar \omega = \mu B T / \pi\\
& H=-\frac{1}{2}\eta\hbar\omega\vec{n}(t)\cdot\vec{\sigma}\\
\end{align*}
$$
The exact extra factor for one period of motion 
$$
\begin{align*}
& \quad w _ + ^ \dagger (t)(H-\ii\hbar\partial _ {t})w _ + (t) = \e ^ {- \ii \pi (1 \mp \cos(\theta-\alpha))}
\end{align*}
$$
defines Berry's phase
$$
\begin{align*}
\Omega _ \pm & \equiv 2 \oint \vec{A} _ \pm (\vec{B}) \frac{\dd \vec{B}}{\dd t}\dd t\\
& = 2 \pi (1 \mp \cos (\theta-\alpha))
\end{align*}
$$
where Berry's connection is defined by
$$
\vec{A} _ \pm (\vec{B})=w ^ \dagger _ \pm (t) (-\ii \partial _ \vec{B})w _ \pm (t)
$$
The exact expression of $\Omega _ \pm$ is not topological because of the presence of $\alpha$, which modifies the magnetic flux $\Omega _ +$, for example, from the monopole value
$$
\Omega _ {\text{mono}} = 2 \pi (1-\cos\theta)
$$
The "magnetic monopole" disappears for nonadiabatic limit $\eta\rightarrow 0$ which includes the approach to the spurious monopole position $B\rightarrow 0$ with fixed $T$ or $T\rightarrow 0$ with fixed $B$ in the exact solution; physically, this means that the nonadiabatic phase can't describe a genuine monopole in the nonadiabatic domain such as $B\rightarrow 0$ with fixed $T$.

The vanishing of the monopole more quantitatively, we define the ratio $\Omega _ + / \Omega _ \text{mono}=(1-\cos(\theta-\alpha))/(1-\cos\theta)$ which approaches $\Omega _ + / \Omega _ \text{mono}=\eta^2\cos^2\frac{\theta}{2}$ for $\eta\rightarrow 0$ since we have $\theta-\alpha\simeq\eta\sin\theta$ in this limit. We thus have for the upper half-sphere with $\theta=\pi/2$,
$$
\Omega _ +/\Omega _ \text{mono} = \frac{1}{2}\eta^2
$$
which is an indicator how the monopole flux vanishes in the nonadiabatic limit $\eta = 2 \mu B/\omega \rightarrow 0$. Physically, this shows that the movement of the spin does not follow the rapid movement of $\vec{B}$ or very weak $\vec{B}$; it is well known that Berry's phase is understood as the solid angle subtended by the moving spin
$$
\begin{align*}
\psi _ \pm ^ \dagger (t) \vec{\sigma} \psi _ \pm (t) & = w _ \pm ^ \dagger (t) \vec{\sigma} w _ \pm (t) \\
& = \pm \begin{pmatrix}
\sin (\theta-\alpha) \cos \varphi & \sin (\theta-\alpha) \sin \varphi & \cos (\theta-\alpha)
\end{pmatrix}
\end{align*}
$$
Using the hidden-local gauge symmetry inherent in the second quantized formulation, one can parametrize any solution of the Schrödinger equation $\ii \hbar \partial _ t \psi(t,\vec{x})=\op{H}(t)\psi(t,\vec{x})$ for a general Hamiltonian $\op{H}(t)$, which is cyclic, in the form
$$
\psi(t,\vec{x}) = w(t,\vec{x}) \e ^ {-\frac{\ii}{\hbar}\int _ 0 ^ t \dd t \int \dd ^ 3 x \left[w _ \pm ^ \dagger (t) \op{H}(t) w _ \pm (t) - w _ \pm ^ \dagger (t) \ii \hbar \partial _ t w _ \pm (t)\right]}
$$
with a suitable function $w (t,\vec{x})$ with $w (0,\vec{x})=w(T,\vec{x})$.Our exact solution has this general structure. The nonadiabatic phase (holonomy) in the manner of Aharonov and Anandan is then written as
$$
\begin{align*}
\arg\left\{\psi ^ \dagger (0,\vec{y}) \e ^ {\frac{\ii}{\hbar} \int ^ T _ 0 \dd t \int \dd ^ 3 x \psi ^ \dagger (t,\vec{x}) \ii\hbar \partial _ t \psi (t,\vec{x})} \psi (T,\vec{y}) \right\} = \frac{1}{\hbar} \int ^ T _ 0 \dd t \int \dd ^ 3 x w ^ \dagger (t,\vec{x}) \ii\hbar \partial _ t w (t,\vec{x})
\end{align*}
$$
This shows that Berry's phase used in the present paper for the spatially independent problem with $w(t)$ is the nonadiabatic phase. 

In application of Berry's phase to condensed matter physics, one analyzes a $2\times 2$ energy matrix $h(\vec{p}(t))$ which is a truncation of band structure to the two levels crossing at $\vec{p}(t)=0$. The variable $\vec{p}(t)$ specifies the movement of the electron along the levels in the band structure; in a semiclassical picture, $\frac{\dd}{\dd t} \vec{p}=e[\vec{E}+\vec{v} _ F \times \vec{B}]$. This two-level truncation of the multiband structure is expected to be valid at sufficiently close to the level-crossing point. It is generally expanded as 
$$
h(\vec{p}(t))=\begin{pmatrix}
y _ 0 (t) & 0 \\
0 & y _ 0 (t) 
\end{pmatrix}+ \vec{\sigma} \cdot \vec{y}(t)
$$
where $(y _0,\vec{y})$ are functions of $\vec{p}(t)$. Ignoring the common term $y _ 0(t)$, one may consider a special(Weyl) case $\vec{y}=v _ F \vec{p}$ with $v _ F$ a suitable constant, and one obtains the Hamiltonian with pseudospin,
$$
H = v _ F \vec{\sigma}\cdot \vec{p}(t),
$$


## Communication in BJK prescription

 BJK prescription has worked for all the known cases of anomalous commutators associated with anomalies. We start with the time ordered correlation function of dynamical variables such as
$$
\int _ {-\infty} ^ \infty \dd t \e ^ {\ii \omega t} \avg{T^* x _ k (t) x _ l (0)}
$$
where $T ^*$ stands for the so-called covariant $T$ product, which does not specify the precise equal-time limit $t=0$ of the correlation function. We assume that an explicit form of the correlation function is known by the path integral evaluation, for example. The basic observation of BJL is that, if the above correlation vanishes for $\omega\rightarrow\infty$, one can replace $T^*$ by the conventional $T$ product which is assumed to specify the equal-time limit precisely. This criterion is regarded as an analog of Riemann-Lebesgue lemma in the Fourier transform; is the function $f(t)$ is smooth and well defined around $t=0$, the large frequency limit of $\int ^ \infty _ {-\infty} \dd t \e ^ {\ii \omega t} f(t)$ vanishes. We can thus identify the canonical $T$ product from the quantity defined by the $T^*$ product.

We now examine an explicit effective action for the electron
$$
S=\int \dd t \left[p _ k \dot{x} _ k + A _ k (\vec{x},t) \dot{x} _ k -\mathcal{A} _ k (\vec{p}) \dot{p} _ k - \frac{(\vec{p}-\vec{p} _ F)^2}{2m} \right]
$$
which played a central role in the analyses of anomalous commutation relations induced by Berry's phase. This action is constructed to reproduce the equations of motion in the precise adiabatic limit. $A _ k (\vec{x},t)$ is the electromagnetic potential of which the explicit time dependence is assumed to be very slow in our analysis. The expression of the Berry connection $\mathcal{A} _ k (\vec{p})$ has a well-defined monopole form only in the precise adiabatic limit $\eta = 2 v _ F \abs{\vec{p}} /\hbar\omega\rightarrow\infty$, namely, sufficiently slow time dependence of $\vec{p}(t)$ and sizable $\abs{\vec{p}(t)}$. 

We next observe that canonical communication relations are not modified by any static potential in quantum mechanics. Only the terms with an explicit time derivative such as the kinetic energy term are essential, and the absolute size of the potential such as the harmonic oscillator potential does not matter. We can use the quadratic expansion of the origin of the space of dynamical variables to analyze the commutation relations. We thus consider the quadratic form around $(\vec{x},\vec{p})=(0,\vec{p} _ F)$ by redefining the momentum $(\vec{p}-\vec{p} _ F)\rightarrow \vec{p}$,
$$
S=\int \dd t \left[p _ k \dot{x} _ k + \frac{1}{2}F _ {lk} x _ l \dot{x} _ k -\frac{1}{2}\Omega _ {lk} p _ l \dot{p} _ k - \frac{\vec{p}^2}{2m} \right]
$$

where $F _ {lk} = \partial _ l A _ k(0)-\partial _ k A _ l (0)$ and $\Omega _ {lk} = \partial _ l \mathcal{A} _ k(0)-\partial _ k \mathcal{A} _ l (0)$. One can then confirm the basic correlation function by first integrating over $\vec{p}$ in the path integral $\int \mathcal{D} \vec{x} \mathcal{D}\vec{p}x _ k (t)x _ l (0) \e ^ {(\ii / \hbar)S}$ as
$$
\begin{align*}
\int \dd t \e ^ {\ii \omega t} \avg{T ^ * x _ k (t) x _ l (0)} & = \ii \hbar \left\{[1+\ii m \omega \Omega] ^ {-1} m \omega ^ 2 + \ii \omega F\right\}^ {-1}\\
& = \frac{\ii\hbar}{m\omega^2 + \ii \omega F-m\omega^2\Omega F}(1+\ii m\omega\Omega)
\end{align*}
$$
where it is understood that the $kl$ matrix element of the right-hand side is taken in the following, together with the equation of motion $p _ k =m[\delta _ {kl}-(\Omega F) _ {kl}]\dot{x} _ l$. The correlation vanishes for $\omega\rightarrow \infty$, and thus we can replace $T^*$ by the canonical $T$. We then multiply the both sides by $-\ii\omega$ and consider the large $\omega$ limit. We then obtain
$$
\lim _ {\omega\rightarrow\infty} \int \dd t \e ^{\ii \omega t}\left\{\avg{T\dot{x} _ k (t) x _ l (0)}+ \delta(t)[x _ k (0), x _ l (0)]\right\} = \ii\hbar\frac{1}{1-\Omega F}\Omega
$$
where we used $\frac{\dd}{\dd t}\avg{T x _ k (t) x _ l (0)} = \avg{T \dot{x} _ k(t) x _ l(0)}+\delta(t)[x _ k (0), x _ l (0)]$. We thus conclude
$$
[x _ k(0),x _ l(0)]=\ii\hbar\frac{1}{1-\Omega F}\Omega
$$
and 
$$
\int\dd t \e ^ {\ii\omega t}\avg{T \dot{x} _ k (t) x _ l (0)} = \frac{\hbar\omega}{m\omega^2+\ii\omega F=m\omega^2\Omega F}(1+\ii m \omega\Omega)-\ii\hbar\frac{\Omega}{1-\Omega F}
$$
We then multiply both sides of this relation by $-\ii\omega$ and examine the behavior for $\omega\rightarrow\infty$.Repeating this procedure, we obtain
$$
\begin{align*}
[\dot{x} _ k (0), x _ l (0)] & = -\ii\hbar \left[ \frac{1/m}{1-\Omega F} + \frac{1/m}{1-\Omega F} F \frac{1}{1-\Omega F} \Omega \right]\\
[\dot{x} _ k (0), \dot{x} _ l (0)] & = -\ii\hbar \left[ \frac{1/m}{1-\Omega F}F\frac{1/m}{1-\Omega F} + \frac{1/m}{1-\Omega F} F \frac{1/m}{1-\Omega F} F \frac{1}{1-\Omega F} \Omega \right]
\end{align*}
$$
and $[\ddot {x} _ k (0), x _ l (0)]=-[\dot {x} _ k (0), \dot{x} _ l (0)]$. Here, we briefly comment on what we mean by the high frequency region. When one defines
$$
\mathcal{F}(\omega)=\int\dd t \e ^ {\ii\omega t} \bra{0}T x _ k (t) x _ l (0)\ket{0}
$$
we confirm $\mathcal{F}(\infty)=0$, but $\lim _ {\omega\rightarrow\infty} \omega \mathcal{F}(\omega)\approx\bra{0}[x _ k, x _ l]\ket{0}=\sum _ n (\bra{0}x _ k \ket{n}\bra{n}x _ l \ket{0}-\bra{0}x _ l \ket{n}\bra{n}x _ k \ket{0})$; namely, all the intermediate states contribute with equal weight. 



## References

[1] Fujikawa, Kazuo. "Characteristics of chiral anomaly in view of various applications." Physical Review D 97.1 (2018): 016018.