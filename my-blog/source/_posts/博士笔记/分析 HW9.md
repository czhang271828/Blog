---
title: 分析 HW9
date: 2023-11-21 11:40:00
category: 
- 学科笔记
- 博一(秋)
- 分析
tags: 
- 笔记
mathjax: true
---

## HW9 for Analysis

> ANALYSIS $\bullet$ MATH6105 $\bullet$ HOMEWORK \#9
> THE PROBLEM SHEETS ARE NOT TO BE HANDED IN

**Ex 1** Let $Y,Z\subset \ell^2$ be given by 
$$
\begin{align*}
Y&:=\{\{y_n\}\in \ell^2:y_{2n}=1\text{ for all }n\geq 1\},\\
Z&:=\{\{z_n\}\in \ell^2:z_{2n-1}=nz_{2n}\text{ for all }n\geq 1\}.
\end{align*}
$$

1. Show that $Y$ and $Z$ are closed subspaces of $\ell^2$ and that $Y\cap Z=\{0\}$. 
2. Show that the algebraic direct sum $X:=Y\oplus Z$ is a dense proper subspace of $\ell^2$. 
3. Let $\pi:X\to X$ be the projection $\pi(y+z):=y$ for all $y\in Y$ and $z\in Z$. Show directly that $\pi$ is unbounded. 

> **Proof** 
>
> 1. Let $\{y_n^{(\lambda)}\}_{n\geq 1}\subseteq Y$ be a sequence s.t. $y^{(\lambda)}\to y^{(0)}\in \ell^2$, then $y^{(\lambda)}_{2n}\to y_{2n}^{(0)}=1$ for all $n\geq 1$. Hence, $Y$ is closed. By the same token, suppose $\{z_n^{(\lambda)}\}_{n\geq 1}\subseteq Z$ be a sequence s.t. $z^{(\lambda)}\to z^{(0)}\in \ell^2$, then $z_{2n-1}^{(0)}=nz_{2n}^{(0)}$ for all $n\geq 1$. Hence, $Z$ is also closed in $\ell^2$. 
>
> 2. For any finite sequence $\{x_n\}_{n\geq 1}$, we see that 
>    $$
>    (x_{2n-1},x_{2n})=(x_{2n-1}-n(x_{2n}-1),1)+(n(x_{2n}-1),x_{2n}-1).
>    $$
>    Hence, $X\cap \ell^2_{\text{finite}}$ is dense in $\ell^2_{\text{finite}}$, hence is dense in $\ell^2$. 
>
> 3. Consider the sequence of points on the unit sphere of $\ell^2$, $\{x^{(m)}=e_{2m-1}\}$. Since
>    $$
>    (x_{2m-1},0)=(x_{2m+1}+m,1)+(-m,-1)\quad (x_{2m-1}=1),
>    $$
>    we have that $\|\pi(x^{(m)})\|_{\ell^2}=\|(1+m,1)\|_{\ell^2}\to \infty$. Hence, $\pi$ is unbounded. 

**Ex 2** In the lectures we have seen that for Banach spaces $X$, $Y$ and $T\in \mathcal B(X, Y)$, in general $\overline{\operatorname{ran}T^\ast}$ might be strictly contained in $(\operatorname{ker}T)^\circ$. However, show that in the setting of the closed range theorem we will have equality. That is, prove that

> for Banach spaces $X$ and $Y$ and $T\in \mathcal B(X,Y)$, if $\operatorname{ran} T$ is closed, then $\operatorname{ran}T^\ast=(\operatorname{ker}T)^\circ$. 

> **Proof** 

**Ex 3** This question will be frequently used in the discuss of weak and weak-$\star$ topologies.

1. Let $X$, $Y$, and $Z$ be vector spaces and $T:X\to Y$, $S:Y\to Z$ be linear maps. Show that there exists a linear map $\pi:Z\to Y$ such that $T=\pi\circ S$ if and only if $\ker S\subset \ker T$. 
2. Hence or otherwise, show that if $n\in \mathbb N$ and if $f_1,\ldots, f_n$ and $f$ are linear functionals on a vector space $X$, then $f$ is spanned by $f_1,\ldots, f_n$ if and only if $\bigcap _{k=1}^n\ker f_k\subset \ker f$. 
3. Deduce  (without Hahn-Banach theorems) that, if $F$ is finite dimensional subspace of a normed vector space, then $F=(F^\circ)_\circ $, the pre annihilator of the annihilator. 

**Ex 4** Let $X$ be a real Banach space and $C\subset X$ be a convex subset. Denote by $\mu_C:X\to \mathbb R$ the Minkowski functional/gauge associated to  $C$. Prove that the following statements

1. When $X=B_X$ (the unit open ball), $\mu_{B_X}(x)=\|x\|$; 
2. $\mu_{aC}(x)=\frac1a\mu_C(x)$ for $a>0$;
3. If $C$ is open, then $C=\{\mu_C<1\}$; if $C$ is closed, then $C=\{\mu_C\leq 1\}$; 
4. If $C$ is moreover symmetric, then $\mu_C$ is a seminorm;
5. If $C$ is moreover symmetric and bounded, then $\mu_C$ is a norm that is equivalent to $\|\bullet\|_X$. 
