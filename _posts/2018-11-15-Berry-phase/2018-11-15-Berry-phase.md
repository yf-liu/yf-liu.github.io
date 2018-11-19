---
title: Berry phase
category: Physics
tags:
  - Topology
  - Berry phase
---

[TOC]



## Spinning quantum system in an external magnetic field

Key words: periodic rotation, exact solution, Aharonov-Anandan phase. 

### The parameterization of the Basis Vector

#### Hamiltonian and parameter space

---

Hamiltonian: 

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

h(\vec{R} (t)) = - \frac{B g e}{2 m c} \vec{R} (t) \cdot \op{\vec{J}} = b \vec{R} (t) \cdot \op{\vec{J}}
\label{Hamiltonian_of_system}
$$

with parameter $\vec{R} (t)$ and angular momentum operator $\op{\vec{J}}$. The parameter space is a unit sphere.

$$
\notag
\vec{R} = \left(\begin{matrix}
\sin \theta \cos \varphi\\
\sin \theta \sin \varphi\\
\cos \theta 
\end{matrix}\right)
$$

The path we adapt is to process around $z$ axis, that is, $\varphi = 2 \omega t$.

$$
\vec{R} (t) = \left(\begin{matrix}
\sin \theta \cos 2 \omega t\\
\sin \theta \sin 2 \omega t\\
\cos \theta 
\end{matrix}\right) =  \sin \theta \vec{e} _ {12} (t) + \cos \theta \vec{e} _ {3}
$$

<img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-15-Berry-phase/assets/space_of_parameter.png" width="40%">

where $ \vec{e} _ {12} (t)=\vec{e} _ 1 \cos 2 \omega t + \vec{e} _ 2 \sin 2 \omega t$. The Hamiltonian is

$$
\begin{align*}
h(t) & = b \vec{R} (t) \cdot \op{\vec{J}} \\
& = b ( \sin \theta \vec{e} _ {12} (t) + \cos \theta \vec{e} _ {3}) \cdot \op{\vec{J}}\\
& = b \sin \theta (J _ 1 \cos 2 \omega t + \op{J} _ 2 \sin 2 \omega t ) + b \cos \theta \op{J} _ 3\\
& = b \sin \theta \e ^{- \ii \omega t \op{J} _ 3 } \op{J} _ 1 \e ^{\ii \omega t \op{J} _ 3 } + b \cos \theta \op{J} _ 3 \\
& = \e ^{- \ii \omega t \op{J} _ 3 } (b \sin \theta \op{J} _ 1 + b \cos \theta \op{J} _ 3) \e ^{\ii \omega t \op{J} _ 3 }\\
& = \e ^{- \ii \omega t \op{J} _ 3 } h _ 0 \e ^{\ii \omega t \op{J} _ 3 }
\end{align*}
$$

with the initial Hamiltonian $h _ 0 = b \sin \theta \op{J} _ 1 + b \cos \theta \op{J} _ 3$. The Hamiltonian is periodic, $h (\frac{2\pi}{\omega})=h_0$.

>Using the properties of  angular momentum operator, we prove the above transformation.
>
>- $\e ^{-\ii \omega t  \op{J}  _ 3}  \op{J}  _ 1 \e ^{\ii \omega t  \op{J}  _ 3} =   \op{J}  _ 1 \cos \omega t +  \op{J}  _ 2 \sin \omega t $ :
>
>$$
>\begin{align*}
>& \because \e ^A B \e ^{-A}=B+\sum _ {n=1} ^\infty \frac{B _ n}{n!}, \text{where } B _ 0 \defas B,\ B _ n \defas [A, B _ {n-1}] ;\ [J _ i, \op{J} _ j] = \ii \varepsilon _ {ijk} \op{J} _ k\\
>& \therefore \e ^{-\ii \omega t \op{J} _ 3} \op{J} _ 1 \e ^{\ii \omega t \op{J} _ 3} \\
>& = \op{J} _ 1 + \omega t \op{J} _ 2 - \frac{1}{2!} (\omega t)^2 \op{J} _ 1  + \frac{1}{3!}  (\omega t)^3 \op{J} _ 2 + \cdots \\ 
>& = \op{J} _ 1 (1 - \frac{1}{2!} (\omega t)^2 + \cdots) + \op{J} _ 2 (\omega t  + \frac{1}{3!}  (\omega t)^3 + \cdots) \\ 
>& = \op{J} _ 1 \cos \omega t + \op{J} _ 2 \sin \omega t \\
>\end{align*}
>$$
>
>- $ \e ^{-\ii \omega t  \op{J}  _ 3}  \op{J} _ 3 \e ^{\ii \omega t  \op{J}  _ 3} =  \op{J}  _ 3$ ;
>- Generally, $\e ^{-\ii a  \op{J} _ i}  \op{J}  _ j \e ^{\ii a  \op{J}  _ i} =   \op{J}  _ j (\delta _ {ij} + (1-\delta _ {ij}) \cos a) +  \op{J}  _ k \varepsilon _ {ijk} \sin a$.
>

#### Eigenvectors and eigenvalues

---

The eigenvectors are (can't be proved?)

$$
h(R) \ket{k , R} = b \vec{R} (t) \cdot \op{\vec{J}} \ket{k , R} = b k \ket{k , R}
$$

where $k$ is the quantum number for the component of angular momentum along the changing direction of the external magnetic field, and $R$  refers to $\theta, \ \varphi$ . The eigenvalues $E _ k (R (t)) = b k$ are time-independent, while the eigenvectors and eigen projectors $ \Lambda _ k (R (t)) = \ket{k , R} \bra{k , R}$ are not.

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-15-Berry-phase/assets/time_dependence.png" width="80%">

There are 2 conditions:

- $H^{total}=H_0+h(t)$, where $H_0$ is the rotationally invariant part.
  - Hamiltonian commutes with $\op{\vec{J}} ^2$, so the state vectors $\ket{k, R}$ are also eigenvectors of $\op{\vec{J}} ^2$.
  - But Hamiltonian doesn't commute with $\op{J}_z$. So (why) the possible values of $k$ are

$$
k=-j,-j+1,...,j-1,j,\quad \text{where}\ j \in \frac{\intset}{2}
$$


>$$
>\begin{align*}
>& \quad \ [h(t),\op{\vec{J}} ^2] \\
>& = [ b \vec{R} (t) \cdot \op{\vec{J}},\op{\vec{J}} ^2] \\
>& = b [R _ 1 \op{J} _ 1 + R _ 2 \op{J} _ 2 + R _ 3 \op{J} _ 3,\op{\vec{J}} ^2] \\
>& = b R _ 1 [\op{J} _ 1 ,\op{\vec{J}} ^2]+ b R _ 2 [\op{J} _ 2 ,\op{\vec{J}} ^2] + R _ 3 [\op{J} _ 3,\op{\vec{J}} ^2] \\
>& = 0\\
>& \quad \ [h(t),\op{J} _ 3] \\
>& = [ b \vec{R} (t) \cdot \op{\vec{J}},\op{J} _ 3] \\
>& = b [R _ 1 \op{J} _ 1 + R _ 2 \op{J} _ 2 + R _ 3 \op{J} _ 3,\op{J} _ 3] \\
>& = 2 \ii b (- R _ 1 \op{J} _ 2 + R _ 2 \op{J} _ 1 )\\
>& \ne 0
>\end{align*}
>$$
>


- $H^{total} = \op{\vec{X}} \cdot \op{\vec{J}}+h(t)$, where $\op{\vec{X}} \cdot \op{\vec{J}}$ describes the slowly changing quantum environment for the electron, and $\op{\vec{X}}$ is the position operator of the internuclear axis of the molecule,  rotating in space.
  - Hamiltonian commutes with $\op{\vec{X}} \cdot \op{\vec{J}}$, instead of $\op{\vec{J}} ^2$.
  - The electronic angular momentum is not a good quantum number, because one does not have spherical symmetry but only axial symmetry about the internuclear axis $\op{\vec{X}}$.

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-15-Berry-phase/assets/position_operator.png" width="80%">

>$$
>\begin{align*}
>& \quad \ [h(t),\op{\vec{X}} \cdot \op{\vec{J}}] \\
>& = [ b \vec{R} (t) \cdot \op{\vec{J}},\op{\vec{X}} \cdot \op{\vec{J}}] \\
>& = b [R _ 1 \op{J} _ 1 + R _ 2 \op{J} _ 2 + R _ 3 \op{J} _ 3 , \op{X} _ 1 \op{J} _ 1 + \op{X} _ 2 \op{J} _ 2 + \op{X} _ 3 \op{J} _ 3] \\
>& = b(R _ 1 \op{X} _ 2 - R _ 2 \op{X} _ 1)[\op{J} _ 1, \op{J} _ 2] +  b(R _ 2 \op{X} _ 3 - R _ 3 \op{X} _ 2)[\op{J} _ 2, \op{J} _ 3] + b(R _ 3 \op{X} _ 1 - R _ 1 \op{X} _ 3)[\op{J} _ 3, \op{J} _ 1]  + b R _ 1 [\op{J} _ 1 , \op{X} _ 2] \op{J} _ 2 \\
>& \quad \ + b R _ 1 [\op{J} _ 1 , \op{X} _ 3] \op{J} _ 3 + b R _ 2 [\op{J} _ 2 , \op{X} _ 1] \op{J} _ 1 + b R _ 2 [\op{J} _ 2 , \op{X} _ 3] \op{J} _ 3 + b R _ 3 [\op{J} _ 3 , \op{X} _ 1] \op{J} _ 1 + b R _ 3 [\op{J} _ 3 , \op{X} _ 2] \op{J} _ 2\\
>& = \ii b (R _ 1 \op{X} _ 2 - R _ 2 \op{X} _ 1) \op{J} _ 3 + \ii b (R _ 2 \op{X} _ 3 - R _ 3 \op{X} _ 2) \op{J} _ 1 + \ii b (R _ 3 \op{X} _ 1 - R _ 1 \op{X} _ 3) \op{J} _ 2 \\
>& \quad \ + \ii b R _ 1 \op{X} _ 3 \op{J} _ 2 - \ii b R _ 1 \op{X} _ 2 \op{J} _ 3 - \ii b R _ 2 \op{X} _ 3 \op{J} _ 1 + \ii b R _ 2 \op{X} _ 1 \op{J} _ 3 + \ii b R _ 3 \op{X} _ 2 \op{J} _ 1 - \ii b R _ 3 \op{X} _ 1 \op{J} _ 2 \\
>& = 0\\
>& \quad \ [\op{\vec{X}} \cdot \op{\vec{J}},\op{\vec{J}} ^2] \\
>& = [\op{X} _ 1 \op{J} _ 1 + \op{X} _ 2 \op{J} _ 2 + \op{X} _ 3 \op{J} _ 3, \op{J} _ 1 ^2 + \op{J} _ 2 ^2 + \op{J} _ 3 ^2]\\
>& = [\op{X} _ 1,\op{J} _ 2 ^2] \op{J} _ 1 + [\op{X} _ 1,\op{J} _ 3 ^2] \op{J} _ 1 + [\op{X} _ 2,\op{J} _ 3 ^2] \op{J} _ 2 + [\op{X} _ 2,\op{J} _ 1 ^2] \op{J} _ 2 + [\op{X} _ 3,\op{J} _ 1 ^2] \op{J} _ 3 + [\op{X} _ 3,\op{J} _ 2 ^2] \op{J} _ 3 \\
>& = \ii \op{J} _ 2 \op{X} _ 3 \op{J} _ 1 + \ii \op{X} _ 3 \op{J} _ 2 \op{J} _ 1 - 
>\ii \op{J} _ 3 \op{X} _ 2 \op{J} _ 1 - \ii \op{X} _ 2 \op{J} _ 3 \op{J} _ 1 + 
>\ii \op{J} _ 3 \op{X} _ 1 \op{J} _ 2 + \ii \op{X} _ 1 \op{J} _ 3 \op{J} _ 2  \\
>& \quad - \ii \op{J} _ 1 \op{X} _ 3 \op{J} _ 2 - \ii \op{X} _ 3 \op{J} _ 1 \op{J} _ 2 + \ii \op{J} _ 1 \op{X} _ 2 \op{J} _ 3 + \ii \op{X} _ 2 \op{J} _ 1 \op{J} _ 3 - \ii \op{J} _ 2 \op{X} _ 1 \op{J} _ 3 - \ii \op{X} _ 1 \op{J} _ 2 \op{J} _ 3 + \\
>& =  \op{\vec{X}} \cdot \op{\vec{J}} - \op{\vec{J}} \cdot \op{\vec{X}}  \\
>& \ne 0
>\end{align*}
>$$
>

#### Rotation operator

---

Applying ($\theta,\varphi$)-dependent rotations to an eigenvector $\ket{k , \vec{e}_3}$ gives unit vector along arbitrary direction.

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-15-Berry-phase/assets/rotation_of_e3.png" width="80%">

The representations of rotation operation are 

$$
\begin{align*}
U _ 3 (\varphi) & = \e ^ {-\ii \varphi \op{J} _ 3} \defas \id + \frac{\varphi}{ \ii} \op{J} _ 3 + \frac{1}{2!} \left( \frac{\varphi}{ \ii} \op{J} _ 3 \right)^2 + \cdots \\
U _ 2 (\theta) & = \e ^ {-\ii \theta \op{J} _ 2} \defas \id + \frac{\theta}{\ii} \op{J} _ 2 + \frac{1}{2!} \left( \frac{\theta}{\ii} \op{J} _ 2 \right)^2 + \cdots\\
U ( \theta , \varphi) & = U _ 3 (\varphi) U _ 2 (\theta) U _ 3 (-\varphi)= \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3}\\
\end{align*}
$$

$$
\begin{align*}
& \text{Hermition conjugate: }U ^\dagger (\theta , \varphi) = \e ^ {- \ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3}=U(- \theta , \varphi)\\
& \text{Unitary: } U ^\dagger (\theta , \varphi) U (\theta , \varphi) = \e ^ {- \ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} = \id
\end{align*}
$$

#### Different parameterizations

---

The normalized eigenvector $\ket{k,\vec{e} _ 3}$ of $\op{J} _ 3 = \vec{R} (0, 0) \cdot \vec{J}$ are transformed using the unitary operator $U (\theta, \varphi)$. The resulting vector is an eigenvector of the operator $\vec{R} (\theta , \varphi) \cdot \vec{J}$ with eigenvalue $k$.

$$
\ket{k,\theta, \varphi } \defas U ( \theta , \varphi) \ket{k,\vec{e} _ 3} = U _ 3 (\varphi) U _ 2 (\theta) U _ 3 (-\varphi) \ket{k,\vec{e} _ 3}\\
\vec{R} ( \theta , \varphi )\cdot \op{\vec{J}} \ket{k,\theta, \varphi } = k \ket{k,\theta, \varphi }
$$

For south pole $-\vec{e} _ 3$, the eigenvector $\ket{k,\pi, \varphi } = \e ^{-\ii \pi  \op{J}  _ 2} \e ^ {2 \ii \varphi k}  \ket{k,\vec{e} _ 3}$ has more than one normalized state vectors, obtained with varying $\varphi$. So there is a smooth single-valued vector function everywhere on $S^2$ except at the south pole.

>
>- When $i=2, j=3$ and $a = \pi$, the equation $\e ^{-\ii a J _ i} \op{J} _  j \e ^{\ii a \op{J} _ i} =  \op{J} _ j (\delta _ {ij} + (1-\delta _ {ij}) \cos 2 a) + \op{J} _ k \varepsilon _ {ijk} \sin 2 a$ becomes
>
>$$
>\begin{align*}
>\e ^{-\ii \pi \op{J} _ 2} \op{J} _ 3 \e ^{\ii \pi \op{J} _ 2} & =  \op{J} _ 3 \cos \pi + \op{J} _ 1 \sin \pi = - \op{J} _ 3\\
>\e ^{-\ii \pi \op{J} _ 2} \e ^{- \ii \varphi \op{J} _ 3} \e ^{\ii \pi \op{J} _ 2} & = \e ^{\ii \varphi \op{J} _ 3} \\
>\e ^{-\ii \pi \op{J} _ 2} \e ^{- \ii \varphi \op{J} _ 3}  & = \e ^{\ii \varphi \op{J} _ 3} \e ^{-\ii \pi \op{J} _ 2}\\
>\e ^{-\ii \pi \op{J} _ 2} & = \e ^{\ii \varphi \op{J} _ 3} \e ^{-\ii \pi \op{J} _ 2} \e ^{ \ii \varphi \op{J} _ 3}  \\
>\end{align*}
>$$
>
>- When $\theta=\pi$, the equation $\ket{k,\theta, \varphi } \defas U ( \theta , \varphi) \ket{k,\vec{e} _ 3} = U _ 3 (\varphi) U _ 2 (\theta) U _ 3 (-\varphi) \ket{k,\vec{e} _ 3}$ becomes
>
>$$
>\begin{align*}
>\ket{k,\pi, \varphi } & = U _ 3 (\varphi) U _ 2 (\pi) U _ 3 (-\varphi) \ket{k,\vec{e} _ 3}\\
>& = \e ^ {-\ii \varphi \op{J} _ 3} \e ^ {-\ii \pi \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \ket{k,\vec{e} _ 3}\\
>& = \e ^ {-\ii \varphi \op{J} _ 3} \e ^{ \ii \varphi  \op{J}  _ 3} \e ^{-\ii \pi  \op{J}  _ 2} \e ^{\ii \varphi  \op{J}  _ 3} \e ^ {\ii \varphi \op{J} _ 3} \ket{k,\vec{e} _ 3}\\
>& =\e ^{-\ii \pi  \op{J}  _ 2} \e ^ {2 \ii \varphi \op{J} _ 3}  \ket{k,\vec{e} _ 3}\\
>& =\e ^{-\ii \pi  \op{J}  _ 2} \e ^ {2 \ii \varphi k}  \ket{k,\vec{e} _ 3}\\
>\end{align*}
>$$
>

Using a gauge transformation, the smooth single-valued vector function also can defined on $S^2$ except at the north pole. The gauge transformation is

$$
\ket{k,\theta, \varphi }' = \e ^ {- \ii 2 k \varphi} \ket{k,\theta, \varphi }\\
\text{North pole: }\ket{k,0, \varphi }' = \e ^ {- \ii 2 k \varphi} \ket{k, \vec{e} _ 3}\\
\text{South pole: }\ket{k,\pi, \varphi }' = \e ^ {- \ii 2 k \varphi} \ket{k,\pi, \varphi } = \e ^ {- \ii 2 k \varphi} \e ^{-\ii \pi  \op{J}  _ 2} \e ^ {2 \ii \varphi k}  \ket{k,\vec{e} _ 3} = \e ^{-\ii \pi  \op{J}  _ 2} \ket{k,\vec{e} _ 3}
$$

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-15-Berry-phase/assets/smooth_subspace.png" width="80%">

The projector operators and the corresponding subspaces of these two parameterization in the Hilbert space coincide:

$$
\ket{k,\theta, \varphi } \bra{k,\theta, \varphi } =\ket{k,\theta, \varphi } ' \bra{k,\theta, \varphi } '
$$


### Mead-Berry connection and Berry phase for adiabatic evolutions - magnetic monopole potentials



#### Mead-Berry connection one-form

---

Mead-Berry connection one-form $A^k$ for the adiabatic evolution of the Hamiltonian ($\ref{Hamiltonian_of_system}$) is

$$
A ^ k (R) = A _ i ^ k \dd R ^ i = \ii \bra{k,R} \frac{\partial}{\partial R^i} \ket{k,R} \dd R ^ i\\
$$

where $R^i$ corresponding to $\theta$ and $\varphi$. The matrix of one-forms is

$$
A ^ {k ' k} (R ^ i) = A ^ {k ' k} _ i d R ^ i = \ii \bra{k ',R} \frac{\partial}{\partial R^i} \ket{k,R} \dd R ^ i\\
$$

On the patch $O _ 1$ ($\theta \ne \pi$), we have

$$
A ^ {k'k} _ \theta = \ii \bra{k',\theta,\varphi} \frac{\partial}{\partial \theta} \ket{k,\theta,\varphi}\\
A ^ {k'k} _ \varphi = \ii \bra{k',\theta,\varphi} \frac{\partial}{\partial \varphi} \ket{k,\theta,\varphi}
$$

>$$
>\begin{align*}
>A ^ {k'k} _ \theta & = \ii \bra{k',\theta,\varphi} \frac{\partial}{\partial \theta} \ket{k,\theta,\varphi} \\
>& = \bra{k',\vec{e} _ 3} \ii U ^ \dagger ( \theta , \varphi) \frac{\partial}{\partial \theta} U ( \theta , \varphi) \ket{k,\vec{e} _ 3} \\
>& = \bra{k',\vec{e} _ 3} \ii \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \frac{\partial}{\partial \theta} (\e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} ) \ket{k,\vec{e} _ 3} \\
>& = \bra{k',\vec{e} _ 3} \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {-\ii \theta \op{J} _ 2} \op{J} _ 2 \e ^ {\ii \varphi \op{J} _ 3}  \ket{k,\vec{e} _ 3} \\
>& = \bra{k',\vec{e} _ 3} \e ^ {-\ii \varphi \op{J} _ 3}  \op{J} _ 2 \e ^ {\ii \varphi \op{J} _ 3}  \ket{k,\vec{e} _ 3} \\
>& = \bra{k',\vec{e} _ 3} ( \op{J} _ 2 \cos \varphi -\op{J} _ 1 \sin \varphi ) \ket{k,\vec{e} _ 3} \\
>A ^ {k'k} _ \varphi & = \ii \bra{k',\theta,\varphi} \frac{\partial}{\partial \varphi} \ket{k,\theta,\varphi} \\
>& = \bra{k',\vec{e} _ 3} \ii U ^ \dagger ( \theta , \varphi) \frac{\partial}{\partial \varphi} U ( \theta , \varphi) \ket{k,\vec{e} _ 3} \\
>& = \bra{k',\vec{e} _ 3} \ii \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \frac{\partial}{\partial \varphi} (\e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} ) \ket{k,\vec{e} _ 3} \\
>& = \bra{k',\vec{e} _ 3} ( \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \e ^ {-\ii \varphi \op{J} _ 3}  \op{J} _ 3 \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} - \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \e ^ {-\ii \varphi \op{J} _ 3} \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \op{J} _ 3 ) \ket{k,\vec{e} _ 3} \\
>& = \bra{k',\vec{e} _ 3} ( \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \op{J} _ 3 \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} - \op{J} _ 3 ) \ket{k,\vec{e} _ 3}  \\
>& = \bra{k',\vec{e} _ 3} ( \e ^ {-\ii \varphi \op{J} _ 3}  (\op{J} _ 3\cos \theta - \op{J} _ 1 \sin \theta) \e ^ {\ii \varphi \op{J} _ 3} - \op{J} _ 3 ) \ket{k,\vec{e} _ 3}  \\
>& = \bra{k',\vec{e} _ 3} (\op{J} _ 3 \cos \theta -  ( \op{J} _ 1 \cos \varphi + \op{J} _ 2 \sin \varphi ) \sin \theta  - \op{J} _ 3 ) \ket{k,\vec{e} _ 3}  \\
>& = \bra{k',\vec{e} _ 3} (-  ( \op{J} _ 1 \cos \varphi + \op{J} _ 2 \sin \varphi ) \sin \theta + \op{J} _ 3 ( \cos \theta  - 1 )) \ket{k,\vec{e} _ 3}  \\
>\end {align*}
>$$
>

For diagonal matrix elements, we have

$$
A _ \theta ^ k (\theta , \varphi) = 0 \\
A _ \varphi ^ k (\theta , \varphi) = k (\cos \theta -1)
$$

On the patch $O _ 2(\theta \ne 0)$, we repeat the calculation

$$
A' ^ {k'k} _ \theta = \ii \bra{k',\theta,\varphi} ' \frac{\partial}{\partial \theta} \ket{k,\theta,\varphi} ' \\
A' ^ {k'k} _ \varphi = \ii \bra{k',\theta,\varphi} ' \frac{\partial}{\partial \varphi} \ket{k,\theta,\varphi} '
$$

>$$
>\begin{align*}
>A' ^ {k'k} _ \theta & = \ii \bra{k',\theta,\varphi}' \frac{\partial}{\partial \theta} \ket{k,\theta,\varphi}' \\
>& = \bra{k',\vec{e} _ 3} \ii U ^ \dagger ( \theta , \varphi) \e ^ { \ii 2 k \varphi} \frac{\partial}{\partial \theta} \e ^ {- \ii 2 k \varphi} U ( \theta , \varphi) \ket{k,\vec{e} _ 3} \\
>& = \bra{k',\vec{e} _ 3} \ii \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \e ^ { \ii 2 k \varphi} \frac{\partial}{\partial \theta} (\e ^ {- \ii 2 k \varphi} \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} ) \ket{k,\vec{e} _ 3} \\
>& = \bra{k',\vec{e} _ 3} ( \op{J} _ 2 \cos \varphi -\op{J} _ 1 \sin \varphi ) \ket{k,\vec{e} _ 3} \\
>A' ^ {k'k} _ \varphi & = \ii \bra{k',\theta,\varphi}' \frac{\partial}{\partial \varphi} \ket{k,\theta,\varphi}' \\
>& = \bra{k',\vec{e} _ 3} \ii U ^ \dagger ( \theta , \varphi) \e ^ { \ii 2 k \varphi} \frac{\partial}{\partial \varphi} \e ^ {- \ii 2 k \varphi} U ( \theta , \varphi) \ket{k,\vec{e} _ 3} \\
>& = \bra{k',\vec{e} _ 3} \ii \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \e ^ {- \ii 2 k \varphi} \frac{\partial}{\partial \varphi} (\e ^ {- \ii 2 k \varphi} \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} ) \ket{k,\vec{e} _ 3} \\
>& = \bra{k',\vec{e} _ 3} (-  ( \op{J} _ 1 \cos \varphi + \op{J} _ 2 \sin \varphi ) \sin \theta + \op{J} _ 3 ( \cos \theta  - 1 ) + 2 k)\ket{k,\vec{e} _ 3}  \\
>\end {align*}
>$$
>

For diagonal matrix elements, we have

$$
A ' ^ {k} _ \theta  (\theta , \varphi) = 0 \\
A ' ^ {k} _ \varphi (\theta , \varphi) = k (\cos \theta +1)
$$

Thus, the difference of Mead-Berry connection one-form on two patches is

$$
A ' ^ {k} _ \varphi (\theta , \varphi) - A ^ {k} _ \varphi (\theta , \varphi) = 2 k
$$

#### Mead-Berry curvature two-form

---

The Mead-Berry curvature two-form is defined as

$$
\begin{align*}
F ^ k & = \dd A ^ k \\
& = \frac{\partial A ^ k _ \theta}{\partial \varphi} \dd \varphi \wedge \dd \theta +  \frac{\partial A ^ k _ \varphi}{\partial \theta} \dd \theta \wedge \dd \varphi\\
& = F ^ k _ {\theta \varphi} \dd \theta \wedge \dd \varphi \\
& = - k \sin \theta \dd \theta \wedge \dd \varphi
\end{align*}
$$

>Wedge product (from [Wikipedia](https://en.wikipedia.org/wiki/Exterior_algebra))
>
>The exterior product of two vectors $\vec{u}$ and $\vec{v}$, denoted by $\vec{u} \wedge \vec{v}$, is called a bivector and lives in a space called the exterior square, a vector space that is distinct from the original space of vectors. The magnitude of $\vec{u} \wedge \vec{v}$ can be interpreted as the area of the parallelogram with sides $\vec{u}$ and $\vec{v}$, which in three dimensions can also be computed using the cross product of the two vectors. 
>
>Anticommutative:
>
>$$
>\vec{u} \wedge \vec{v} = - \vec{v} \wedge \vec{u}
>$$
>
>Example:
>
>$$
>\vec{u} = \begin{bmatrix} a \\ b \end{bmatrix} = a \vec{e} _ 1 + b \vec{e} _ 2,\ \vec{v} = \begin{bmatrix} c \\ d \end{bmatrix} = c \vec{e} _ 1 + d \vec{e} _ 2\\
>\text{Area} = \abs{\det \begin{bmatrix} \vec{u} & \vec{v}  \end{bmatrix}} = \abs{\det \begin{bmatrix} a & c \\ b & d \end{bmatrix}} = \abs{ad-bc}\\
>\vec{u} \wedge \vec{v} = ( a \vec{e} _ 1 + b \vec{e} _ 2) ( c \vec{e} _ 1 + d \vec{e} _ 2) = (ad-bc) \vec{e} _ 1 \wedge \vec{e} _ 2
>$$
>
><img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-15-Berry-phase/assets/wedge_product.png" width="50%">
>
>$\dd \theta \wedge \dd \varphi$ :
>
>$$
>\dd \theta \wedge \dd \varphi = \dd \theta \otimes \dd \varphi -\dd \varphi \otimes \dd \theta = - \dd \varphi \wedge \dd \theta
>$$
>
>where $\otimes$ is tensor product.

The curvature two-form $F^k$ is independent of the choice of local coordinates. Using $A'^k$ in $O _ 2$, the curvature is

$$
\begin{align*}
F ^ k & = \dd A' ^ k \\
& = \frac{\partial A' ^ k _ \theta}{\partial \varphi} \dd \varphi \wedge \dd \theta +  \frac{\partial A' ^ k _ \varphi}{\partial \theta} \dd \theta \wedge \dd \varphi\\
& = - k \sin \theta \dd \theta \wedge \dd \varphi
\end{align*}
$$

#### Berry phase

---

Berry phase for a closed path $\mathbf{C}$ is

$$
\gamma _ k (\mathbf{C}) = \int _ S F ^ k = - k \int _ S \sin \theta \dd \theta \wedge \dd \varphi = -k \int _ S \dd \Omega = - k \Omega (\mathbf{C})  \mod 2\pi
$$

>Solid angle:
>
>$$
>\Omega(\mathbf{C}) \defas \int _ S \sin \theta \dd \theta \wedge \dd \varphi
>$$
>

Using $S'$, Berry phase is

$$
\begin{align*}
\gamma _ k (\mathbf{C}) & = \int _ {S'} F ^ k \\
& = - k \int _ {S'} \sin \theta \dd \theta \wedge \dd \varphi \\
& = k \int _ {S^2 \backslash S} \sin \theta \dd \theta \wedge \dd \varphi \\
& = k \int _ {S^2} \sin \theta \dd \theta \wedge \dd \varphi - k \int _ {S} \sin \theta \dd \theta \wedge \dd \varphi \\
& = k (4 \pi - \Omega (\mathbf{C})) \quad \mod 2\pi\\
& = 4 \pi k - k \Omega (\mathbf{C}) \quad \mod 2\pi\\
\end{align*}
$$

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-15-Berry-phase/assets/normal_sphere.png" width="50%">

where $S^2 \backslash S$ denotes the surface with the same area as $S'$ but whose normal points out of the sphere $S^2$. The Berry phase of a loop is unique even using the different coordinates. 

$$
(4 \pi k - k \Omega (\mathbf{C}) ) \mod 2\pi = (- k \Omega (\mathbf{C}) ) \mod 2\pi \\
(4 \pi k ) \mod 2\pi  = 0 \\
k = 0,\pm \frac{1}{2},\pm 1,\pm \frac{3}{2},\pm 2,\cdots
$$

If the state vectors $\ket{k,R}$ are the eigenvectors of $\op{\vec{J}}^2$, then the possible values of $k$ are from $\ref{value_of_k}$. But if not, then is a new result. (See Chapter 6)

#### Mead-Berry (three-)vector potential and curvature three-vector

---

We write the connection one-form $A^k$ as a one-form in $\realset ^3$ in the Cartesian basis ($\dd r, r \dd \theta, r \sin \theta \dd \varphi$).

$$
A ^ k = A ^ k _ r \dd r + A ^ k _ \theta \dd \theta + A ^ k _ \varphi \dd \varphi \\
A ^ k = \op{A} ^ k _ r \dd r + \op{A} ^ k _ \theta r \dd \theta + \op{A} ^ k _ \varphi r \sin \theta \dd \varphi
$$

where the spherical components are defined as

$$
\op{A} ^ k _ r \defas A ^ k _ r = \ii \bra{k,r,\theta,\varphi} \frac{\partial}{\partial r} \ket{k,r,\theta,\varphi}\\
r \op{A} ^ k _ \theta \defas A ^ k _ \theta = \ii \bra{k,r,\theta,\varphi} \frac{\partial}{\partial \theta} \ket{k,r,\theta,\varphi}\\
r \sin \theta \op{A} ^ k _ \varphi \defas A ^ k _ \varphi = \ii \bra{k,r,\theta,\varphi} \frac{\partial}{\partial \varphi} \ket{k,r,\theta,\varphi}
$$

>The line element for an infinitesimal displacement from $(r,\theta,\varphi)$ to $(r + \dd r,\theta + \dd \theta,\varphi + \dd \varphi)$ is
>
>$$
>\dd \vec{r} = \vec{e} _ r \dd r + \vec{e} _ \theta r \dd \theta + \vec{e} _ \varphi r \sin \theta \dd \varphi
>$$
>
>namely,
>
>$$
>\frac{\partial \vec{r}}{\partial \theta} = \vec{e} _ \theta r \\
>\frac{\partial \vec{r}}{\partial \varphi} = \vec{e} _ \varphi r \sin \theta\\
>$$
>
>The gradient is
>
>$$
>\nabla = \frac {\partial}{\partial r} \vec{e} _ r + \frac{1}{r} \frac{\partial}{\partial \theta} \vec{e} _ \theta + \frac{1}{r \sin \theta} \frac{\partial}{\partial \varphi} \vec{e} _ \varphi
>$$
>
>The curl is
>
>$$
>\begin{align*}
>\nabla \times \vec{A} & = \frac{1}{r \sin \theta} \left( \frac{\partial}{\partial \theta} ( A _ \varphi \sin \theta ) - \frac{\partial A _ \theta}{\partial \varphi}  \right) \vec{e} _ r\\
>& \quad + \frac{1}{r} \left( \frac{1}{\sin \theta} \frac{\partial A _ r}{\partial \varphi} - \frac{\partial}{\partial r} (r A _ \varphi) \right) \vec{e} _ \theta\\
>& \quad + \frac{1}{r} \left( \frac{\partial}{\partial r} (r A _ \theta) - \frac{\partial A _ r}{\partial \theta} \right) \vec{e} _ \varphi\\
>\end{align*}
>$$
>

They yields the components of the Mead-Berry vector potential ($r=\text{const.}$) in the spherical coordinates,

$$
\begin{align*}
\op{\vec{A}} ^ k & = \op{A} ^ k _ r \vec{e} _ r + \op{A} ^ k _ \theta \vec{e} _ \theta + \op{A} ^ k _ \varphi \vec{e} _ \varphi = \frac{k ( \cos \theta  - 1 )}{r \sin \theta} \vec{e} _ \varphi \ ,\ \theta \ne \pi \\
\op{\vec{A}}' ^ k & = \op{A} ' ^ k _ r \vec{e} _ r + \op{A} ' ^ k _ \theta \vec{e} _ \theta + \op{A} ' ^ k _ \varphi \vec{e} _ \varphi = \frac{k ( \cos \theta  + 1 )}{r \sin \theta} \vec{e} _ \varphi \ ,\ \theta \ne 0 \\
 \end{align*}
$$

>$$
>\begin{align*}
>\op{\vec{A}} ^ k & = \op{A} ^ k _ r \vec{e} _ r + \op{A} ^ k _ \theta \vec{e} _ \theta + \op{A} ^ k _ \varphi \vec{e} _ \varphi\\
>& = \ii \bra{k,r,\theta,\varphi} ( \vec{e} _ r \frac{\partial}{\partial r} + \vec{e} _ \theta  \frac{1}{r} \frac{\partial}{\partial \theta} +  \vec{e} _ \varphi \frac{1}{r \sin \theta} \frac{\partial}{\partial \varphi} )  \ket{k,r,\theta,\varphi} \\
>& = \ii \bra{k,\vec{e} _ 3} \e ^ {- \ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} ( \vec{e} _ r \frac{\partial}{\partial r} + \vec{e} _ \theta  \frac{1}{r} \frac{\partial}{\partial \theta} +  \vec{e} _ \varphi \frac{1}{r \sin \theta} \frac{\partial}{\partial \varphi} ) \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \ket{k,\vec{e} _ 3} \\
>& = \bra{k,\vec{e} _ 3} ( \vec{e} _ \theta  \frac{1}{r} ( \op{J} _ 2 \cos \varphi -\op{J} _ 1 \sin \varphi ) + \vec{e} _ \varphi \frac{1}{r \sin \theta} (-  ( \op{J} _ 1 \cos \varphi + \op{J} _ 2 \sin \varphi ) \sin \theta + \op{J} _ 3 ( \cos \theta  - 1 )) ) \ket{k,\vec{e} _ 3} \\
>& = \bra{k,\vec{e} _ 3} \vec{e} _ \varphi \frac{1}{r \sin \theta} \op{J} _ 3 ( \cos \theta  - 1 ) \ket{k,\vec{e} _ 3} \\
>& = \bra{k,\vec{e} _ 3} \vec{e} _ \varphi \frac{1}{r \sin \theta} k ( \cos \theta  - 1 ) \ket{k,\vec{e} _ 3} \\
>& = \frac{k ( \cos \theta  - 1 )}{r \sin \theta} \vec{e} _ \varphi \\
>\op{\vec{A}} ' ^ k & = \op{A} ' ^ k _ r \vec{e} _ r + \op{A} ' ^ k _ \theta \vec{e} _ \theta + \op{A} ' ^ k _ \varphi \vec{e} _ \varphi\\
>& = \ii \bra{k,r,\theta,\varphi} ' ( \vec{e} _ r \frac{\partial}{\partial r} + \vec{e} _ \theta  \frac{1}{r} \frac{\partial}{\partial \theta} +  \vec{e} _ \varphi \frac{1}{r \sin \theta} \frac{\partial}{\partial \varphi} )  \ket{k,r,\theta,\varphi} ' \\
>& = \ii \bra{k,\vec{e} _ 3} \e ^ {- \ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} ( \vec{e} _ r \frac{\partial}{\partial r} + \vec{e} _ \theta  \frac{1}{r} \frac{\partial}{\partial \theta} +  \vec{e} _ \varphi \frac{1}{r \sin \theta} \frac{\partial}{\partial \varphi} ) \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \ket{k,\vec{e} _ 3} \\
>& = \bra{k,\vec{e} _ 3} ( \vec{e} _ \theta  \frac{1}{r} ( \op{J} _ 2 \cos \varphi -\op{J} _ 1 \sin \varphi ) + \vec{e} _ \varphi \frac{1}{r \sin \theta} (-  ( \op{J} _ 1 \cos \varphi + \op{J} _ 2 \sin \varphi ) \sin \theta + \op{J} _ 3 ( \cos \theta  - 1 ) + 2 k ) ) \ket{k,\vec{e} _ 3} \\
>& = \bra{k,\vec{e} _ 3} \vec{e} _ \varphi \frac{1}{r \sin \theta} (\op{J} _ 3 ( \cos \theta  - 1 ) + 2 k ) \ket{k,\vec{e} _ 3} \\
>& = \bra{k,\vec{e} _ 3} \vec{e} _ \varphi \frac{1}{r \sin \theta} k ( \cos \theta  + 1 ) \ket{k,\vec{e} _ 3} \\
>& = \frac{k ( \cos \theta + 1 )}{r \sin \theta} \vec{e} _ \varphi \\
> \end{align*}
>$$
>

They are related by the gauge transformation.

$$
\op{\vec{A}} ' ^ k - \op{\vec{A}} ^ k = \frac{2 k}{r \sin \theta} \vec{e} _ \varphi
$$

The corresponding curvature three-vector is

$$
\begin{align*}
\vec{F} ^ k & = \nabla \times \op{\vec{A}} ^ k \\
& = \frac{1}{r \sin \theta} \left( \frac{\partial}{\partial \theta} \frac{k ( \cos \theta  - 1 )}{r } \right) \vec{e} _ r + \frac{1}{r} \left(- \frac{\partial}{\partial r}  \frac{k ( \cos \theta  - 1 )}{ \sin \theta}  \right) \vec{e} _ \theta\\
& = - \frac{k}{r ^ 2} \vec{e} _ r 
\end{align*}
$$

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-15-Berry-phase/assets/three_vector.png" width="70%">

>The analogy between spin in rotating magnetic field and a monopole's magnetic field implies that the existence of monopole can explain why electric charge is always a multiple of elementary charge.
>
>|                                                              |          spin in rotating magnetic field          | a monopole's magnetic field |
>| :----------------------------------------------------------: | :-----------------------------------------------: | :-------------------------: |
>| $\frac{k (\cos \theta - 1)}{r \sin \theta} \vec{e} _ \varphi\quad$ | Mead-Berry (three-)vector potential $\vec{A} ^ k$ | vector potential $\vec{A}$  |
>|             $-\frac{k }{r^2} \vec{e} _ r \quad$              |       curvature three-vector $\vec{F} ^ k$        |  magnetic field $\vec{B}$   |
>|                           integer                            |                       $2 k$                       |     $\frac{e g}{2 \pi}$     |





to-do list:

- [ ] prove $\vec{R} ( \theta , \varphi )\cdot \op{\vec{J}} \ket{k,\theta, \varphi } = k \ket{k,\theta, \varphi }$
- [ ] 

References

[1] Pascazio, S. "The geometric phase in quantum systems." (2003): 12345.