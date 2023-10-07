---
title: 分析 HW3
date: 2023-10-10 11:40:00
category: 
- 学科笔记
- 博一(秋)
- 分析
tags: 
- 笔记
mathjax: true
---

## HW4 for Analysis

> ANALYSIS $\bullet$ MATH6105 $\bullet$ HOMEWORK \#4
> THE PROBLEM SHEETS ARE NOT TO BE HANDED IN

**Ex 1** The Luzin theorem says that every bounded, measurable function on $\mathbb R^d$ is nearly continuous. Here *nearly* is understood in the Luzin sense, i.e., outside a subset of arbitrarily small measure. The aim of this question is to show that *nearly* cannot be understood as *a.e.*. 

1. Show that there is no continuous function $f:\mathbb R\to \mathbb R$ which equals $\chi_{[0,1]}$ a.e..
2. Consider the following variant of the standard Cantor set let $C_0=[0,1]$, and each time remove the middle $\ell_j$ of every of the remaining intervals in $C_j$ to form $C_{j+1}$. By suitably choosing $\{\ell_j\}_{j=0}^\infty$, show that for any $\xi\in ]0,1[$ one may construct a Cantor-like set $\mathcal C_\xi$ which is perfect, totally disconnected, uncountable, and has Lebesgue measure $\xi$. 
3. By suitably iterating the above construction, construct a measurable subset $E\subset [0,1]$ such that for any open interval $I\subset ]0,1[$, both $E\cap I$ and $E^c\cap I$ have positive measure. 
4. Deduce that there exists a measurable function $g:\mathbb R\to \mathbb R$ satisfying the following property: let $h:\mathbb R\to \mathbb R$ be any function that equals $g$ a.e. on $\mathbb R$; then $h$ cannot be continuous at *any* point in $[0, 1]$.
> **Proof** 
> 1. If such continuous function exists (denoted by $g$), then $\mathrm{spt}(g)\subseteq [0,1]$. By continuity we have $\lim_{x\to 0}g(x)=0$. Therefore, for arbitrary $\varepsilon >0$, there exists $\delta >0$ such that $|f(x)-g(x)|>\varepsilon$ on $[0,\delta]$. It yields that $f\neq g$ on a positive measure set, a contradiction.
> 2. Since $C_0\setminus C_\xi$ is a disjoint union of intervals, we have that
> $$
> \mu(C_\xi)=1-\sum_{j\geq 0}2^j\cdot \ell_j
> $$
> If we choose $4^j\ell_j=\ell_0\in ]0,\frac 12[$, then $\mu(C_\xi)=1-2\ell_0\in]0,1[$. 
>
> * $C_\xi$ is uncountable, since $C_\xi\twoheadrightarrow 2^{\mathbb N}$ by construction. 
> * $C_\xi$ is totally disconnected, since any $x,y\in C_\xi$ with $|x-y|=\epsilon>0$ are separated in some $C_k$, where $2^{-k}< \epsilon$. 
> * $C_\xi $ is perfect, since it is closed without isolated points. For arbitrary $x\in C_\xi$ and $\varepsilon >0$, there exists $k>(2-\log_2 \varepsilon)$ such that $C_k\cap \,]x-\varepsilon,x+\varepsilon[$ contains at least $2$ connected components in $C_k$. Here each components contains some elements in $C_\xi$. Therefore, 
> $$
> \Big(]x-\varepsilon,x+\varepsilon[ \,\cap C_\xi\Big)\setminus \{x\}\neq \varnothing.
> $$
> 3. First we add $2^j$ $C_{\xi_1}$'s with rescaling $4^{-j}$ for $j\in \mathbb N$ and then iterate such operation, i.e., every we add countable many $C_{\xi_k}$'s with appropriate rescaling for $k\in \mathbb N$ ($\xi_0:=\xi$​). Ultimately we obtain a Lebesgue measurable set with measure
>    $$
>    \mu=1-\prod_{k\in \mathbb N}(1-\xi_k).
>    $$
>    For any $\alpha\in ]0,1[$, we take $\xi_0=\frac{1+\alpha}2$ and $\xi_{k+1}=\frac 1{k+3}$ for $k\geq 1$. Then $\mu=\alpha$. Such resulting set is dense and positive measure everywhere. 
>
> 4. Take $\chi_X$, where $X$ is the result in 3..

**Ex 2** By considering the Cantor-Lebesgue function (the devil's staircase), or otherwise, construct Lebesgue-measurable functions $f,g:\mathbb R\to \mathbb R$ such that $f\circ g$ is not Lebesgue-measurable.
> **Proof** We restrict $f,g:[0,1]\to[0,1]$ for simplicity. Let $C\subset [0,1]$ be Cantor set, $\Phi$ be Cantor-Lebesgue function as follows
> <img src="https://cdn.jsdelivr.net/gh/czhang271828/imgs/test/Cantor_function.gif" alt="Cantor_function" style="zoom:25%;" />. Then $\varphi:=\frac{\mathrm{id}+\Phi}{2}:[0,1]\to[0,1]$ is monotonous. Clearly $\varphi^{-1}$ is also monotonic and thus is mesurable. 
>
> Now we take arbitrary non-Lebesgue-measurable subset $P\subset \varphi(C)$, such subset exists since $\varphi(C)$ has positive measure. Here $\psi:=\mathrm{id}_{[0,1]}\cdot 1_{\varphi^{-1}(P)}$ is measurable since $\varphi^{-1}(P)\subset C$ is null. 
> However, $\varphi\circ \psi:[0,1]\to P$ is non-measurable. 


**Ex 3** Prove the following result stated in the lectures:

**Theorem** Let $f:[a,b]\to \mathbb R$ be Borel measurable. We can find sequences $\{f_n\}$ converging to $f$ in the Lebesgue measure such that

1. $f_n$ are bounded and Borel measurable;
2. $f_n$ are simple functions;
3. $f_n$ are step functions;
4. $f_n$ are continuous functions.

> **Proof** Consider the followings
> 1. $f_n:=\min\{f_-,-n\}+\max\{f_+,n\}$;
> 2. By 1., WLOG we suppose that $f$ is bounded. Consider $f_n=2^{-n}\lfloor 2^n\cdot f(x)\rfloor$;
> 3. By 2., WLOG we suppose that $f=\sum \alpha_i 1_{E_i}$ is a simple function. By definition of Borel measurable sets, $E_i$ is approximated by open sets. Therefore, $f$ is approximated by step function;
> 4. By 3., WLOG we suppose that $f=\sum c_i1_{I_i}$ is a step function, where $I_i=[a,b]$ is an interval. Let $f_n$ be consisting of polylines passing $(-\infty,0)$, $(a-n^{-1},0)$, $(a,1)$, $(b,1)$, $(b+n^{-1},0)$. 
> > Here the word *approximate* means *convergent in measure*.

**Ex 4** Let $\{f_n\}$ be a sequence of integrable functions on $(X,\mathscr F,\mu)$ that converges to $f$ in $\mathscr L^1$, namely that $\lim_{n\to\infty}\int_X|f_n-f|\mathrm d\mu=0$. Can we conclude that $f_n\to f$ in measure $\mu$? 
> **Proof** No. Consider $f=0$ and $f_n=n^{-2}\cdot 1_{[-n,n]}$ for $n\geq 1$. 

**Ex 5** Can you find [BV] functions on $[0, 1]$ that are not absolutely continuous? How about continuous [BV] functions on $[0, 1]$ that are not absolutely continuous?
> **Proof** The Cantor-Lebesgue function $\Phi$ is monotonous (thus is BV) and continuous. We show that $\Phi$ is not [AC]. One can always choose all the connected components (intervals) in each $C_j$ (with variation $1$), whereas $\mu(C_j)\to 0$. 

**Ex 6** Prove that absolutely continuous functions on $[0, 1]$ form a closed subspace of BV-functions on $[0, 1]$.
> **Proof** The additivity of linearity are clear. The norm of $f$ in [BV] is defined as
> $$
> \|f\|_{\mathrm{BV}}:=|f(0)|+V_0^1(f).
> $$
> When $f$ is [AC], we know that $f$ is differentiable a.e. and thus
> $$
> \|f\|_{\mathrm{BV}}=|f(0)|+\int_0^1|f^\prime(s)|\mathrm ds.
> $$
> Given a Cauchy sequence of absolutely continuous function $\{f_n\}$, we see that $\{f_n(0)\}$ is Cauchy and $\{f_n^\prime\}$ is also Cauchy w.r.t. $\mathscr L^1$. Let $s_0$ be the limit of $f_n(0)$ and $g$ be the limit of $\{f'_n\}$ ($\mathscr L^1$ is complete), then
> $$
> \varphi(x):=s_0+\int_0^xg(s)\mathrm ds
> $$
> is the limit which is also [AC]. 