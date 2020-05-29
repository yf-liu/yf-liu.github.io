---
title: An application of CAR algebra
category: Physics
tags:
  - Quantum Theory
---



## Preparation

From https://arxiv.org/pdf/1906.07309.pdf, in terms of the standard generators of $M _ {2^L}$, we have

$$
\begin{align}
a_i^*a_i &=\sum_{n=0}^{2^L-1} E_{n,n} \delta_{\mathfrak b_{n}(i),1} 
\end{align}
$$

where $E _ {n,n} $ is the $2^L\times2^L$ matrix with entry 1 at position $(n,n)$ and 0 in rest and $\mathfrak b _ {n}(i)$ is the $i$-th digit of binary form of the number $n$. The above equation basically says that the $a_i^\star a_i$ is represented by a selected set of matrices. For $M$-particle sector, we have:

$$
\begin{align}
(a_i^*a_i)_M
&=\sum_{n=0}^{2^L-1} \delta_{\mathcal{N}(n),M}\delta_{\mathfrak b_{n}(i),1}E_{n,n}  \\
(n_in_j)_M&=\sum_{n=0}^{2^L-1}\delta_{\mathcal{N}(n),M}\delta_{\mathfrak b_{n}(i),1}\delta_{\mathfrak b_{n}(j),1}E_{n,n}
\end{align}
$$

With these, we could construct interaction Hamiltonian $H_I$.

## M=1 with CBC

### Analytical calculation

The eigenvectors for M=1 could be indexed as follows.

| Eigenvectors      | Indices($n$) |
| ----------------- | ------------ |
| $(0,0,...,0,0,1)$ | $1=2^0$      |
| $(0,0,...,0,1,0)$ | $2=2^1$      |
| ...               | ...          |
| $(1,0,...,0,0,0)$ | $2^{L-1}$    |

The Hamiltonian of interaction is 

$$
\begin{align*}
H_I&=J_z\sum_{i=0}^{L-1}\left(a_i^*a_i-\frac{1}{2}\right)\left(a_{i+1}^*a_{i+1}-\frac{1}{2}\right)\\
&=J_z\sum_{i=0}^{L-1}\left(\sum_{n=0}^{2^L-1} E_{n,n} \left(\delta_{\mathfrak b_{n}(i),1} -\frac{1}{2}\right)\right)\left(\sum_{m=0}^{2^L-1} E_{m,m}\left(\delta_{\mathfrak b_{m}(i+1),1} -\frac{1}{2}\right)\right)\\
&=J_z\sum_{n,m=0}^{2^L-1} E_{n,n}E_{m,m} \sum_{i=0}^{L-1}\left(\delta_{\mathfrak b_{n}(i),1} -\frac{1}{2}\right) \left(\delta_{\mathfrak b_{m}(i+1),1} -\frac{1}{2}\right)\\
&=J_z\sum_{n=0}^{2^L-1} E_{n,n} \sum_{i=0}^{L-1}\left(\delta_{\mathfrak b_{n}(i),1} -\frac{1}{2}\right) \left(\delta_{\mathfrak b_{n}(i+1),1} -\frac{1}{2}\right)\\
\end{align*}
$$

where $L$ is the length of the 1-D chain.

Then we could generate the Hamiltonian $H^{(M=1)} _ I$ for one particle sector. Only one digit in the binary form of every index $n$ is $1$. 

$$
\begin{align*}
H^{(M=1)}_I&=J_z\sum_{k=0}^{L-1} E_{2^k,2^k} \sum_{i=0}^{L-1}\left(\delta_{\mathfrak b_{2^k}(i),1} -\frac{1}{2}\right) \left(\delta_{\mathfrak b_{2^k}(i+1),1} -\frac{1}{2}\right)\\
&=J_z\sum_{k=0}^{L-1} E_{2^k,2^k} \sum_{i=0}^{L-1}\left(\delta_{k,i} -\frac{1}{2}\right) \left(\delta_{k,i+1} -\frac{1}{2}\right)\\
&=J_z\sum_{k=0}^{L-1} E_{2^k,2^k} \sum_{i=0}^{L-1}\left(\delta_{k,i} \delta_{k,i+1} -\frac{1}{2}\delta_{k,i+1}-\delta_{k,i} \frac{1}{2} +\frac{1}{4} \right) \\
&=J_z\sum_{k=0}^{L-1} E_{2^k,2^k} \left(\sum_{i=0}^{L-1}-\frac{1}{2}\delta_{k,i+1}-\sum_{i=0}^{L-1}\delta_{k,i} \frac{1}{2} +\sum_{i=0}^{L-1}\frac{1}{4} \right) \\
&=J_z\sum_{k=0}^{L-1} E_{2^k,2^k} \left(-\frac{1}{2}-\frac{1}{2} +\frac{L}{4} \right) \\
&=J_z\frac{L-4}{4}\sum_{k=0}^{L-1} E_{2^k,2^k}
\end{align*}
$$

We could shrink it into an equivalent $L\times L$ matrix. So the whole eigensystem is,

| Eigenvectors      | Eigenvalues        | Degeneracies | Sketch                                                       |
| ----------------- | ------------------ | ------------ | ------------------------------------------------------------ |
| $(0,0,...,0,0,1)$ | $\frac{L-4}{4}J_z$ | $L$          | <img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/11.png" style="zoom:40%;" /> |
| ...               | ...                | ...          |                                                              |



### Numerical calculation

Here is the numerical calculation the spectrum of $H_I^{(M=1)}$ with length of chain $L=100$ and $J_z=100$. As expected, eigenvalue is $\frac{L-4}{4}J_z=2400$ and degeneracy is $L=100$.

<img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/E1.png" style="zoom:60%;" />

## M=2 with CBC

### Analytical calculation

The eigenvectors for M=2 could be indexed as follows.

| Eigenvectors          | Indices($n$)      |
| --------------------- | ----------------- |
| $(0,0,0,...,0,0,1,1)$ | $3=2^0+2^1$       |
| $(0,0,0,...,0,1,0,1)$ | $5=2^0+2^2$       |
| ...                   | ...               |
| $(1,1,0,...,0,0,0,0)$ | $2^{L-1}+2^{L-2}$ |



The Hamiltonian is

$$
\begin{align*}
H_I&=J_z\sum_{i=0}^{L-1}\left(a_i^*a_i-\frac{1}{2}\right)\left(a_{i+1}^*a_{i+1}-\frac{1}{2}\right)\\
&=J_z \sum_{i=0}^{L-1} \left((n_in_{i+1})_M-\frac{1}{2}(a_i^*a_i)_M-\frac{1}{2}(a_{i+1}^*a_{i+1})_M+\frac{1}{4}\right)\\
&=J_z \sum_{n=0}^{2^L-1}E_{n,n}\sum_{i=0}^{L-1}\left(\left(\delta_{\mathcal{N}(n),M}\delta_{\mathfrak b_{n}(i),1}\delta_{\mathfrak b_{n}(i+1),1}-\frac{1}{2}\delta_{\mathcal{N}(n),M}\delta_{\mathfrak b_{n}(i),1}
-\frac{1}{2}\delta_{\mathcal{N}(n),M}\delta_{\mathfrak b_{n}(i+1),1}\right)+\frac{L}{4}\right)\\
&=J_z \sum_{n=0}^{2^L-1}E_{n,n}\sum_{i=0}^{L-1}\left(\delta_{\mathcal{N}(n),M}\left(\delta_{\mathfrak b_{n}(i),1}\delta_{\mathfrak b_{n}(i+1),1}-\frac{1}{2}\delta_{\mathfrak b_{n}(i),1}
-\frac{1}{2}\delta_{\mathfrak b_{n}(i+1),1}\right)+\frac{L}{4}\right)\\
\end{align*}
$$

Consider $M=2$,

$$
\begin{align*}
& \ H_I^{(M=2)}\\&=J_z \sum_{n=0}^{2^L-1}E_{n,n}\left(\sum_{i=0}^{L-1}\delta_{\mathcal{N}(n),2}\left(\delta_{\mathfrak b_{n}(i),1}\delta_{\mathfrak b_{n}(i+1),1}-\frac{1}{2}\delta_{\mathfrak b_{n}(i),1}
-\frac{1}{2}\delta_{\mathfrak b_{n}(i+1),1}\right)+\frac{L}{4}\right)\\
&=J_z \sum_{k=0}^{L-1}\sum_{l>k}^{L-1}E_{2^k+2^l,2^k+2^l}\left(\sum_{i=0}^{L-1}\left(\delta_{\mathfrak b_{2^k+2^l}(i),1}\delta_{\mathfrak b_{2^k+2^l}(i+1),1}-\frac{1}{2}\delta_{\mathfrak b_{2^k+2^l}(i),1}
-\frac{1}{2}\delta_{\mathfrak b_{2^k+2^l}(i+1),1}\right)+\frac{L}{4}\right)\\
&=J_z \sum_{k=0}^{L-1}\sum_{l>k}^{L-1}E_{2^k+2^l,2^k+2^l}\left(\sum_{i=0}^{L-1}\left((\delta_{k,i}+\delta_{l,i})(\delta_{k,i+1}+\delta_{l,i+1})-\frac{1}{2}(\delta_{k,i}+\delta_{l,i})
-\frac{1}{2}(\delta_{k,i+1}+\delta_{l,i+1})\right)+\frac{L}{4}\right)\\
&=J_z \sum_{k=0}^{L-1}\sum_{l>k}^{L-1}E_{2^k+2^l,2^k+2^l}\left(\sum_{i=0}^{L-1}\left(\delta_{k,i}\delta_{l,i+1}+\delta_{l,i}\delta_{k,i+1}-\frac{1}{2}\delta_{k,i}-\frac{1}{2}\delta_{l,i}
-\frac{1}{2}\delta_{k,i+1}-\frac{1}{2}\delta_{l,i+1}\right)+\frac{L}{4}\right)\\
&=J_z \left(\frac{L-4}{4}\sum_{(k,l)\in\set{(k,l)|\text{case1}}}^{L-1}E_{2^k+2^{k+1},2^k+2^{k+1}}+\frac{L-8}{4}\sum_{(k,l)\in\set{(k,l)|\neg(\text{case1})}}^{L-1}E_{2^k+2^l,2^k+2^l}\right)\\
\end{align*}
$$

where

$$
\begin{align*}
&\text{case1:}\ k+1=l \text{ or } k=0,l=L-1\\
&\ \sum_{i=0}^{L-1}\left(\delta_{k,i}\delta_{l,i+1}+\delta_{l,i}\delta_{k,i+1}-\frac{1}{2}\delta_{k,i}-\frac{1}{2}\delta_{l,i}
-\frac{1}{2}\delta_{k,i+1}-\frac{1}{2}\delta_{l,i+1}\right)=-1\\
&\neg(\text{case1:})\\
&\ \sum_{i=0}^{L-1}\left(\delta_{k,i}\delta_{l,i+1}+\delta_{l,i}\delta_{k,i+1}-\frac{1}{2}\delta_{k,i}-\frac{1}{2}\delta_{l,i}
-\frac{1}{2}\delta_{k,i+1}-\frac{1}{2}\delta_{l,i+1}\right)=-2\\
\end{align*}
$$


We could shrink it into an equivalent $\left(\begin{matrix}L\newline 2\end{matrix}\right)\times\left(\begin{matrix}L\newline 2\end{matrix}\right)$ matrix. So the whole eigensystem is,

| Eigenvectors        | Eigenvalues        | Degeneracies                                           | Sketch                                                       |
| ------------------- | ------------------ | ------------------------------------------------------ | ------------------------------------------------------------ |
| (0,0,0,...,0,0,1,1) | $\frac{L-4}{4}J_z$ | $L$                                                    | <img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/21.png" style="zoom:40%;" /> |
| ...                 | ...                | ...                                                    | ...                                                          |
| (0,0,0,...0,1,0,1)  | $\frac{L-8}{4}J_z$ | $\left(\begin{matrix}L\newline 2\end{matrix}\right)-L$ | <img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/22.png" style="zoom:40%;" /> |
| ...                 | ...                | ...                                                    | ...                                                          |
### Numerical calculation

Here is the numerical calculation the spectrum of $H_I^{(M=2)}$ with length of chain $L=60$ and $J_z=100$. As expected, eigenvalues are $\frac{L-4}{4}J_z=1300$, and $\frac{L-8}{4}J_z=1400$ and corresponding degeneracies are $L=60$ and $\left(\begin{matrix}L\\2\end{matrix}\right)-L=1710$.

<img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/E2.png" style="zoom:60%;" />

## M=3 with CBC

### Analytical calculation

The eigenvectors for M=3 could be indexed as follows.

| Eigenvectors          | Indices($n$)              |
| --------------------- | ------------------------- |
| $(0,0,0,...,0,1,1,1)$ | $3=2^0+2^1+2^2$           |
| $(0,0,0,...,1,1,0,1)$ | $5=2^0+2^2+2^3$           |
| ...                   | ...                       |
| $(1,1,1,...,0,0,0,0)$ | $2^{L-3}+2^{L-2}+2^{L-1}$ |

The Hamiltonian for M=3 is,

$$
\begin{align*}
& \ H_I^{(M=3)}\\
&=J_z \sum_{n=0}^{2^L-1}E_{n,n}\left(\sum_{i=0}^{L-1}\delta_{\mathcal{N}(n),3}\left(\delta_{\mathfrak b_{n}(i),1}\delta_{\mathfrak b_{n}(i+1),1}-\frac{1}{2}\delta_{\mathfrak b_{n}(i),1}-\frac{1}{2}\delta_{\mathfrak b_{n}(i+1),1}\right)+\frac{L}{4}\right)\\
&=J_z \sum_{k=0}^{L-3}\sum_{l>k}^{L-2}\sum_{m>l}^{L-1} E_{2^k+2^l+2^m,2^k+2^l+2^m}\left(\sum_{i=0}^{L-1}\left(\delta_{\mathfrak b_{2^k+2^l+2^m}(i),1}\delta_{\mathfrak b_{2^k+2^l+2^m}(i+1),1}-\frac{1}{2}\delta_{\mathfrak b_{2^k+2^l+2^m}(i),1}\\
-\frac{1}{2}\delta_{\mathfrak b_{2^k+2^l+2^m}(i+1),1}\right)+\frac{L}{4}\right)\\
&=J_z \sum_{k=0}^{L-3}\sum_{l>k}^{L-2}\sum_{m>l}^{L-1} E_{2^k+2^l+2^m,2^k+2^l+2^m}\left(\sum_{i=0}^{L-1}\left((\delta_{k,i}+\delta_{l,i}+\delta_{m,i})(\delta_{k,i+1}+\delta_{l,i+1}+\delta_{m,i+1})\\
-\frac{1}{2}(\delta_{k,i}+\delta_{l,i}+\delta_{m,i})-\frac{1}{2}(\delta_{k,i+1}+\delta_{l,i+1}+\delta_{m,i+1})\right)+\frac{L}{4}\right)\\
&=J_z \sum_{k=0}^{L-3}\sum_{l>k}^{L-2}\sum_{m>l}^{L-1} E_{2^k+2^l+2^m,2^k+2^l+2^m}\left(\sum_{i=0}^{L-1}\left(\delta_{k,i}\delta_{l,i+1}+\delta_{m,i}\delta_{k,i+1}+\delta_{l,i}\delta_{m,i+1}\\
-\frac{1}{2}\delta_{k,i}-\frac{1}{2}\delta_{l,i}-\frac{1}{2}\delta_{m,i}-\frac{1}{2}\delta_{k,i+1}-\frac{1}{2}\delta_{l,i+1}-\frac{1}{2}\delta_{m,i+1}\right)+\frac{L}{4}\right)\\
&=J_z \left(\frac{L-4}{4}\sum_{(k,l,m)\in\set{(k,l,m)|\text{case1}}}^{L-1}E_{2^k+2^l+2^m,2^k+2^l+2^m}+\frac{L-8}{4}\sum_{(k,l,m)\in\set{(k,l,m)|\text{case2,3,4}}}^{L-1}E_{2^k+2^l+2^m,2^k+2^l+2^m}\\
+\frac{L-12}{4}\sum_{(k,l,m)\in\set{(k,l,m)|\text{case5}}}^{L-1}E_{2^k+2^l+2^m,2^k+2^l+2^m}\right)\\
\end{align*}
$$

where "case#" means 

$$
\begin{align*}
&\text{case1:}\ k+2=l+1=m\\
&\sum_{i=0}^{L-1}\left(\delta_{k,i}\delta_{l,i+1}+\delta_{m,i}\delta_{k,i+1}+\delta_{l,i}\delta_{m,i+1}-\frac{1}{2}\delta_{k,i}-\frac{1}{2}\delta_{l,i}-\frac{1}{2}\delta_{m,i}-\frac{1}{2}\delta_{k,i+1}-\frac{1}{2}\delta_{l,i+1}-\frac{1}{2}\delta_{m,i+1}\right)=-1\\
&\text{case2:}\ k+2=l+1<m\\
&\sum_{i=0}^{L-1}\left(\delta_{k,i}\delta_{l,i+1}+\delta_{m,i}\delta_{k,i+1}+\delta_{l,i}\delta_{m,i+1}-\frac{1}{2}\delta_{k,i}-\frac{1}{2}\delta_{l,i}-\frac{1}{2}\delta_{m,i}-\frac{1}{2}\delta_{k,i+1}-\frac{1}{2}\delta_{l,i+1}-\frac{1}{2}\delta_{m,i+1}\right)=-2\\
&\text{case3:}\ k+2<l+1=m\\
&\sum_{i=0}^{L-1}\left(\delta_{k,i}\delta_{l,i+1}+\delta_{m,i}\delta_{k,i+1}+\delta_{l,i}\delta_{m,i+1}-\frac{1}{2}\delta_{k,i}-\frac{1}{2}\delta_{l,i}-\frac{1}{2}\delta_{m,i}-\frac{1}{2}\delta_{k,i+1}-\frac{1}{2}\delta_{l,i+1}-\frac{1}{2}\delta_{m,i+1}\right)=-2\\
&\text{case4:}\ k+2=2<l+1<m=L-1\\
&\sum_{i=0}^{L-1}\left(\delta_{k,i}\delta_{l,i+1}+\delta_{m,i}\delta_{k,i+1}+\delta_{l,i}\delta_{m,i+1}-\frac{1}{2}\delta_{k,i}-\frac{1}{2}\delta_{l,i}-\frac{1}{2}\delta_{m,i}-\frac{1}{2}\delta_{k,i+1}-\frac{1}{2}\delta_{l,i+1}-\frac{1}{2}\delta_{m,i+1}\right)=-2\\
&\text{case5:}\neg\text{(case1 or case2 or case3 or case4)}\\
&\sum_{i=0}^{L-1}\left(\delta_{k,i}\delta_{l,i+1}+\delta_{m,i}\delta_{k,i+1}+\delta_{l,i}\delta_{m,i+1}-\frac{1}{2}\delta_{k,i}-\frac{1}{2}\delta_{l,i}-\frac{1}{2}\delta_{m,i}-\frac{1}{2}\delta_{k,i+1}-\frac{1}{2}\delta_{l,i+1}-\frac{1}{2}\delta_{m,i+1}\right)=-3\\
\end{align*}
$$

We could shrink it into an equivalent $\left(\begin{matrix}L\\3\end{matrix}\right)\times \left(\begin{matrix}L\\3\end{matrix}\right)$ matrix. So the whole eigensystem is,

| Eigenvectors        | Eigenvalues         | Degeneracies                                                | Sketch                                                       |
| ------------------- | ------------------- | ----------------------------------------------------------- | ------------------------------------------------------------ |
| (0,0,0,...,0,1,1,1) | $\frac{L-4}{4}J_z$  | $L$                                                         | <img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/31.png" style="zoom:40%;" /> |
| ...                 | ...                 | ...                                                         | ...                                                          |
| (0,0,0,...,1,0,1,1) | $\frac{L-8}{4}J_z$  | $L(L-4)$                                                    | <img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/32.png" style="zoom:40%;" /> |
| ...                 | ...                 | ...                                                         | ...                                                          |
| (1,0,1,...,0,0,1,0) | $\frac{L-12}{4}J_z$ | $\left(\begin{matrix}L\newline 3\end{matrix}\right)-L^2+3L$ | <img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/33.png" style="zoom:40%;" /> |



>How to calculate the degeneracy of case3?
>
>Suppose the numbers of sites between the three upspins are $x,y,z$.
>$$
>x+y+z=L-3\\
>x,y,z>0
>$$
>It's like to insert cards between $L-3$ balls. There are $L-4$ options for the first card and $L-5$ options for the second card. We overcount them twice so the total choices of these two cards are $\frac{(L-4)(L-5)}{2}$. Then we pick one upspin and put it at any of $L$ sites and the whole configuration is determined, but we overcount them third times because any of it could be the first upspin. So the final result is $\frac{(L-4)(L-5)}{2}\frac{L}{3}$.

The sum of three degeneracies is $\left(\begin{matrix}L\newline 3\end{matrix}\right)$.

### Numerical calculation

Here is the numerical calculation the spectrum of $H_I^{(M=3)}$ with length of chain $L=30$ and $J_z=100$. As expected, eigenvalues are $\frac{L-4}{4}J_z=650$, $\frac{L-8}{4}J_z=550$ and $\frac{L-12}{4}J_z=450$ and corresponding degeneracies are $L=30$, $L(L-4)=780$ and $\left(\begin{matrix}L\newline  3\end{matrix}\right)-L^2+3L=3250$.

<img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/E3.png" style="zoom:60%;" />

## M=1 with OBC

### Analytical calculation

$$
\begin{align*}
H^{(M=1)}_I&=J_z\sum_{k=0}^{L-1} E_{2^k,2^k} \sum_{i=0}^{L-2}\left(\delta_{\mathfrak b_{2^k}(i),1} -\frac{1}{2}\right) \left(\delta_{\mathfrak b_{2^k}(i+1),1} -\frac{1}{2}\right)\\
&=J_z\sum_{k=0}^{L-1} E_{2^k,2^k} \sum_{i=0}^{L-2}\left(\delta_{k,i} -\frac{1}{2}\right) \left(\delta_{k,i+1} -\frac{1}{2}\right)\\
&=J_z\sum_{k=0}^{L-1} E_{2^k,2^k} \sum_{i=0}^{L-2}\left( -\frac{1}{2}\delta_{k,i+1}- \frac{1}{2}\delta_{k,i} +\frac{1}{4} \right) \\
&=J_z\left(\frac{L-2}{4}E_{1,1}+\sum_{k(\text{case2})}^{L-1}\frac{L-4}{4} E_{2^k,2^k}\right)
\end{align*}
$$

$$
\begin{align*}
&\text{case1:} \ k=0,L-1\\
&\sum_{i=0}^{L-2}\left( -\frac{1}{2}\delta_{k,i+1}-\delta_{k,i} \frac{1}{2} +\frac{1}{4} \right)=\frac{L-3}{4}\\
&\text{case2:}\ \neg(\text{case1})\\
&\sum_{i=0}^{L-2}\left(-\frac{1}{2}\delta_{k,i+1}-\delta_{k,i} \frac{1}{2} +\frac{1}{4} \right)=\frac{L-5}{4}\\
\end{align*}
$$

| Eigenvectors          | Eigenvalues        | Degeneracies | Sketch                                                       |
| --------------------- | ------------------ | ------------ | ------------------------------------------------------------ |
| $(0,0,...,0,0,1)$     | $\frac{L-3}{4}J_z$ | $2$          | <img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/11o1.png" style="zoom:40%;" /> |
| ...                   | ...                | ...          | ...                                                          |
| $(0,...,0,1,0,...,0)$ | $\frac{L-5}{4}J_z$ | $L-1$        | <img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/11o.png" style="zoom:40%;" /> |
| ...                   | ...                | ...          | ...                                                          |

### Numerical calculation

L=200

Jz=100

<img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/M1o.png" style="zoom:40%;" />

## M=2 with OBC

### Analytical calculation

$$
\begin{align*}
H_I
&=J_z \sum_{n=0}^{2^L-1}E_{n,n}\left(\sum_{i=0}^{L-2}\delta_{\mathcal{N}(n),2}\left(\delta_{\mathfrak b_{n}(i),1}\delta_{\mathfrak b_{n}(i+1),1}-\frac{1}{2}\delta_{\mathfrak b_{n}(i),1}
-\frac{1}{2}\delta_{\mathfrak b_{n}(i+1),1}\right)+\frac{L-1}{4}\right)\\
&=J_z \sum_{k=0}^{L-2}\sum_{l>k}^{L-1}E_{2^k+2^l,2^k+2^l}\left(\sum_{i=0}^{L-2}\left(\delta_{k,i}\delta_{l,i+1}-\frac{1}{2}\delta_{k,i}-\frac{1}{2}\delta_{l,i}
-\frac{1}{2}\delta_{k,i+1}-\frac{1}{2}\delta_{l,i+1}\right)+\frac{L-1}{4}\right)\\
&=J_z \left(\sum_{k,l(\text{case1})}E_{2^k+2^l,2^k+2^l}\frac{L-3}{4}+\sum_{k,l(\text{case2})}E_{2^k+2^l,2^k+2^l}\frac{L-5}{4}\\+\sum_{k,l(\text{case3})}E_{2^k+2^l,2^k+2^l}\frac{L-7}{4}+\sum_{k,l(\text{case4})}E_{2^k+2^l,2^k+2^l}\frac{L-9}{4}\right)\\
\end{align*}
$$

where
$$
\begin{align*}
&\text{case1:}\ (k=0,l=1) \ or \ (k=L-2,l=L-1) \\
&\ \sum_{i=0}^{L-2}\left(\delta_{k,i}\delta_{l,i+1}-\frac{1}{2}\delta_{k,i}-\frac{1}{2}\delta_{l,i}
-\frac{1}{2}\delta_{k,i+1}-\frac{1}{2}\delta_{l,i+1}\right)=-\frac{1}{2}\\
&\text{case2:}\ (k+1=l \ and \ \neg(\text{case1}))\ or \ k=0,l=L-1\\
&\ \sum_{i=0}^{L-2}\left(\delta_{k,i}\delta_{l,i+1}-\frac{1}{2}\delta_{k,i}-\frac{1}{2}\delta_{l,i}
-\frac{1}{2}\delta_{k,i+1}-\frac{1}{2}\delta_{l,i+1}\right)=-1\\
&\text{case3:}\ (\neg(\text{case1 or 2})) \ and \ (k=0\ or \ l=L-1)\\
&\ \sum_{i=0}^{L-2}\left(\delta_{k,i}\delta_{l,i+1}-\frac{1}{2}\delta_{k,i}-\frac{1}{2}\delta_{l,i}
-\frac{1}{2}\delta_{k,i+1}-\frac{1}{2}\delta_{l,i+1}\right)=-\frac{3}{2}\\
&\text{case4:}\neg(\text{case1 or 2 or 3 }) \ and \ \\
&\ \sum_{i=0}^{L-2}\left(\delta_{k,i}\delta_{l,i+1}-\frac{1}{2}\delta_{k,i}-\frac{1}{2}\delta_{l,i}
-\frac{1}{2}\delta_{k,i+1}-\frac{1}{2}\delta_{l,i+1}\right)=-2\\

\end{align*}
$$

The possible values for $k,l,i$ are slightly different, as shown below pictorially.

<img src="kli.png" style="zoom:40%;" />

Also, different cases could be shown as follows pictorially.

| case | sketch                                                       | red                                                          | green                                                        | E                   | degeneracies                                         |
| ---- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------- | ---------------------------------------------------- |
| 1    | <img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/M2case1.png" style="zoom:40%;" /> | $\begin{matrix}\delta _ {k,i}\delta _ {l,i+1}=1\\\delta _ {k,i}=1\\\delta_ {l,i}=1\\\delta_ {l,i+1}=1\end{matrix}$ | $\begin{matrix}\delta _ {k,i}\delta _ {l,i+1}=1\\\delta_ {k,i}=1\\ \delta_ {k,i+1}=1\\\delta_ {l,i+1}=1\end{matrix}$ | $\frac{L-3}{4} J _ z$ | $2$                                                  |
| 2    | <img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/M2case2.png" style="zoom:40%;" /> | $\begin{matrix}\delta _ {k,i}\delta _ {l,i+1}=1\\ \delta _ {k,i}=1\\ \delta _ {l,i}=1\\ \delta _ {k,i+1}=1\\ \delta_ {l,i+1} =1 \end{matrix}$ | $\begin{matrix}\delta _ {k,i}=1\\ \delta_ {l,i+1} =1 \end{matrix}$ | $\frac{L-5}{4}J _ z$  | $L-2$                                                |
| 3    | <img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/M2case3.png" style="zoom:40%;" /> | $\begin{matrix}\delta _ {k,i}=1\\\delta _ {k,i+1}=1\\\delta _ {l,i+1}=1\end{matrix}$ | $\begin{matrix}\delta _ {k,i}=1\\\delta _ {l,i}=1\\\delta _ {l,i+1}=1\end{matrix}$ | $\frac{L-7}{4}J _ z$  | $2(L-3)$                                             |
| 4    | others                                                       |                                                              |                                                              | $\frac{L-9}{4}J_z$  | $\left(\begin{matrix}L\newline 2\end{matrix}\right)-3(L-2)$ |



### Numerical calculation

L=60

Jz=100

<img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/M2o.png" style="zoom:40%;" />

## M=3 with OBC

### Analytical calculation

$$
\begin{align*}
& \ H_I^{(M=3)}\\
&=J_z \sum_{n=0}^{2^L-1}E_{n,n}\left(\sum_{i=0}^{L-2}\delta_{\mathcal{N}(n),3}\left(\delta_{\mathfrak b_{n}(i),1}\delta_{\mathfrak b_{n}(i+1),1}-\frac{1}{2}\delta_{\mathfrak b_{n}(i),1}-\frac{1}{2}\delta_{\mathfrak b_{n}(i+1),1}\right)+\frac{L-1}{4}\right)\\
&=J_z \sum_{k=0}^{L-3}\sum_{l>k}^{L-2}\sum_{m>l}^{L-1} E_{2^k+2^l+2^m,2^k+2^l+2^m}\left(\sum_{i=0}^{L-2}\left(\delta_{k,i}\delta_{l,i+1}+\delta_{l,i}\delta_{m,i+1}
-\frac{1}{2}\delta_{k,i}-\frac{1}{2}\delta_{l,i}-\frac{1}{2}\delta_{m,i}\\-\frac{1}{2}\delta_{k,i+1}-\frac{1}{2}\delta_{l,i+1}-\frac{1}{2}\delta_{m,i+1}\right)+\frac{L-1}{4}\right)\\
&=J_z
\end{align*}
$$

$$
\begin{align*}
&\text{case1:}\ (k=0,l=1,m=2)\ or\ (k=L-3,l=L-2,m=L-1)\\
&\sum_{i=0}^{L-2}\left(\delta_{k,i}\delta_{l,i+1}+\delta_{l,i}\delta_{m,i+1}
-\frac{1}{2}\delta_{k,i}-\frac{1}{2}\delta_{l,i}-\frac{1}{2}\delta_{m,i}-\frac{1}{2}\delta_{k,i+1}-\frac{1}{2}\delta_{l,i+1}-\frac{1}{2}\delta_{m,i+1}\right)=-\frac{1}{2}\\
&\text{case2:}\ (\neg(\text{case1})\ and \ k+2=l+1=m)\ or\ (k=0,l=1,m=L-1)\ or\ (k=0,l=L-2,m=L-1)\\
&\sum_{i=0}^{L-2}\left(\delta_{k,i}\delta_{l,i+1}+\delta_{l,i}\delta_{m,i+1}
-\frac{1}{2}\delta_{k,i}-\frac{1}{2}\delta_{l,i}-\frac{1}{2}\delta_{m,i}-\frac{1}{2}\delta_{k,i+1}-\frac{1}{2}\delta_{l,i+1}-\frac{1}{2}\delta_{m,i+1}\right)=-1\\
&\text{case3:}\ \neg(\text{case1 or 2})\ and ((k=0,l=1)\ or\ (k=L-2,m=L-1))\\
&\sum_{i=0}^{L-2}\left(\delta_{k,i}\delta_{l,i+1}+\delta_{l,i}\delta_{m,i+1}
-\frac{1}{2}\delta_{k,i}-\frac{1}{2}\delta_{l,i}-\frac{1}{2}\delta_{m,i}-\frac{1}{2}\delta_{k,i+1}-\frac{1}{2}\delta_{l,i+1}-\frac{1}{2}\delta_{m,i+1}\right)=-\frac{3}{2}\\
&\text{case4:}\ \neg(\text{case1 or 2 or 3}) \ and \ ((k=0,m=L-1)\ or\ k+1=l\ or\ l+1=m) \\
&\sum_{i=0}^{L-2}\left(\delta_{k,i}\delta_{l,i+1}+\delta_{l,i}\delta_{m,i+1}
-\frac{1}{2}\delta_{k,i}-\frac{1}{2}\delta_{l,i}-\frac{1}{2}\delta_{m,i}-\frac{1}{2}\delta_{k,i+1}-\frac{1}{2}\delta_{l,i+1}-\frac{1}{2}\delta_{m,i+1}\right)=-2\\
&\text{case5:}\ \neg(\text{case1 or 2 or 3 or 4}) \ and \ (k=0\ or \ m=L-1)\\
&\sum_{i=0}^{L-2}\left(\delta_{k,i}\delta_{l,i+1}+\delta_{l,i}\delta_{m,i+1}
-\frac{1}{2}\delta_{k,i}-\frac{1}{2}\delta_{l,i}-\frac{1}{2}\delta_{m,i}-\frac{1}{2}\delta_{k,i+1}-\frac{1}{2}\delta_{l,i+1}-\frac{1}{2}\delta_{m,i+1}\right)=-\frac{5}{2}\\
&\text{case6:}\ \neg(\text{case1 or 2 or 3 or 4 or 5}) \\
&\sum_{i=0}^{L-2}\left(\delta_{k,i}\delta_{l,i+1}+\delta_{l,i}\delta_{m,i+1}
-\frac{1}{2}\delta_{k,i}-\frac{1}{2}\delta_{l,i}-\frac{1}{2}\delta_{m,i}-\frac{1}{2}\delta_{k,i+1}-\frac{1}{2}\delta_{l,i+1}-\frac{1}{2}\delta_{m,i+1}\right)=-3\\
\end{align*}
$$

The possible values for $k,l,m,i$ are slightly different, as shown below pictorially.

<img src="klmi.png" style="zoom:40%;" />

Also, different cases could be shown as follows pictorially.

| case | sketch                                                       | red                                                          | green                                                        | E                   | degeneracies                                           |
| ---- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------- | ------------------------------------------------------ |
| 1    | <img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/M3case1.png" style="zoom:40%;" /> | $\begin{matrix}\delta_{k,i}\delta_{l,i+1}=1\\\delta_{l,i}\delta_{m,i+1}=1\\\delta_{k,i}=1\\\delta_{l,i}=1\\\delta_{l,i+1}=1\\\delta_{m,i}=1\\\delta_{m,i+1}=1\end{matrix}$ | $\begin{matrix}\delta_{k,i}\delta_{l,i+1}=1\\\delta_{l,i}\delta_{m,i+1}=1\\\delta_{k,i}=1\\\delta_{k,i+1}=1\\\delta_{l,i}=1\\\delta_{l,i+1}=1\\\delta_{m,i+1}=1\end{matrix}$ | $\frac{L-3}{4} J_z$ | $2$                                                    |
| 2    | <img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/M3case2.png" style="zoom:40%;" /> | $\begin{matrix}\delta_{k,i}\delta_{l,i+1}=1\\\delta_{k,i}=1\\\delta_{l,i}=1\\\delta_{l,i+1}=1\\\delta_{m,i+1}=1\end{matrix}$ | $\begin{matrix}\delta_{k,i}\delta_{l,i+1}=1\\\delta_{l,i}\delta_{m,i+1}=1\\\delta_{k,i}=1\\\delta_{k,i+1}=1\\\delta_{l,i}=1\\\delta_{l,i+1}=1\\\delta_{m,i}=1\\\delta_{m,i+1}=1\end{matrix}$ | $\frac{L-5}{4}J_z$  | $L-2$                                                  |
| 3    | <img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/M3case3.png" style="zoom:40%;" /> | $\begin{matrix}\delta_{k,i}\delta_{l,i+1}=1\\\delta_{k,i}=1\\\delta_{l,i}=1\\\delta_{l,i+1}=1\\\delta_{m,i}=1\\\delta_{m,i+1}=1\end{matrix}$ | $\begin{matrix}\delta_{l,i}\delta_{m,i+1}=1\\\delta_{k,i}=1\\\delta_{k,i+1}=1\\\delta_{l,i}=1\\\delta_{l,i+1}=1\\\delta_{m,i+1}=1\end{matrix}$ | $\frac{L-7}{4} J_z$ | $4(L-4)$                                               |
| 4    | <img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/M3case4.png" style="zoom:40%;" /> | $\begin{matrix}\delta_{k,i}=1\\\delta_{l,i}=1\\\delta_{l,i+1}=1\\\delta_{m,i+1}=1\end{matrix}$ | $\begin{matrix}\delta_{k,i}\delta_{l,i+1}=1\\\delta_{k,i}=1\\\delta_{k,i+1}=1\\\delta_{l,i}=1\\\delta_{l,i+1}=1\\\delta_{m,i}=1\\\delta_{m,i+1}=1\end{matrix}$ | $\frac{L-9}{4}J_z$  | $(L-4)\\+(L-4)(L-5)\\=(L-4)^2$                         |
| 5    | <img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/M3case5.png" style="zoom:40%;" /> | $\begin{matrix}\delta_{k,i}=1\\\delta_{l,i}=1\\\delta_{l,i+1}=1\\\delta_{m,i}=1\\\delta_{m,i+1}=1\end{matrix}$ | $\begin{matrix}\delta_{k,i}=1\\\delta_{k,i+1}=1\\\delta_{l,i}=1\\\delta_{l,i+1}=1\\\delta_{m,i+1}=1\end{matrix}$ | $\frac{L-11}{4}J_z$ | $(L-4)(L-5)$                                           |
| 6    | others like <img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/M3case6.png" style="zoom:40%;" /> | $\begin{matrix}\delta_{k,i}=1\\\delta_{k,i+1}=1\\\delta_{l,i}=1\\\delta_{l,i+1}=1\\\delta_{m,i}=1\\\delta_{m,i+1}=1\end{matrix}$ |                                                              | $\frac{L-13}{4}J_z$ | $\left(\begin{matrix}L-4\newline 3\end{matrix}\right)$ |

The sum of degeneracies is $\left(\begin{matrix}L\newline 3\end{matrix}\right)$.



### Numerical calculation

L=30

Jz=100

<img src="https://raw.githubusercontent.com/yf-liu/yf-liu.github.io/master/_posts/2020-04-15-CAR-algebra/assets/M3o.png" style="zoom:40%;" />

