---
title: 分析 HW8
date: 2023-11-14 11:40:00
category: 
- 学科笔记
- 博一(秋)
- 分析
tags: 
- 笔记
mathjax: true
---

## HW8 for Analysis

> ANALYSIS $\bullet$ MATH6105 $\bullet$ HOMEWORK \#8
> THE PROBLEM SHEETS ARE NOT TO BE HANDED IN

**Ex 1** Let $X$ be a Banach space whose norm satisfies the parallelogram law. Dene $\langle\bullet, \bullet\rangle$ by the polarisation identity. Prove that this denes an inner product.

> **Proof** For real Banach space, we define
> $$
> (x,y):=\frac{1}{4}\left(\|x+y\|^2-\|x-y\|^2\right)=\frac{1}{2}(\|x+y\|^2-\|x\|^2-\|y\|^2).
> $$
> Then we have that 
> $$
> \|x+y+z\|^2=2\|x+y\|^2+2\|z\|^2-\|x+y-z\|^2=2\|x+z\|^2+\|y\|^2-\|x-y+z\|^2.
> $$
> Hence, 
> $$
> \begin{align*}
> (x,y+z)&=\frac{1}{4}(\|x+y+z\|^2-\|x-y-z\|^2)\\[6pt]
> &=\frac{1}{8}(2\|x+y\|^2+2\|x+z\|^2-2\|x-y\|^2-2\|x-z\|^2)\\[6pt]
> &=(x,y)+(x,z).
> \end{align*}
> $$
> By induction, $(\bullet ,\bullet )$ is $\mathbb Q$-linear, and thus is $\mathbb R$-linear by continuity. 
>
> For complex Banach spaces, we define
> $$
> (x,y):=\frac{1}{4}\sum_{k=0}^3i^k\|x+i^ky\|.
> $$
> Hence, $i(x,y)=(ix,y)=-(x,iy)$, $(x,y)=\overline{(y,z)}$. We also have that 
> $$
> (x,y+z)=\frac{1}{4}\sum_{k=0}^3 i^k\left(\|x+i^ky\|+\|x+i^kz\|\right)=(x,y)+(x,z).
> $$
> Hence, $(\bullet ,\bullet )$ is $\mathbb Q[i]$-linear inner product, and thus is $\mathbb C$-linear by continuity. 

**Ex 2** Let $H$ be an infinite-dimensional separable Hilbert space. Show that $H$ admits a norm that is not equivalent to the original norm.

> **Proof** Since $H$ is separable, we can select an orthonormal basis $\{e_i\}_{i=1}^\infty$ w.r.t. the norm 
> $$
> \left\|\sum c_ie_i\right\|=\sum |c_i|^2. 
> $$
> Then we take the new basis $\{f_i:=n e_i\}_{i=1}^n$ and define 
> $$
> \left\|\sum d_if_i\right\|^\prime =\sum |d_i|^2<\sum n^2|d_i|^2=\left\|\sum d_if_i\right\|<\infty.
> $$
> Since 
> $$
> 1=\|f_n\|^\prime =n^{-2}\|f_n\|,
> $$
> we see that $\|\bullet \|^\prime\lesssim \|\bullet\|$, while $\|\bullet \|\not\lesssim \|\bullet\|^\prime$. 

**Ex 3** Carefully prove the Riesz representation theorem for Hilbert spaces - Let $H$ be a Hilbert space. Then for each $f\in H^\ast$, there is a unique $x\in H$ such that $f(y)=(y,x)$ for all $y\in H$. The map $f\mapsto x$ is a conjugate-linear isometry of $H^\ast$ onto $H$. 

> **Proof** $y=0$ if $f=0$. For $f\neq 0$, $\ker f$ is closed with codimension $1$. Hence, we can find $z\in (\ker f)^\perp$ and see that 
> $$
> \ker f\oplus \operatorname {span} z=H. 
> $$
> Take $\lambda\neq 0$ s.t. $f(z)=(z,\lambda z)$. We claim that $x=\lambda z$. 
>
> 1. For any $(p+tz)\in \ker f\oplus z$, 
>    $$
>    (p+tz,\lambda z)=t(z,\lambda z)=tf(z)=f(p+tz). 
>    $$
>
> 2. For uniqueness, if there exists $x^\prime$ such that $f(-)=(-,x^\prime)$, we see that $(-,x-x^\prime)$ is a zero functional and thus 
>    $$
>    \|x-x^\prime\|^2=(x-x^\prime,x-x^\prime )=0.
>    $$
>
> Then we shall prove the conjugate-linear isometry
> $$
> \varphi:H^\ast \to H,\quad f\mapsto x.
> $$
> $\varphi$ is clearly conjugate linear and one-to-one. For isometry, 
> $$
> \|f\|=\max_{\|y\|=1}|f(y)|=\max_{\|y\|=1}|(y,x)|=\|x\|.
> $$
> The last equality is due to Cauchy-Schwartz inequality, i.e., 
> $$
> |(y,x)|\leq \|x\|\cdot \|y\|\quad (|(x,x)|=\|x\|^2).
> $$

**Ex 4** Denote $\mathcal B:=\{f:[0,\infty[\to \mathbb R:f\text{ is bounded}\}$. It is a Banach space under the supremum norm, without any measurability assumption. Prove that

> There exists a linear function $\operatorname{LIM}_{t\to\infty}$ on $\mathcal B$ such that 
>
> 1. $\operatorname{LIM}_{t\to\infty}f(t)=\lim_{t\to\infty}$ if the usual limit exists; 
> 2. $\operatorname{LIM}_{t\to\infty}$ is linear on $\mathcal B$; 
> 3. $\operatorname{LIM}_{t\to\infty} f(t+\tau)=\operatorname{LIM}_{t\to\infty}f(t)$ for any $\tau>0$ and $f\in \mathcal B$; 
> 4. $\liminf_{s\to\infty \leq }\operatorname{LIM}_{t\to\infty} f(t)\leq \limsup_{s\to\infty} f(s)$ for $f\in \mathcal B$. 

> **Proof** (Everything is clear with Hahn-Banach theorem) We define the sub-linear functional
> $$
> p(f):=\inf_{I\subset \mathbb R_+,|I|<\infty}\left(\limsup_{t\to \infty}\frac{1}{|I|}\sum_{s\in I}f(t+s)\right).
> $$

**Ex 5** Denote by $\mathbf D(z, r)$ the disc centred at $z$ of radius $r$ in $\mathbb C$, and set $\mathbf D := \mathbf D(0, 1)$​. Consider the Bergman space
$$
\mathcal A(\mathbf D):=\{f\in \mathscr L^2(\mathbf D):f\in \operatorname{Hol}(\mathbf D)\}.
$$
In this question, $\langle \bullet ,\bullet \rangle _{\mathscr L^2(\mathbf D)}$ denotes the $\mathscr L^2$-inner product and $\|\bullet\|_{\mathscr L^2(\mathbf D)}$ the $\mathscr L^2$-norm over $\mathbf D$. 

1. Show that for each $0<r<1-s$ and $z\in \mathbf D(0,r)$, we have 
   $$
   f(z)=\frac{1}{\pi (1-s)^2}\langle f,\chi_{\mathbf D(z,1-s)}\rangle _{\mathscr L^2(\mathbf D)}. 
   $$

2. Show that if $\{f_n\}\subset \mathcal A(\mathbf D)$ is a Cauchy sequence with respect to $\mathscr L^2$-norm, then it converges uniformly on compact subsets of $\mathbf D$. 
3. Hence, or otherwise, prove that there is a bounded linear operator $\pi:\mathscr L^2(\mathbf D)\to \mathcal A(\mathbf D)$ such that for each $\varphi \in \mathscr L^2(\mathbf D)$, $\pi (\varphi)$ is the unique point in $\mathcal A$ such that
$$
\|\varphi -\pi(\varphi)\|_{\mathscr L^2(\mathbf D)}:=\int_{\psi\in \mathcal A(\mathbf D)}\|\varphi -\psi\|_{\mathscr L^2(\mathbf D)}.
$$

> **Proof** 
> 1. It is directly obtained from
> $$
> \begin{align*}
>  &\quad \,\int_{\mathbf D}f(w)\overline{\chi_{\mathbf D(z,1-s)}(\omega)}\operatorname{d}w\\[6pt]
>  &=\int_{{\mathbf D(z,1-s)}}f(w)\operatorname{d}w\\[6pt]
>  &=\int_0^{1-s}\operatorname{d}r\int_{\partial S^1}f(z+e^{\theta\sqrt{-1}} r)\operatorname{d}\theta \\[6pt]
>  &=\int_0^{1-s}2\pi rf(z)\operatorname{d}r \\[6pt]
>  &=\pi(1-s)^2f(z).
> \end{align*}
> $$
> 2. Any compact $K\subset \mathbf D$ is covered by some $\mathbf D(0,s)$ ($0<s<1$). WLOG we let $\mathbf{D}(0,s)$ be such compact set. Then 
>    $$
>    \begin{align*}
>    |f(z_0)|^2&=\left|\frac{1}{\pi s^2}\int_{\mathbf D(0,s)} f(z)\cdot 1\operatorname{d}z\right|^2\\[6pt]
>    &\leq \frac{1}{\pi^2 s^4}\int_{\mathbf D}|f(x,y)|^2\operatorname dS\cdot \int_{\mathbf D(0,s)}\operatorname d S\\[6pt]
>    &\leq \frac{1}{\pi s^2}\|f\|_{\mathscr L^2(\mathbf D(0,s))}.
>    \end{align*}
>    $$
>    Hence, uniformly convergence $\Leftarrow$ $\mathscr L^2$ convergence on some $\mathbf D(r,(1-s)/2)$ $\Leftarrow$ $\mathscr L^2$ convergence on $\mathbf D(0,1-(1-s)/3)$. 
>3. 
