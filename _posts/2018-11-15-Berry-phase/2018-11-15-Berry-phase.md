---
title: Geometric phase of a magnetic dipole in a processing magnetic field
category: Physics
tags:
  - Topology
  - Berry phase
---



This note is following [The Geometric Phase in Quantum Systems: Foundations, Mathematical Concepts, and Applications in Molecular and Condensed Matter Physics](https://cds.cern.ch/record/737299/files/3540000313_TOC.pdf).

## The parameterization of the Basis Vector

### Hamiltonian and parameter space

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
& = b \sin \theta (\op{J} _ 1 \cos 2 \omega t + \op{J} _ 2 \sin 2 \omega t ) + b \cos \theta \op{J} _ 3\\
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
>& = \op{J} _ 1 \cos \omega t + \op{J} _ 2 \sin \omega t 
>\end{align*}
>$$
>
>- $ \e ^{-\ii \omega t  \op{J}  _ 3}  \op{J} _ 3 \e ^{\ii \omega t  \op{J}  _ 3} =  \op{J}  _ 3$ ;
>- Generally, $\e ^{-\ii a  \op{J} _ i}  \op{J}  _ j \e ^{\ii a  \op{J}  _ i} =   \op{J}  _ j (\delta _ {ij} + (1-\delta _ {ij}) \cos a) +  \op{J}  _ k \varepsilon _ {ijk} \sin a$.

### Eigenvectors and eigenvalues

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

### Rotation operator

---

Applying ($\theta,\varphi$)-dependent rotations to an eigenvector $\ket{k , \vec{e}_3}$ gives unit vector along arbitrary direction.

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-15-Berry-phase/assets/rotation_of_e3.png" width="80%">

The representations of rotation operation are 

$$
\begin{align*}
U _ 3 (\varphi) & = \e ^ {-\ii \varphi \op{J} _ 3} \defas \id + \frac{\varphi}{ \ii} \op{J} _ 3 + \frac{1}{2!} \left( \frac{\varphi}{ \ii} \op{J} _ 3 \right)^2 + \cdots \\
U _ 2 (\theta) & = \e ^ {-\ii \theta \op{J} _ 2} \defas \id + \frac{\theta}{\ii} \op{J} _ 2 + \frac{1}{2!} \left( \frac{\theta}{\ii} \op{J} _ 2 \right)^2 + \cdots\\
U ( \theta , \varphi) & = U _ 3 (\varphi) U _ 2 (\theta) U _ 3 (-\varphi)= \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3}
\end{align*}
$$

$$
\begin{align*}
& \text{Hermition conjugate: }U ^\dagger (\theta , \varphi) = \e ^ {- \ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3}=U(- \theta , \varphi)\\
& \text{Unitary: } U ^\dagger (\theta , \varphi) U (\theta , \varphi) = \e ^ {- \ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} = \id
\end{align*}
$$

### Different parameterizations

---

The normalized eigenvector $\ket{k,\vec{e} _ 3}$ of $\op{J} _ 3 = \vec{R} (0, 0) \cdot \vec{J}$ are transformed using the unitary operator $U (\theta, \varphi)$. The resulting vector is an eigenvector of the operator $\vec{R} (\theta , \varphi) \cdot \vec{J}$ with eigenvalue $k$.

$$
\ket{k,\theta, \varphi } \defas U ( \theta , \varphi) \ket{k,\vec{e} _ 3} = U _ 3 (\varphi) U _ 2 (\theta) U _ 3 (-\varphi) \ket{k,\vec{e} _ 3}\\
\vec{R} ( \theta , \varphi )\cdot \op{\vec{J}} \ket{k,\theta, \varphi } = k \ket{k,\theta, \varphi }
$$

For south pole $-\vec{e} _ 3$, the eigenvector $\ket{k,\pi, \varphi } = \e ^{-\ii \pi  \op{J}  _ 2} \e ^ {2 \ii \varphi k}  \ket{k,\vec{e} _ 3}$ has more than one normalized state vectors, obtained with varying $\varphi$. So there is a smooth single-valued vector function everywhere on $S^2$ except at the south pole.

>
>- When $i=2, j=3$ and $a = \pi$, the equation $\e ^{-\ii a J _ i} \op{J} _  j \e ^{\ii a \op{J} _ i} =  \op{J} _ j (\delta _ {ij} + (1-\delta _ {ij}) \cos a) + \op{J} _ k \varepsilon _ {ijk} \sin a​$ becomes
>
>$$
>\begin{align*}
>\e ^{-\ii \pi \op{J} _ 2} \op{J} _ 3 \e ^{\ii \pi \op{J} _ 2} & =  \op{J} _ 3 \cos \pi + \op{J} _ 1 \sin \pi = - \op{J} _ 3\\
>\e ^{-\ii \pi \op{J} _ 2} \e ^{- \ii \varphi \op{J} _ 3} \e ^{\ii \pi \op{J} _ 2} & = \e ^{\ii \varphi \op{J} _ 3} \\
>\e ^{-\ii \pi \op{J} _ 2} \e ^{- \ii \varphi \op{J} _ 3}  & = \e ^{\ii \varphi \op{J} _ 3} \e ^{-\ii \pi \op{J} _ 2}\\
>\e ^{-\ii \pi \op{J} _ 2} & = \e ^{\ii \varphi \op{J} _ 3} \e ^{-\ii \pi \op{J} _ 2} \e ^{ \ii \varphi \op{J} _ 3}  
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
>& =\e ^{-\ii \pi  \op{J}  _ 2} \e ^ {2 \ii \varphi k}  \ket{k,\vec{e} _ 3}
>\end{align*}
>$$
>

Using a gauge transformation, the smooth single-valued vector function also can defined on $S^2$ except at the north pole. The gauge transformation is

$$
\ket{k,\theta, \varphi } ^ \prime = \e ^ {- \ii 2 k \varphi} \ket{k,\theta, \varphi }\\
\begin {cases} \text{North pole: }\ket{k,0, \varphi } ^ \prime = \e ^ {- \ii 2 k \varphi} \ket{k, \vec{e} _ 3}\\
\text{South pole: }\ket{k,\pi, \varphi } ^ \prime = \e ^ {- \ii 2 k \varphi} \ket{k,\pi, \varphi } = \e ^ {- \ii 2 k \varphi} \e ^{-\ii \pi  \op{J}  _ 2} \e ^ {2 \ii \varphi k}  \ket{k,\vec{e} _ 3} = \e ^{-\ii \pi  \op{J}  _ 2} \ket{k,\vec{e} _ 3} 
\end {cases}
$$

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-15-Berry-phase/assets/smooth_subspace.png" width="80%">

The projector operators and the corresponding subspaces of these two parameterization in the Hilbert space coincide:

$$
\ket{k,\theta, \varphi } \bra{k,\theta, \varphi } =\ket{k,\theta, \varphi } ^ \prime \bra{k,\theta, \varphi } ^ \prime
$$


## Mead-Berry connection and Berry phase for adiabatic evolutions - magnetic monopole potentials



### Mead-Berry connection one-form

---

Mead-Berry connection one-form $A^k$ for the adiabatic evolution of the Hamiltonian ($\ref{Hamiltonian_of_system}$) is

$$
A ^ k (R) = A _ i ^ k \dd R ^ i = \ii \bra{k,R} \frac{\partial}{\partial R^i} \ket{k,R} \dd R ^ i
$$

where $R^i$ corresponding to $\theta$ and $\varphi$. The matrix of one-forms is

$$
\begin{align*}
A ^ {k ^ \prime k} (R) & = A ^ {k ^ \prime k} _ i d R ^ i = \ii \bra{k ^ \prime,R} \frac{\partial}{\partial R^i} \ket{k,R} \dd R ^ i \\
& = A ^ {k ^ \prime k} _ \theta d \theta + A ^ {k ^ \prime k} _ \varphi d \varphi = \ii \bra{k ^ \prime,R} \frac{\partial}{\partial \theta} \ket{k,R} \dd \theta + \ii \bra{k ^ \prime,R} \frac{\partial}{\partial \varphi} \ket{k,R} \dd \varphi 
\end{align*}
$$

On the patch $O _ 1$ ($\theta \ne \pi$), we have

$$
A ^ {k ^ \prime k} _ \theta = \ii \bra{k ^ \prime ,\theta,\varphi} \frac{\partial}{\partial \theta} \ket{k,\theta,\varphi}\\
A ^ {k ^ \prime k} _ \varphi = \ii \bra{k ^ \prime ,\theta,\varphi} \frac{\partial}{\partial \varphi} \ket{k,\theta,\varphi}
$$

>$$
>\begin{align*}
>A ^ {k ^ \prime k} _ \theta & = \ii \bra{k ^ \prime ,\theta,\varphi} \frac{\partial}{\partial \theta} \ket{k,\theta,\varphi} \\
>& = \bra{k ^ \prime ,\vec{e} _ 3} \ii U ^ \dagger ( \theta , \varphi) \frac{\partial}{\partial \theta} U ( \theta , \varphi) \ket{k,\vec{e} _ 3} \\
>& = \bra{k ^ \prime ,\vec{e} _ 3} \ii \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \frac{\partial}{\partial \theta} (\e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} ) \ket{k,\vec{e} _ 3} \\
>& = \bra{k ^ \prime ,\vec{e} _ 3} \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {-\ii \theta \op{J} _ 2} \op{J} _ 2 \e ^ {\ii \varphi \op{J} _ 3}  \ket{k,\vec{e} _ 3} \\
>& = \bra{k ^ \prime ,\vec{e} _ 3} \e ^ {-\ii \varphi \op{J} _ 3}  \op{J} _ 2 \e ^ {\ii \varphi \op{J} _ 3}  \ket{k,\vec{e} _ 3} \\
>& = \bra{k ^ \prime ,\vec{e} _ 3} ( \op{J} _ 2 \cos \varphi -\op{J} _ 1 \sin \varphi ) \ket{k,\vec{e} _ 3} \\
>A ^ {k ^ \prime k} _ \varphi & = \ii \bra{k ^ \prime ,\theta,\varphi} \frac{\partial}{\partial \varphi} \ket{k,\theta,\varphi} \\
>& = \bra{k ^ \prime ,\vec{e} _ 3} \ii U ^ \dagger ( \theta , \varphi) \frac{\partial}{\partial \varphi} U ( \theta , \varphi) \ket{k,\vec{e} _ 3} \\
>& = \bra{k ^ \prime ,\vec{e} _ 3} \ii \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \frac{\partial}{\partial \varphi} (\e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} ) \ket{k,\vec{e} _ 3} \\
>& = \bra{k ^ \prime ,\vec{e} _ 3} ( \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \e ^ {-\ii \varphi \op{J} _ 3}  \op{J} _ 3 \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} - \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \e ^ {-\ii \varphi \op{J} _ 3} \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \op{J} _ 3 ) \ket{k,\vec{e} _ 3} \\
>& = \bra{k ^ \prime ,\vec{e} _ 3} ( \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \op{J} _ 3 \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} - \op{J} _ 3 ) \ket{k,\vec{e} _ 3}  \\
>& = \bra{k ^ \prime ,\vec{e} _ 3} ( \e ^ {-\ii \varphi \op{J} _ 3}  (\op{J} _ 3\cos \theta - \op{J} _ 1 \sin \theta) \e ^ {\ii \varphi \op{J} _ 3} - \op{J} _ 3 ) \ket{k,\vec{e} _ 3}  \\
>& = \bra{k ^ \prime ,\vec{e} _ 3} (\op{J} _ 3 \cos \theta -  ( \op{J} _ 1 \cos \varphi + \op{J} _ 2 \sin \varphi ) \sin \theta  - \op{J} _ 3 ) \ket{k,\vec{e} _ 3}  \\
>& = \bra{k ^ \prime ,\vec{e} _ 3} (-  ( \op{J} _ 1 \cos \varphi + \op{J} _ 2 \sin \varphi ) \sin \theta + \op{J} _ 3 ( \cos \theta  - 1 )) \ket{k,\vec{e} _ 3}  
>\end {align*}
>$$
>

For diagonal matrix elements, we have

$$
A _ \theta ^ k (\theta , \varphi) = 0 \\
A _ \varphi ^ k (\theta , \varphi) = k (\cos \theta -1)
\label{connection}
$$

On the patch $O _ 2(\theta \ne 0)$, we repeat the calculation

$$
A ^ {\prime k^ \prime k} _ \theta = \ii \bra{k ^ \prime,\theta,\varphi} ^ \prime \frac{\partial}{\partial \theta} \ket{k,\theta,\varphi} ^ \prime \\
A ^ {\prime k^ \prime k} _ \varphi = \ii \bra{k^ \prime,\theta,\varphi} ^ \prime \frac{\partial}{\partial \varphi} \ket{k,\theta,\varphi} ^ \prime
$$

>$$
>\begin{align*}
>A ^ {\prime k ^ \prime k} _ \theta & = \ii \bra{k ^ \prime ,\theta,\varphi} ^ \prime  \frac{\partial}{\partial \theta} \ket{k,\theta,\varphi} ^ \prime  \\
>& = \bra{k ^ \prime ,\vec{e} _ 3} \ii U ^ \dagger ( \theta , \varphi) \e ^ { \ii 2 k \varphi} \frac{\partial}{\partial \theta} \e ^ {- \ii 2 k \varphi} U ( \theta , \varphi) \ket{k,\vec{e} _ 3} \\
>& = \bra{k ^ \prime ,\vec{e} _ 3} \ii \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \e ^ { \ii 2 k \varphi} \frac{\partial}{\partial \theta} (\e ^ {- \ii 2 k \varphi} \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} ) \ket{k,\vec{e} _ 3} \\
>& = \bra{k ^ \prime ,\vec{e} _ 3} ( \op{J} _ 2 \cos \varphi -\op{J} _ 1 \sin \varphi ) \ket{k,\vec{e} _ 3} \\
>A ^ {\prime k ^ \prime k} _ \varphi & = \ii \bra{k ^ \prime , \theta , \varphi} ^ \prime \frac{\partial}{\partial \varphi} \ket{k , \theta , \varphi} ^ \prime \\
>& = \bra{k ^ \prime,\vec{e} _ 3} \ii U ^ \dagger ( \theta , \varphi) \e ^ { \ii 2 k \varphi} \frac{\partial}{\partial \varphi} \e ^ {- \ii 2 k \varphi} U ( \theta , \varphi) \ket{k,\vec{e} _ 3} \\
>& = \bra{k ^ \prime,\vec{e} _ 3} \ii \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \e ^ {- \ii 2 k \varphi} \frac{\partial}{\partial \varphi} (\e ^ {- \ii 2 k \varphi} \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} ) \ket{k,\vec{e} _ 3} \\
>& = \bra{k ^ \prime,\vec{e} _ 3} (-  ( \op{J} _ 1 \cos \varphi + \op{J} _ 2 \sin \varphi ) \sin \theta + \op{J} _ 3 ( \cos \theta  - 1 ) + 2 k)\ket{k,\vec{e} _ 3}  
>\end {align*}
>$$
>

For diagonal matrix elements, we have

$$
A ^ {\prime k} _ \theta  (\theta , \varphi) = 0 \\
A ^ {\prime k} _ \varphi (\theta , \varphi) = k (\cos \theta +1)
$$

Thus, the difference of Mead-Berry connection one-form on two patches is

$$
A ^ {\prime k} _ \varphi (\theta , \varphi) - A ^ {k} _ \varphi (\theta , \varphi) = 2 k
$$

### Mead-Berry curvature two-form

---

The Mead-Berry curvature two-form is defined as

$$
\begin{align*}
F ^ k & = \dd A ^ k \\
& = \frac{\partial A ^ k _ \theta}{\partial \varphi} \dd \varphi \wedge \dd \theta +  \frac{\partial A ^ k _ \varphi}{\partial \theta} \dd \theta \wedge \dd \varphi \\
& = - k \sin \theta \dd \theta \wedge \dd \varphi \\
& = F ^ k _ {\theta \varphi} \dd \theta \wedge \dd \varphi 
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

The curvature two-form $F^k$ is independent of the choice of local coordinates. Using $A ^{\prime k}$ in $O _ 2$, the curvature is

$$
\begin{align*}
F ^ k & = \dd A ^{\prime k} \\
& = \frac{\partial A ^{\prime k} _ \theta}{\partial \varphi} \dd \varphi \wedge \dd \theta +  \frac{\partial A ^{\prime k} _ \varphi}{\partial \theta} \dd \theta \wedge \dd \varphi\\
& = - k \sin \theta \dd \theta \wedge \dd \varphi
\end{align*}
$$

### Berry phase

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

Using $S ^ \prime$, Berry phase is

$$
\begin{align*}
\gamma _ k (\mathbf{C}) & = \int _ {S ^ \prime} F ^ k \\
& = - k \int _ {S ^ \prime} \sin \theta \dd \theta \wedge \dd \varphi \\
& = k \int _ {S^2 \backslash S} \sin \theta \dd \theta \wedge \dd \varphi \\
& = k \int _ {S^2} \sin \theta \dd \theta \wedge \dd \varphi - k \int _ {S} \sin \theta \dd \theta \wedge \dd \varphi \\
& = k (4 \pi - \Omega (\mathbf{C})) \quad \mod 2\pi\\
& = 4 \pi k - k \Omega (\mathbf{C}) \quad \mod 2\pi
\end{align*}
$$

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-15-Berry-phase/assets/normal_sphere.png" width="50%">

where $S^2 \backslash S$ denotes the surface with the same area as $S ^ \prime$ but whose normal points out of the sphere $S^2$. The Berry phase of a loop is unique even using the different coordinates. 

$$
(4 \pi k - k \Omega (\mathbf{C}) ) \mod 2\pi = (- k \Omega (\mathbf{C}) ) \mod 2\pi \\
(4 \pi k ) \mod 2\pi  = 0 \\
k = 0,\pm \frac{1}{2},\pm 1,\pm \frac{3}{2},\pm 2,\cdots
$$

If the state vectors $\ket{k,R}$ are the eigenvectors of $\op{\vec{J}}^2$, then the possible values of $k$ are from $\ref{value_of_k}$. But if not, then is a new result. (See Chapter 6)

### Mead-Berry (three-)vector potential and curvature three-vector

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
>\frac{\partial \vec{r}}{\partial \varphi} = \vec{e} _ \varphi r \sin \theta
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
>& \quad + \frac{1}{r} \left( \frac{\partial}{\partial r} (r A _ \theta) - \frac{\partial A _ r}{\partial \theta} \right) \vec{e} _ \varphi
>\end{align*}
>$$
>

They yields the components of the Mead-Berry vector potential ($r=\text{const.}$) in the spherical coordinates,

$$
\begin{align*}
\op{\vec{A}} ^ k & = \op{A} ^ k _ r \vec{e} _ r + \op{A} ^ k _ \theta \vec{e} _ \theta + \op{A} ^ k _ \varphi \vec{e} _ \varphi = \frac{k ( \cos \theta  - 1 )}{r \sin \theta} \vec{e} _ \varphi \ ,\ \theta \ne \pi \\
\op{\vec{A}} ^ {\prime k} & = \op{A} ^ {\prime k} _ r \vec{e} _ r + \op{A} ^ {\prime k} _ \theta \vec{e} _ \theta + \op{A} ^ {\prime k} _ \varphi \vec{e} _ \varphi = \frac{k ( \cos \theta  + 1 )}{r \sin \theta} \vec{e} _ \varphi \ ,\ \theta \ne 0 
 \end{align*}
$$

>$$
>\begin{align*}
>\op{\vec{A}} ^ k & = \ii \bra{k,r,\theta,\varphi} \nabla \ket{k,r,\theta,\varphi} \\
>& = \ii \bra{k,r,\theta,\varphi} ( \vec{e} _ r \frac{\partial}{\partial r} + \vec{e} _ \theta  \frac{1}{r} \frac{\partial}{\partial \theta} +  \vec{e} _ \varphi \frac{1}{r \sin \theta} \frac{\partial}{\partial \varphi} )  \ket{k,r,\theta,\varphi} \\
>& = \ii \bra{k,\vec{e} _ 3} \e ^ {- \ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} ( \vec{e} _ r \frac{\partial}{\partial r} + \vec{e} _ \theta  \frac{1}{r} \frac{\partial}{\partial \theta} +  \vec{e} _ \varphi \frac{1}{r \sin \theta} \frac{\partial}{\partial \varphi} ) \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \ket{k,\vec{e} _ 3} \\
>& = \bra{k,\vec{e} _ 3} ( \vec{e} _ \theta  \frac{1}{r} ( \op{J} _ 2 \cos \varphi -\op{J} _ 1 \sin \varphi ) + \vec{e} _ \varphi \frac{1}{r \sin \theta} (-  ( \op{J} _ 1 \cos \varphi + \op{J} _ 2 \sin \varphi ) \sin \theta + \op{J} _ 3 ( \cos \theta  - 1 )) ) \ket{k,\vec{e} _ 3} \\
>& = \bra{k,\vec{e} _ 3} \vec{e} _ \varphi \frac{1}{r \sin \theta} \op{J} _ 3 ( \cos \theta  - 1 ) \ket{k,\vec{e} _ 3} \\
>& = \bra{k,\vec{e} _ 3} \vec{e} _ \varphi \frac{1}{r \sin \theta} k ( \cos \theta  - 1 ) \ket{k,\vec{e} _ 3} \\
>& = \frac{k ( \cos \theta  - 1 )}{r \sin \theta} \vec{e} _ \varphi \\
>\op{\vec{A}} ^ {\prime k} & = \ii \bra{k,r,\theta,\varphi} ^ \prime \nabla \ket{k,r,\theta,\varphi} ^ \prime \\
>& = \ii \bra{k,r,\theta,\varphi} ^ \prime ( \vec{e} _ r \frac{\partial}{\partial r} + \vec{e} _ \theta  \frac{1}{r} \frac{\partial}{\partial \theta} +  \vec{e} _ \varphi \frac{1}{r \sin \theta} \frac{\partial}{\partial \varphi} )  \ket{k,r,\theta,\varphi} ^ \prime \\
>& = \ii \bra{k,\vec{e} _ 3} \e ^ {- \ii \varphi \op{J} _ 3}  \e ^ {\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} ( \vec{e} _ r \frac{\partial}{\partial r} + \vec{e} _ \theta  \frac{1}{r} \frac{\partial}{\partial \theta} +  \vec{e} _ \varphi \frac{1}{r \sin \theta} \frac{\partial}{\partial \varphi} ) \e ^ {-\ii \varphi \op{J} _ 3}  \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \varphi \op{J} _ 3} \ket{k,\vec{e} _ 3} \\
>& = \bra{k,\vec{e} _ 3} ( \vec{e} _ \theta  \frac{1}{r} ( \op{J} _ 2 \cos \varphi -\op{J} _ 1 \sin \varphi ) + \vec{e} _ \varphi \frac{1}{r \sin \theta} (-  ( \op{J} _ 1 \cos \varphi + \op{J} _ 2 \sin \varphi ) \sin \theta + \op{J} _ 3 ( \cos \theta  - 1 ) + 2 k ) ) \ket{k,\vec{e} _ 3} \\
>& = \bra{k,\vec{e} _ 3} \vec{e} _ \varphi \frac{1}{r \sin \theta} (\op{J} _ 3 ( \cos \theta  - 1 ) + 2 k ) \ket{k,\vec{e} _ 3} \\
>& = \bra{k,\vec{e} _ 3} \vec{e} _ \varphi \frac{1}{r \sin \theta} k ( \cos \theta  + 1 ) \ket{k,\vec{e} _ 3} \\
>& = \frac{k ( \cos \theta + 1 )}{r \sin \theta} \vec{e} _ \varphi 
> \end{align*}
>$$
>

They are related by the gauge transformation.

$$
\op{\vec{A}} ^ {\prime k} - \op{\vec{A}} ^ k = \frac{2 k}{r \sin \theta} \vec{e} _ \varphi
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

## The exact solution of the Schrödinger equation

Schrödinger equation:

$$
\ii \frac{\partial}{\partial t} \psi (t) = h (t) \psi (t),\text{ with } h(t) = b \vec{R} (\theta , \omega t) \cdot \vec{J}
$$

The cyclic evolution is

$$
\ket{\psi (\tau)} \bra{\psi (\tau)} = \ket{\psi (0)} \bra{\psi (0)}
$$

### Adiabatic approximation has a problem

---

We shall first consider the case where the adiabatic approximation is valid.

$$
\begin{align*}
& \because h (\vec{R}) \ket{k,R} = b \vec{R} \cdot \op{\vec{J}} \ket{k,R} = b k \ket{k,R},\
\gamma _ k (\mathbf{C} _ 1) = - 2 \pi k (1 - \cos \theta)\\
& \therefore \psi (t) \myeq \e ^ {- \ii \int ^ t _ 0 E _ n (t ^ \prime) \dd t ^ \prime} \e ^ {\ii \gamma _ k (t)} \ket{k , R (t)}
= \e ^ {- \ii  b k t } \e ^ {\ii \gamma _ k (t)} \ket{k , \theta , \omega t},\ \text{where } \gamma _ k (t) = \frac{t}{T} \gamma _ k (\mathbf{C} _ 1) 
\end{align*}
$$

In particular for $t=T$, 

$$
\psi (T) \myeq \e ^ {- \ii  b k \frac{2 \pi}{\omega}} \e ^ {\ii \gamma _ k (\mathbf{C} _ 1) } \ket{k , \theta , 0} = \e ^ {- \ii  b k \frac{2 \pi}{\omega}} \e ^ {\ii \gamma _ k (\mathbf{C} _ 1) } \psi (0)
\label{adiabatic_psi}
$$

But the results of adiabatic approximation aren't compatible with the Schrödinger equation.

>We substitute ($\ref{adiabatic_psi}$) in Schrödinger equation,
>
>$$
>\begin{align*}
>\ii \frac{\partial}{\partial t} \psi (t) & = b \vec{R} (\theta , \omega t) \cdot \vec{J} \psi (t) \\
>\ii \frac{\partial}{\partial t} \e ^ {- \ii  b k t } \e ^ {\ii \gamma _ k (t)} \ket{k , \theta , \omega t} & = b \e ^ {- \ii  b k t } \e ^ {\ii \gamma _ k (t)} \vec{R} (\theta , \omega t) \cdot \vec{J} \ket{k , \theta , \omega t} \\
>(bk - \frac{\partial \gamma _ k (t)}{\partial t}) \e ^ {- \ii  b k t } \e ^ {\ii \gamma _ k (t)} \ket{k , \theta , \omega t} & = b k \e ^ {- \ii  b k t } \e ^ {\ii \gamma _ k (t)}  \ket{k , \theta , \omega t} 
>\end{align*}
>$$
>
>The equation has an extra $\frac{\partial \gamma _ k (t)}{\partial t}$, which is omitted in the adiabatic approximation.

### Transformation of coordinate

---

The unitary transformation of the state vector $\psi (t)$ is

$$
\tilde{U} (t) \defas U _ 3 ^ \dagger (\omega t) = \e ^ {\ii \omega t \op{J} _ 3}\\
\begin{cases}\psi ^ \prime (t) = \tilde{U} (t) \psi (t) = \e ^ {\ii \omega t \op{J} _ 3} \psi (t) \\
\psi (t) = \tilde{U} ^ \dagger (t) \psi ^ \prime (t) = \e ^ {- \ii \omega t \op{J} _ 3} \psi ^ \prime (t) \end{cases}
$$

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-15-Berry-phase/assets/coordinate_transformation.png" width="90%">

> With the transformation, the Schrödinger equation becomes
>
> $$
> \ii \frac{\partial}{\partial t} (\e ^ {- \ii \omega t \op{J} _ 3} \psi^ \prime(t))  = h (t) \e ^ {- \ii \omega t \op{J} _ 3} \psi ^ \prime (t)\\
> \omega \e ^ {- \ii \omega t \op{J} _ 3} \op{J} _ 3 \psi ^ \prime (t) + \ii \e ^ {- \ii \omega t \op{J} _ 3} \frac{\partial}{\partial t} \psi ^ \prime (t) = h (t) \e ^ {- \ii \omega t \op{J} _ 3} \psi ^ \prime (t)\\
> \omega \op{J} _ 3 \psi ^ \prime (t) + \ii \frac{\partial}{\partial t} \psi ^ \prime (t) = \e ^ { \ii \omega t \op{J} _ 3} h (t) \e ^ {- \ii \omega t \op{J} _ 3} \psi ^ \prime (t)\\
> \ii \frac{\partial}{\partial t} \psi ^ \prime (t) = (\e ^ { \ii \omega t \op{J} _ 3} h (t) \e ^ {- \ii \omega t \op{J} _ 3} - \omega \op{J} _ 3) \psi ^ \prime (t)\\
> \ii \frac{\partial}{\partial t} \psi ^ \prime (t) = (\e ^ { \ii \omega t \op{J} _ 3}  \e ^{- \ii \omega t \op{J} _ 3 } h _ 0 \e ^{\ii \omega t \op{J} _ 3 } \e ^ {- \ii \omega t \op{J} _ 3} - \omega \op{J} _ 3) \psi ^ \prime (t)\\
> \ii \frac{\partial}{\partial t} \psi ^ \prime (t) = (h _ 0 - \omega \op{J} _ 3) \psi ^ \prime (t)\\
> \ii \frac{\partial}{\partial t} \psi ^ \prime (t) = (b \sin \theta \op{J} _ 1 + b \cos \theta \op{J} _ 3 - \omega \op{J} _ 3) \psi ^ \prime (t)\\
> $$
>

The Hamiltonian doesn't change with time, and can be related to the angular momentum. 

$$
\begin{align*}
h ^ \prime (t) & = b (\cos \theta \op{J} _ 3 + \sin \theta \op{J} _ 1 - \frac{\omega}{b} \op{J} _ 3) \defas H = \Omega \vec{e} \cdot \vec{J}
\end{align*}
$$

where $\Omega =  b \sqrt{1 + \frac{\omega}{b} (-2 \cos \theta + \frac{\omega}{b})}$ can be treated as new angular frequency of magnetic momentum like $b$, and $\vec{e} = \frac{b}{\Omega}  \left( \left( \cos \theta - \frac{\omega}{b} \right) \vec {e} _ 3 + \sin \theta \vec{e} _ 1 \right)$ can be treated as new rotating axis like $\vec{R}$. 

>The equation above can be easily proved.
>
>$$
>\begin {align*}
>H & = \Omega \vec{e} \cdot \vec{J}\\
>& = \Omega \frac{b}{\Omega}  \left( \left( \cos \theta - \frac{\omega}{b} \right) \vec {e} _ 3 + \sin \theta \vec{e} _ 1 \right) \cdot (\op{J} _ 1 \vec {e} _ 1 + \op{J} _ 2 \vec {e} _ 2 + \op{J} _ 3 \vec {e} _ 3) \\
>& = b \left( \left( \cos \theta - \frac{\omega}{b} \right) \op{J} _ 3 + \sin \theta \op{J} _ 1 \right)
>\end {align*}
>$$
>

The evolution of $\vec{e}$ is along a larger circle on the unit sphere than $\vec{R}$.

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-15-Berry-phase/assets/e_evolution.png" width="90%">

>It means the rotating axis has a slight offset. The offset can be calculated as follows.
>
>$$
>\begin {align*}
>& \vec{e} = \cos \tilde{\theta} \vec{e} _ 3 + \sin \tilde{\theta} \vec{e} _ 1 = \vec{R} (\tilde{\theta} , 0) \\
>& \begin{cases} \cos \tilde{\theta} = \frac{b}{\Omega} (\cos \theta - \frac{\omega}{b}) \\ 
>\sin \tilde{\theta} = \frac{b}{\Omega} \sin \theta \end{cases}
>\end {align*}
>$$
>
><img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-15-Berry-phase/assets/tilde_theta.png" width="25%">
>
>Imbedded into the $\realset ^ 3$, the transformation of $\theta$ to $\tilde{\theta}$ is easier to understand.
>
>$$
>\begin {align*}
>& F _ \nu (\vec{R} (\theta , 0)) = \vec{R} (\cos ^ {-1} \frac{\cos \theta - \nu}{\sqrt{\nu ^ 2 -2 \cos \theta \nu + 1}}, 0) = \vec{R} (\tilde{\theta}, 0) \\
>& F _ \nu (x ^ 1, 0, x ^ 3) = \frac{(x ^ 1, 0, x ^ 3 - \nu)}{\sqrt{(x ^ 1) ^ 2  + (x ^ 3 - \nu) ^ 2}} = (\tilde {x} ^ 1, 0, \tilde {x} ^ 3) 
>\end {align*}
>$$
>
>where $\nu=\frac{\omega}{b}$ is a constant.
>
><img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-15-Berry-phase/assets/transformation_theta.png" width="90%">


|                  |                           Old way                            |                           New way                            |
| ---------------- | :----------------------------------------------------------: | :----------------------------------------------------------: |
| State vector     |                          $\psi (t)$                          | $\psi ^ \prime (t) = \e ^ {\ii \omega t \op{J} _ 3} \psi (t)$ |
| Hamiltonian      | $h (t) = \e ^ {- \ii \omega t \op{J} _ 3} h _ 0 \e ^ {\ii \omega t \op{J} _ 3}$ | $h ^ \prime (t) = \e ^ { \ii \omega t \op{J} _ 3} h (t) \e ^ {- \ii \omega t \op{J} _ 3} - \omega \op{J} _ 3$ |
| Observable       | $\bra{\psi (t)} h (t) \ket{\psi (t)}  = \bra{\psi (t)} \e ^ {- \ii \omega t \op{J} _ 3} h _ 0 \e ^ {\ii \omega t \op{J} _ 3} \ket{\psi (t)}$ | $\bra{\psi ^ \prime (t)} h _ 0 \ket{\psi ^ \prime (t)}  = \bra{\e ^ {\ii \omega t \op{J} _ 3} \psi (t)} h _ 0 \ket{\e ^ {\ii \omega t \op{J} _ 3} \psi (t)}$ |
| Schrödinger eqn. | $\ii \frac{\partial}{\partial t} \psi (t) = h (t) \psi (t)$  | $\ii \frac{\partial}{\partial t} \psi ^ \prime (t) = h ^ \prime (t) \psi ^ \prime (t)$ |

### General Solution

---

The new Schrödinger equation can be integrated immediately.

$$
\begin{align*}
\psi ^ \prime (t) & = \e ^ {- \ii H t} \psi ^ \prime (0)\\
& = \e ^ {- \ii \Omega \vec{e} \cdot \vec{J} t} \psi ^ \prime (0)\\
& = \e ^ {- \ii \Omega t \vec{R}  (\tilde{\theta} , 0) \cdot \op{\vec{J}}} \psi ^ \prime (0)
\end{align*}
$$

which represents a 'rotation' of the state vector $\psi ^ \prime _ 0$ by an angular momentum $\Omega$ about the $\vec{e}$-axis. Then transform back to the laboratory frame.

$$
\psi (t) = \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {- \ii \Omega \vec{e} \cdot \op{\vec{J}} t} \psi (0) = \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {- \ii \Omega t \vec{R}  (\tilde{\theta} , 0) \cdot \op{\vec{J}}} \psi (0)
$$

>When $\omega \rightarrow 0(\nu \rightarrow 0)$, the adiabatic approximation is valid.
>
>$$
>\begin{align*}
>& \because \Omega \vec{R}  (\tilde{\theta} , 0) = b \vec{R} (\theta , 0)\\
>& \therefore \psi (t) = \e ^ {- \ii t b \vec{R} (\theta , 0) \cdot \op{\vec{J}}} \psi (0)
>\end{align*}
>$$
>
>The corresponding Hamiltonian is time-independent.
>
>$$
>h = b \vec{R} (\theta , 0) \cdot \op{\vec{J}}
>$$
>
><img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-15-Berry-phase/assets/adiabatic_approxmation.png" width="40%">


>When $\omega \gg 0(\nu \gg 0)$, the motion of the magnetic momentum is nutation.
>
><img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-15-Berry-phase/assets/quantum_trajectory_parameter.png" width="40%">
>
>$$
>\begin{align*}
>& \omega = 1 \\
>& b = 1 \\
>& \theta = \pi/6 \\
>& \theta _ \mu = \pi/2 \\
>& \Omega =  b \sqrt{1 + \frac{\omega}{b} (-2 \cos \theta + \frac{\omega}{b})} \\
>& \vec{\mu} (0) = (\mu _ 1 , \mu _ 2 , \mu _ 3) , \begin{cases} 
>\mu _ 1 = \sin \theta _ \mu \\
>\mu _ 2 = 0 \\ 
>\mu _ 3 = \cos \theta _ \mu \end{cases} \\
>& \vec{e} = \frac{(e _ 1 , e _ 2 , e _ 3)}{\sqrt{e ^ 2 _ 1 + e ^ 2 _ 2 + e ^ 2 _ 3}} , \begin{cases} 
>e _ 1 = \sin \theta  \\
>e _ 2 = 0  \\ 
>e _ 3 = \cos \theta - \frac{\omega}{b} \end{cases} \\
>& \vec{b} = \vec{e} \times \vec{\mu} \\
>& \vec{a} = \vec{b} \times \vec{e} \\
>& \vec{c} = \vec{\mu} - \vec{a} \\
>& \vec{x} ^ \prime = \vec{c} + \vec{a} \cos \Omega t + \vec{b} \sin \Omega t \\ 
>& \vec{x} = \begin{pmatrix}
>\cos \omega t & - \sin \omega t & 0\\
>\sin \omega t & \cos \omega t & 0\\
>0 & 0 & 0\\
>\end{pmatrix} \vec{x} ^ \prime\\ 
>\end{align*}
>$$
>
><img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-15-Berry-phase/assets/quantum_trajectory.png" width="100%">
>
>With classic limit, we can solve the average motion of magnetic momentum.
>
>$$
>\begin{align*}
>& h(t) = b \vec{R} (\theta , \omega t) \cdot \op{\vec{J}}\\
>& \vec{R} =(R _ 1 , R _ 2 , R _ 3),\begin{cases}
>R _ 1 = \sin \theta \cos \omega t \\
>R _ 2 = \sin \theta \sin \omega t \\
>R _ 3 = \cos \theta 
>\end{cases}\\
>& \dot{\avg{\op{\vec{J}}}} = \frac{\avg{[\op{\vec{J}} , h]}}{\ii \hbar} = \frac{\avg{[\op{\vec{J}} , b \vec{R} \cdot \op{\vec{J}}]}}{\ii \hbar} = b \vec{R} \times \op{\vec{J}} 
>\end{align*}
>$$
>
><img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-15-Berry-phase/assets/classical_trajectory.png" width="100%">
>
>Both of them are nutation, but there is a offset of the rotating axis.

### Cyclic solution

---

By definition the cyclic solutions with period $\tau$ are obtained by choosing the initial state vector $\psi (0)$ to be an non-stationary eigenvector of the evolution operator 

$$
U ^ \dagger (\tau) = \e ^ {-\ii \tau \omega \op{J} _ 3} \e ^ {-\ii \tau \Omega \vec{R} (\tilde{\theta},0) \cdot \op{\vec{J}}}
$$

The corresponding eigenvalue $\e ^ {- \ii \alpha _ \psi}$ is the total phase factor, for

$$
\psi (\tau) = U ^ \dagger (\tau) \psi (0) = \e ^ {- \ii \alpha _ \psi} \psi (0)
\label{evolution}
$$

This is quite easy if $\tau$ is chosen in a way that the initial state is eigenstate of both of the operators appearing in the evolution operator.

$$
\begin{align*}
& [ \e ^ {-\ii \tau \omega \op{J} _ 3} , \e ^ {-\ii \tau \Omega \vec{R} (\tilde{\theta},0) \cdot \op{\vec{J}}} ] \ket{\psi (0)} = 0 \\
& \begin{cases}\text{CLASS A: } \tau = \frac{2\pi}{\omega} = T\\
\text{CLASS B: } \tau = \frac{2\pi}{\Omega}  \end{cases}
\end{align*}
$$

>When $\tau = \frac{2 \pi}{\omega}$, the commutator equals zero.
>
>$$
>\begin{align*}
>& \quad [ \e ^ {-\ii \frac{2 \pi}{\omega} \omega \op{J} _ 3} , \e ^ {-\ii \frac{2 \pi}{\omega} \Omega \vec{R} (\tilde{\theta},0) \cdot \op{\vec{J}}} ] \ket{\psi (0)} \\
>& = \e ^ {-\ii 2 \pi \omega \op{J} _ 3} \e ^ {-\ii \frac{2 \pi}{\omega} \Omega \vec{R} (\tilde{\theta},0) \cdot \op{\vec{J}}} \ket{\psi (0)} - \e ^ {-\ii \frac{2 \pi}{\omega} \Omega \vec{R} (\tilde{\theta},0) \cdot \op{\vec{J}}} \e ^ {-\ii 2 \pi \omega \op{J} _ 3} \ket{\psi (0)} \\
>& = \e ^ {-\ii 2 \pi \omega \op{J} _ 3} \e ^ {-\ii \frac{2 \pi}{\omega} b \left( \left( \cos \theta - \frac{\omega}{b} \right) \op{J} _ 3 + \sin \theta \op{J} _ 1 \right)} \ket{\psi (0)} - \e ^ {-\ii \frac{2 \pi}{\omega} b \left( \left( \cos \theta - \frac{\omega}{b} \right) \op{J} _ 3 + \sin \theta \op{J} _ 1 \right)} \e ^ {-\ii 2 \pi \omega \op{J} _ 3} \ket{\psi (0)} \\
>& = \e ^ {-\ii \frac{2 \pi}{\omega} b \left( \cos \theta \op{J} _ 3 + \sin \theta \op{J} _ 1 \right)} \ket{\psi (0)} - \e ^ {-\ii \frac{2 \pi}{\omega} b \left( \cos \theta \op{J} _ 3 + \sin \theta \op{J} _ 1 \right)} \ket{\psi (0)} \\
>& = 0
>\end{align*}
>$$
>
>When $\tau = \frac{2 \pi}{\Omega}$, the commutator equals zero.
>
>$$
>\begin{align*}
>& \quad [ \e ^ {-\ii \frac{2 \pi}{\Omega} \omega \op{J} _ 3} , \e ^ {-\ii \frac{2 \pi}{\Omega} \Omega \vec{R} (\tilde{\theta},0) \cdot \op{\vec{J}}} ] \ket{\psi (0)} \\
>& = \e ^ {-\ii \frac{2 \pi}{\Omega} \omega \op{J} _ 3} \e ^ {-\ii 2 \pi \vec{R} (\tilde{\theta},0) \cdot \op{\vec{J}}} \ket{\psi (0)} - \e ^ {-\ii 2 \pi \vec{R} (\tilde{\theta},0) \cdot \op{\vec{J}}} \e ^ {-\ii \frac{2 \pi}{\Omega} \omega \op{J} _ 3} \ket{\psi (0)} \\
>& = \e ^ {-\ii \frac{2 \pi}{\Omega} \omega \op{J} _ 3} \e ^ {-\ii 2 \pi \frac{b}{\Omega} \left( \left( \cos \theta - \frac{\omega}{b} \right) \op{J} _ 3 + \sin \theta \op{J} _ 1 \right)} \ket{\psi (0)} - \e ^ {-\ii 2 \pi \frac{b}{\Omega} \left( \left( \cos \theta - \frac{\omega}{b} \right) \op{J} _ 3 + \sin \theta \op{J} _ 1 \right)} \e ^ {-\ii \frac{2 \pi}{\Omega} \omega \op{J} _ 3} \ket{\psi (0)} \\
>& = \e ^ {-\ii \frac{2 \pi}{\Omega} b \left( \cos \theta \op{J} _ 3 + \sin \theta \op{J} _ 1 \right)} \ket{\psi (0)} - \e ^ {-\ii \frac{2 \pi}{\Omega} b \left( \cos \theta \op{J} _ 3 + \sin \theta \op{J} _ 1 \right)} \ket{\psi (0)} \\
>& = 0
>\end{align*}
>$$
>

### Class A

---

The class A cyclic solutions are obtained by finding the simultaneous eigenvectors of the operators $\e ^ {- \ii 2 \pi \op{J} _ 3}$ $\e ^ {- \ii \frac{2 \pi}{\omega} \Omega \vec{R} (\tilde{\theta},0) \cdot \op{\vec{J}}}$. The initial eigenvector can be given as

$$
\ket{k , \tilde{\theta} , 0} = U (\tilde{\theta} , 0) \ket{k , \vec{e} _ 3} = \e ^ {- \ii \tilde{\theta} \op{J} _ 2} \ket{k , \vec{e} _ 3}
\label{initial_state}
$$

They are the eigenvector of $\e ^ {- \ii 2 \pi \op{J} _ 3}$ as follows.

$$
\begin{align*}
& \quad \ \e ^ {- \ii 2 \pi \op{J} _ 3} \ket{k , \tilde{\theta} , 0} \\
& = \e ^ {- \ii 2 \pi \op{J} _ 3} \e ^ {- \ii \tilde{\theta} \op{J} _ 2} \ket{k , 0 , 0}  \\
& = \e ^ {- \ii \tilde{\theta} \op{J} _ 2} \e ^ {- \ii 2 \pi \op{J} _ 3} \ket{k , 0 , 0}  \\
& = \e ^ {- \ii \tilde{\theta} \op{J} _ 2} \e ^ {- \ii 2 \pi k} \ket{k , 0 , 0}  \\
& = \e ^ {- \ii 2 \pi k} \ket{k , \tilde{\theta} , 0} \\
\end{align*}
$$

>The commutator $[\e ^ {- \ii \tilde{\theta} \op{J} _ 2} , \e ^ {- \ii 2 \pi \op{J} _ 3} ]$ equals $0$.
>
>$$
>\e ^ {- \ii \theta \op{J} _ 3} \op{J} _ 2 \e ^ {\ii \theta \op{J} _ 3} = \op{J} _ 2 \cos \theta - \op{J} _ 1 \sin \theta\\
>\e ^ {- \ii 2 \pi \op{J} _ 3} \op{J} _ 2 \e ^ {\ii 2 \pi \op{J} _ 3} = \op{J} _ 2 \cos 2 \pi - \op{J} _ 1 \sin 2 \pi\\
>\e ^ {- \ii 2 \pi \op{J} _ 3} \op{J} _ 2 \e ^ {\ii 2 \pi \op{J} _ 3} = \op{J} _ 2 \\
>\e ^ {- \ii 2 \pi \op{J} _ 3} \op{J} _ 2 = \op{J} _ 2 \e ^ {- \ii 2 \pi \op{J} _ 3} \\
>\e ^ {- \ii 2 \pi \op{J} _ 3} \e ^ {- \ii \tilde{\theta} \op{J} _ 2} = \e ^ {- \ii \tilde{\theta} \op{J} _ 2} \e ^ {- \ii 2 \pi \op{J} _ 3}
>$$
>

They are the eigenvector of $\e ^ {- \ii \frac{2 \pi}{\omega} \Omega \vec{R} (\tilde{\theta},0) \cdot \op{\vec{J}}}$ as follows.

$$
\begin{align*}
& \quad \ \e ^ {- \ii \frac{2 \pi}{\omega} \Omega \vec{R} (\tilde{\theta},0) \cdot \op{\vec{J}}} \ket{k , \tilde{\theta} , 0} \\
& = \e ^ {- \ii \frac{2 \pi}{\omega} \Omega k} \ket{k , \tilde{\theta} , 0} \\
\end{align*}
$$

Thus, the total phase of a period is $\alpha _ k = 2 \pi k (1 + \frac{\Omega}{\omega})$ as follows. 

$$
\begin{align*}
& \quad U ^ \dagger (T) \ket{k , \tilde{\theta} , 0} \\
& = \e ^ {-\ii 2 \pi \op{J} _ 3} \e ^ {-\ii \frac{2 \pi}{\omega} \Omega \vec{R} (\tilde{\theta},0) \cdot \op{\vec{J}}} \ket{k , \tilde{\theta} , 0} \\
& = \e ^ {-\ii 2 \pi k} \e ^ {-\ii \frac{2 \pi}{\omega} \Omega k} \ket{k , \tilde{\theta} , 0} \\
\end{align*}
$$


Namely, if the magnetic momentum is along the direction of magnetic field at first, it will follow magnetic field all the time.

<img src = "https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2018-11-15-Berry-phase/assets/cyclic_trajectory.png" width="100%">

The choice for evolutional state is

$$
U (\tilde {\theta} , \omega t) \ket{k , \vec{e} _ 3} = \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {- \ii \tilde{\theta} \op{J} _ 2} \e ^ {\ii \omega t k} \ket{k , \vec{e} _ 3} \isdefas \ket{k , \tilde{\theta} , \omega t}
$$

With Eqn. ($\ref{evolution}$) and ($\ref{initial_state}$), the cyclic solution is 

$$
\begin{align*}
\psi (t) & = \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {- \ii \Omega t \vec{R}  (\tilde{\theta} , 0) \cdot \op{\vec{J}}} \ket{k , \tilde{\theta} , 0}\\
& = \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {- \ii \Omega t \vec{R}  (\tilde{\theta} , 0) \cdot \op{\vec{J}}} \ket{k , \tilde{\theta} , \omega t}\\
& = \e ^ {- \ii \Omega t k} \e ^ {- \ii \omega t \op{J} _ 3} \ket{k , \tilde{\theta} , 0} \\
& = \e ^ {- \ii \Omega t k} \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {- \ii \tilde{\theta} \op{J} _ 2} \ket{k , 0 , 0}\\
& = \e ^ {- \ii \omega t k} \e ^ {- \ii \Omega t k} \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {- \ii \tilde{\theta} \op{J} _ 2}  \e ^ {\ii \omega t k} \ket{k , 0 , 0}\\
& = \e ^ {- \ii \omega t k} \e ^ {- \ii \Omega t k} \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {- \ii \tilde{\theta} \op{J} _ 2}  \e ^ {\ii \omega t \op{J} _ 3} \ket{k , 0 , 0}\\
& = \e ^ {- \ii \omega t k} \e ^ {- \ii \Omega t k} \ket{k , \tilde{\theta} , \omega t}\\
\end{align*}
$$


|                   |                          Adiabatic                           |                        Non-adiabatic                         |
| :---------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
|   Initial state   |                    $\ket{k , \theta , 0}$                    |                $\ket{k , \tilde{\theta} , 0}$                |
|     Operator      |          $\vec{R} (\theta , 0) \cdot \op{\vec{J}}$           |      $\vec{R} (\tilde{\theta} , 0) \cdot \op{\vec{J}}$       |
|    Total Phase    | $\e ^ {- \ii  2 \pi k \frac{b}{\omega}} \e ^ {\ii \gamma _ k (\mathbf{C} _ 1) }$ | $\e ^ {- \ii 2 \pi k} \e ^ {- \ii 2 \pi \frac{\omega}{\Omega} k}$ |
| Evolutional state | $\ket{k , \theta, \omega t} = \e ^ {-\ii \omega t \op{J} _ 3}  \e ^ {-\ii \theta \op{J} _ 2} \e ^ {\ii \omega t k} \ket{k , \vec{e} _ 3}$ | $\ket{k , \tilde{\theta} , \omega t} = \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {- \ii \tilde{\theta} \op{J} _ 2} \e ^ {\ii \omega t k} \ket{k , \vec{e} _ 3}$ |

## Dynamical and geometrical phase factors for non-adiabatic evolution

### The connection one-form

---

$$
\begin{align*}
A ^ k & \defas \ii \bra{\psi _ k} \dd \ket{\psi _ k} \\
& = \ii \bra{k , \tilde{\theta} , \omega t} \e ^ {\ii \Omega t k} \e ^ {\ii \omega t k} \dd \left(\e ^ {- \ii \omega t k} \e ^ {- \ii \Omega t k} \ket{k , \tilde{\theta} , \omega t}\right) \\ 
& = \ii \bra{k , \tilde{\theta} , \omega t} \e ^ {\ii \Omega t k} \e ^ {\ii \omega t k} \e ^ {- \ii \omega t k} \e ^ {- \ii \Omega t k} \dd \ket{k , \tilde{\theta} , \omega t} \\ 
& = \ii \bra{k , \tilde{\theta} , \omega t} \dd \ket{k , \tilde{\theta} , \omega t} \\
& = \ii \bra{k , \tilde{\theta} , \omega t} \frac{\partial}{\partial \tilde{\theta}} \ket{k , \tilde{\theta} , \omega t} \dd \tilde{\theta} + \ii \bra{k , \tilde{\theta} , \omega t} \frac{\partial}{\partial \varphi} \ket{k , \tilde{\theta} , \omega t} \dd \varphi \\
& = \ii \bra{k , \tilde{\theta} , \omega t} \frac{\partial}{\partial \tilde{\theta}} \ket{k , \tilde{\theta} , \omega t} \frac{\partial \tilde{\theta}}{\partial \theta} \dd \theta + \ii \bra{k , \tilde{\theta} , \omega t} \frac{\partial}{\partial \tilde{\varphi}} \ket{k , \tilde{\theta} , \omega t} \dd \varphi \\
& = A ^ k _ \tilde{\theta} (\tilde{\theta} , \varphi) \frac{\partial \tilde{\theta}}{\partial \theta} \dd \theta + A ^ k _ \varphi (\tilde{\theta} , \varphi) \dd \varphi \\
& = - k (1 - \cos \tilde{\theta}) \dd \varphi \\
& = - k (1 - \frac{b}{\Omega} \cos \theta + \frac{\omega}{\Omega}) \dd \varphi
\end{align*}
$$

where the components $A _ \tilde{\theta} ^ k (\tilde{\theta} , \varphi)$ and $A _ \varphi^ k (\tilde{\theta} , \varphi)$ are similar to the Eqn. ($\ref{connection}$).

$$
A _ \tilde{\theta} ^ k (\tilde{\theta} , \varphi) = 0 \\
A _ \varphi ^ k (\tilde{\theta} , \varphi) = - k (1 - \frac{b}{\Omega} \cos \theta + \frac{\omega}{\Omega})
$$

### The curvature two-form

---

$$
\begin{align*}
F ^ k & = \dd A ^ k \\
& = \frac{\partial A ^ k _ \theta}{\partial \varphi} \dd \varphi \wedge \dd \theta +  \frac{\partial A ^ k _ \varphi}{\partial \theta} \dd \theta \wedge \dd \varphi \\
& = 0 - k \left(\frac{b}{\Omega} \sin \theta + \frac{b}{\Omega ^ 2} \frac{\partial \Omega}{\partial \theta} \cos \theta - \frac{\omega}{\Omega ^ 2} \frac{\partial \Omega}{\partial \theta}\right) \dd \theta \wedge \dd \varphi \\
& = - k \left(\frac{b}{\Omega} \sin \theta + \frac{b}{\Omega ^ 2} \frac{\partial \Omega}{\partial \theta} \cos \theta - \frac{\omega}{\Omega ^ 2} \frac{\partial \Omega}{\partial \theta}\right) \dd \theta \wedge \dd \varphi \\
& = - k \left(\frac{b}{\Omega} \sin \theta + \frac{b}{\Omega ^ 2} \frac{b \omega \sin \theta}{\Omega} \cos \theta - \frac{\omega}{\Omega ^ 2} \frac{b \omega \sin \theta}{\Omega}\right) \dd \theta \wedge \dd \varphi \\
& = - k \sin \theta \frac{b ^ 2}{\Omega ^ 3}\left(b - \omega \cos \theta \right) \dd \theta \wedge \dd \varphi \\
& = - k \sin \theta \frac{1 - \frac{\omega}{b} \cos \theta }{\left(\frac{\Omega}{b}\right) ^ 3} \dd \theta \wedge \dd \varphi \\
& = - k \sin \theta \frac{1 - \frac{\omega}{b} \cos \theta }{\left(1 + \frac{\omega}{b} (-2 \cos \theta + \frac{\omega}{b})\right) ^ {\frac{3}{2}}} \dd \theta \wedge \dd \varphi \\
\end{align*}
$$

>$$
>\begin{align*}
>\Omega & =  b \sqrt{1 + \frac{\omega}{b} (-2 \cos \theta + \frac{\omega}{b})} \\
>\frac{\partial \Omega}{\partial \theta} & = \frac{\partial b \sqrt{1 + \frac{\omega}{b} (-2 \cos \theta + \frac{\omega}{b})}}{\partial \theta} \\
>& = \frac{2 \frac{\omega}{b} b \sin \theta }{2 \sqrt{1 + \frac{\omega}{b} (-2 \cos \theta + \frac{\omega}{b})}} \\
>& = \frac{\omega \sin \theta }{\sqrt{1 + \frac{\omega}{b} (-2 \cos \theta + \frac{\omega}{b})}} \\
>& = \frac{b \omega \sin \theta}{\Omega}
>\end{align*}
>$$
>

### three-vector potential and curvature three-vector

---

$$
\begin{align*}
\op{\vec{A}} ^ k & = \op{A} ^ k _ r \vec{e} _ r + \op{A} ^ k _ \theta \vec{e} _ \theta + \op{A} ^ k _ \varphi \vec{e} _ \varphi = A ^ k _ r \vec{e} _ r + \frac{1}{r} A ^ k _ \theta \vec{e} _ \theta + \frac{1}{r \sin \theta} A ^ k _ \varphi \vec{e} _ \varphi = - \frac{k (1 - \frac{b}{\Omega} \cos \theta + \frac{\omega}{\Omega})}{r \sin \theta} \vec{e} _ \varphi \ ,\ \theta \ne \pi 
 \end{align*}
$$

$$
\begin{align*}
\vec{F} ^ k & = \nabla \times \op{\vec{A}} ^ k \\
& = \frac{1}{r \sin \theta} \left( \frac{\partial}{\partial \theta} ( \op{A} _ \varphi \sin \theta ) \right) \vec{e} _ r + \frac{1}{r} \left( - \frac{\partial}{\partial r} (r \op{A} _ \varphi) \right) \vec{e} _ \theta\\
& = \frac{1}{r \sin \theta} \left( \frac{\partial}{\partial \theta} ( - \frac{k (1 - \frac{b}{\Omega} \cos \theta + \frac{\omega}{\Omega})}{r \sin \theta} \sin \theta ) \right) \vec{e} _ r + \frac{1}{r} \left( - \frac{\partial}{\partial r} (- r \frac{k (1 - \frac{b}{\Omega} \cos \theta + \frac{\omega}{\Omega})}{r \sin \theta}) \right) \vec{e} _ \theta\\
& = \frac{1}{r \sin \theta} \left( \frac{\partial}{\partial \theta} ( - \frac{k (1 - \frac{b}{\Omega} \cos \theta + \frac{\omega}{\Omega})}{r}) \right) \vec{e} _ r + \frac{1}{r} \left(\frac{\partial}{\partial r} (\frac{k (1 - \frac{b}{\Omega} \cos \theta + \frac{\omega}{\Omega})}{\sin \theta}) \right) \vec{e} _ \theta\\
& = \frac{1}{r \sin \theta} \left( \frac{\partial}{\partial \theta} ( - \frac{k (1 - \frac{b}{\Omega} \cos \theta + \frac{\omega}{\Omega})}{r}) \right) \vec{e} _ r \\
& = -\frac{1}{r ^ 2 \sin \theta} k \sin \theta \frac{1 - \frac{\omega}{b} \cos \theta }{\left(1 + \frac{\omega}{b} (-2 \cos \theta + \frac{\omega}{b})\right) ^ {\frac{3}{2}}} \vec{e} _ r \\
& = -\frac{k}{r ^ 2} \frac{1 - \frac{\omega}{b} \cos \theta }{\left(1 + \frac{\omega}{b} (-2 \cos \theta + \frac{\omega}{b})\right) ^ {\frac{3}{2}}} \vec{e} _ r \\
& = -\frac{k}{r ^ 2} \frac{1 - \frac{\omega}{b} \cos \theta }{\left(\frac{\Omega}{b} \right) ^ {\frac{3}{2}}} \vec{e} _ r \\
\end{align*}
$$

### Berry phase

---

$$
\begin{align*}
\gamma _ k (\mathbf{C}) & \defas \int _ \mathbf{C} A ^ k \\
& = \int _ \mathbf{C} - k (1 - \cos \tilde{\theta}) \dd \varphi \\
& = \int _ \mathbf{C} - k (1 - \cos \tilde{\theta}) \omega \dd t \\
\end{align*}
$$

$$
\begin{align*}
\gamma _ k (T) & = \int ^ T _ 0 - k (1 - \cos \tilde{\theta}) \omega \dd t \\
& = - 2 \pi k (1 - \cos \tilde{\theta})\\
& = - 2 \pi k (1 - \cos \tilde{\theta})\\
& = - 2 \pi k (1 - \frac{b}{\Omega} \cos \theta + \frac{\omega}{\Omega})
\end{align*}
$$

### Dynamical phase

---

The dynamic phase for general cyclic evolution is

$$
\begin{align*}
h (\vec{R} (\theta , \omega t)) & = b \vec{R} (\theta , \omega t) \cdot \op{\vec{J}} \\
\ket {\psi (t)} & = \e ^ {- \ii \omega t k} \e ^ {- \ii \Omega t k} \ket{k , \tilde{\theta} , \omega t} = \e ^ {- \ii \Omega t k} \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {- \ii \tilde{\theta} \op{J} _ 2} \ket{k , \vec{e} _ 3} \\
\alpha ^ \text{dyn} _ k & = \int ^ T _ 0 \bra{\psi (t)} h (t) \ket{\psi (t)} \dd t \\
& = \int ^ T _ 0 \bra{k , \tilde{\theta} , \omega t} \e ^ {\ii \Omega t k} \e ^ {\ii \omega t k} b (\vec{R} (\theta , \omega t) \cdot \op{\vec{J}}) \e ^ {- \ii \omega t k} \e ^ {- \ii \Omega t k} \ket{k , \tilde{\theta} , \omega t} \dd t \\ 
& = \int ^ T _ 0 \bra{k , \tilde{\theta} , \omega t} b (\vec{R} (\theta , \omega t) \cdot \op{\vec{J}}) \ket{k , \tilde{\theta} , \omega t} \dd t \\
& = \int ^ T _ 0 \bra{k , \tilde{\theta} , \omega t} b \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {- \ii \theta \op{J} _ 2} \e ^ {\ii \tilde{\theta} \op{J} _ 2} \e ^ {\ii \omega t \op{J} _ 3} \vec{R} (\tilde{\theta} , \omega t) \cdot \op{\vec{J}} \ket{k , \tilde{\theta} , \omega t} \dd t \\
& = \int ^ T _ 0 \bra{k , \tilde{\theta} , \omega t} b \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {- \ii \theta \op{J} _ 2} \e ^ {\ii \tilde{\theta} \op{J} _ 2} \e ^ {\ii \omega t \op{J} _ 3} k \ket{k , \tilde{\theta} , \omega t} \dd t \\
& = \int ^ T _ 0 \bra{k , \vec{e} _ 3} b k \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {\ii \tilde{\theta} \op{J} _ 2} \e ^ {\ii \omega t \op{J} _ 3}\e ^ {- \ii \omega t \op{J} _ 3} \e ^ {- \ii \theta \op{J} _ 2} \e ^ {\ii \tilde{\theta} \op{J} _ 2} \e ^ {\ii \omega t \op{J} _ 3} k \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {- \ii \tilde{\theta} \op{J} _ 2} \e ^ {\ii \omega t \op{J} _ 3} \ket{k , \vec{e} _ 3} \dd t \\
& = \int ^ T _ 0 \bra{k , \vec{e} _ 3} b k \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {\ii \tilde{\theta} \op{J} _ 2}  \e ^ {- \ii \theta \op{J} _ 2} \e ^ {\ii \omega t \op{J} _ 3} \ket{k , \vec{e} _ 3} \dd t \\
& = \int ^ T _ 0 \bra{k , \vec{e} _ 3} b k \e ^ {- \ii \omega t k} \e ^ {\ii \tilde{\theta} \op{J} _ 2}  \e ^ {- \ii \theta \op{J} _ 2} \e ^ {\ii \omega t k} \ket{k , \vec{e} _ 3} \dd t \\
& = \int ^ T _ 0 \bra{k , \vec{e} _ 3} b k \e ^ {\ii \tilde{\theta} \op{J} _ 2}  \e ^ {- \ii \theta \op{J} _ 2} \ket{k , \vec{e} _ 3} \dd t \\
& = \bra{k , \vec{e} _ 3} b k \e ^ {\ii \tilde{\theta} \op{J} _ 2}  \e ^ {- \ii \theta \op{J} _ 2} \ket{k , \vec{e} _ 3}
\end{align*}
$$

$$
\begin{align*}
\vec{R} (\theta , \omega t) & = \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {- \ii \theta \op{J} _ 2} \e ^ {\ii \omega t \op{J} _ 3} \vec{e} _ 3\\
\vec{R} (\tilde{\theta} , \omega t) & = \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {- \ii \tilde{\theta} \op{J} _ 2} \e ^ {\ii \omega t \op{J} _ 3} \vec{e} _ 3\\
\vec{R} (\theta , \omega t) & = \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {- \ii \theta \op{J} _ 2} \e ^ {\ii \omega t \op{J} _ 3} \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {\ii \tilde{\theta} \op{J} _ 2} \e ^ {\ii \omega t \op{J} _ 3} \vec{R} (\tilde{\theta} , \omega t) \\
& = \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {- \ii \theta \op{J} _ 2} \e ^ {\ii \tilde{\theta} \op{J} _ 2} \e ^ {\ii \omega t \op{J} _ 3} \vec{R} (\tilde{\theta} , \omega t) \\
\end{align*}
$$

to-do list:

- [x] $\vec{R} ( \theta , \varphi )\cdot \op{\vec{J}} \ket{k,\theta, \varphi } = k \ket{k,\theta, \varphi }$: the direction of magnetic field is always the direction of measurement. The value of measurement is always be integer or half-integer.
- [x] plot $\psi (t) = \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {- \ii \Omega \vec{e} \cdot \op{\vec{J}} t} \psi (0) = \e ^ {- \ii \omega t \op{J} _ 3} \e ^ {- \ii \Omega t \vec{R}  (\tilde{\theta} , 0) \cdot \op{\vec{J}}} \psi (0)$
- [ ] calculate $\alpha ^ \text{dyn} _ k$

## References

[1] Bohm, Arno, et al. *The Geometric Phase in Quantum Systems: Foundations, Mathematical Concepts, and Applications in Molecular and Condensed Matter Physics*. Springer Science & Business Media, 2013.