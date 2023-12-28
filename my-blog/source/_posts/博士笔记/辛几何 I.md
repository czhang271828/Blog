---
title: 辛几何 I
date: 2023-10-25 18:00
category: 
- 学科笔记
- 博一(秋)
- 辛几何
tags: 
- 笔记
- 线性代数
mathjax: true
---

## Symplectic bilinear forms

**Definition** (Skew-symmetric bilinear forms) Let $V$ be $m$-dimensional $\mathbb R$-vector space. Say bilinear form is skew-symmetric, whenever
$$
\Omega (u,v)=-\Omega(v,u)\quad (\forall u,v\in V).
$$

**Proposition** (Gram-Schmidt procedure) For $V$ and $\Omega$ given a priori, there exists a basis of $V$,
$$
\{e_i\}_{i=1}^n\cup \{f_i\}_{i=1}^n\cup\{u_i\}_{i=1}^k\quad (2n+k=m),
$$
satisfying the following propositions 
1. $\Omega(e_i,f_j)=\delta_{i,j}$,
2. $\Omega(e_i,e_j)=0=\Omega(f_i,f_j)$,
3. $\Omega(u_i,-):V\to \{0\}$. 

Therefore, the matrix form of $\Omega$ writes
$$
\Omega(u,v)\mapsto 
u^T
\begin{pmatrix}
O_{k\times k}&O_{k\times n}&O_{k\times n}\\
O_{n\times k}&O_{n\times n}&I_{n\times n}\\
O_{n\times k}&-I_{n\times n}&O_{n\times n}
\end{pmatrix}
v.
$$
> **Proof** First we choose $\{u_i\}$ which span the annihilator space $U\subseteq V$, i.e., 
> $$
> \Omega :U\times V\to \mathbb R,\quad (u,v)\mapsto 0. 
> $$
> Now we take any interior direct summation $V=U\oplus W$. There exists $e_1$ and $f_1$ in $W$ such that $\Omega(e_1,f_1)=1$. Clearly, $e_1$, $f_1$ are linear independent. Hence, 
> $$
> \operatorname{span}(U\cup \{e_1\}\cup \{f_1\})
> $$
> is an $n+2$-dimensional subspace. Since both $\Omega(f_i,-)$ and $\Omega(e_i,-)$ are linear surjections onto $\mathbb R$, we have that 
> $$
> \operatorname {codim}(\operatorname{span}(U\cup \{e_1\}\cup \{f_1\}))=2k-2.
> $$
> Then we keeps on taking $\{e_i,f_i\}$ in the annihilator of 
> $$
> \operatorname{span}(U\cup \{e_i\}_{i=1}^t\cup \{f_i\}_{i=1}^t)
> $$
> and finally obtain the desired basis. We claim the second last annihilator has dimension $2$; if it has dimension $1$, then it is supposed to be in $U$, a contradiction. 

**Definition** (Non-degenerated skew-symmetric form, symplectic linear structure) If $\Omega(v,-)$ has range $\mathbb R$ for each $v\in V$, then we say $(V,\Omega)$ is symplectic. 

**Proposition** For symplectic form $(V,\Omega)$, we have $U=0$ and thus the matrix form writes $\begin{pmatrix}O&I\\-I&0\end{pmatrix}$. 

**Definition** For $W$ a subspace of $V$, we say

* $W$ is symplectic, when $(W,\Omega|_W)$ is non-generated;
* $W$ is isotropic, when $\Omega|_W=0$.  

**Proposition** The annihilator of a symplectic subspace $W\subseteq V$ has dimension $\dim V-\dim W$. 

> **Proof** Consider the linear map 
> $$
> T:V\to \mathrm{Hom}(W,\mathbb R),\quad v\mapsto \Omega (v,-).
> $$
>
> * $\operatorname{ker}T$ is isomorphic to the annihilator of $W\subseteq V$ by definition;
> * We claim $T$ is surjective. For arbitrary $l\in \mathrm{Hom}(W,\mathbb R)$, there exists a interior direct summand $W_1\oplus W_2$ such that $l|_{W_1}$ is isomorphic while $l_{W_2}=0$. For $w=\sum_{i=1}^nc_ie_i+d_if_i $ spanning $W_1$, we suppose that $c_{i_0}e_{i_0}$ (resp., $d_{j_0}f_{j_0}$)is non-zero. Then $v=c_{i_0}^{-1}f_{i_0}$ (resp., $v=d_{i_0}^{-1}e_{i_0}$) is what we desired. 

**Definition** Let $W^\Omega$ denote the annihilator of $W\subseteq V$. 

**Proposition** $(W^\Omega)^\Omega=W$. 

> **Proof** $W\subseteq (W^\Omega)^\Omega$ is by definition. Since $\dim W=\dim (W^\Omega)^\Omega$, we have that $(W^\Omega)^\Omega=W$. 

**Proposition** For $(V,\Omega)$ simplectic, say $(W,\Omega|_{W\times W})$ is a symplectic subspace, whenever the following equivalent statements holds

1. $(W,\Omega|_{W\times W})$ is simplectic (non-degenerated skew-linear);
2. $W\cap W^\Omega =\{0\}$, that is, $W\oplus W^\Omega =V$. 

> **Proof** When $\neg 2$, there exists some non-zero $w\in W\cap W^\Omega$, we have $\Omega(w,w)=0$, and thus $\Omega$ is generated ($\neg 1$). 
>
> When $\neg 1$, there exists non-zero $w\in W$ annihilating $W$, that is, $W\cap W^\Omega\neq \{0\}$ ($\neg 2$). 

**Definition** (Isotropic, coisotropic) For $(V,\Omega)$ simplectic and $W\subseteq V$, 

* say $W$ is isotropic, if $W\subseteq W^\Omega$;
* say $W$ is co-isotropic, if $W^\Omega\subseteq W$.

**Proposition** If $\dim W=1$, then $W$ is isotropic; if $\operatorname{codim}W=1$, then $W$ is co-isotropic.

> **Proof** If $W=\operatorname{span}(\{w\})$ is one-dimensional, then $\Omega(W,W)$ consists of scalars of $\Omega(w,w)=0$. Hence, $W\subseteq W^\Omega$. 
>
> If $\operatorname{codim}W=1$, then $\dim W^\Omega =1$. Hence, $W^\Omega \subseteq (W^\Omega)^\Omega=W$. 

**Definition** For $(V,\Omega)$ simplectic and $W\subseteq V$, say $W$ is Lagrangian, whenever $W$ is both isotropic and co-isotropic, that is, $W=W^\Omega$. 

**Proposition** For $(V,\Omega)$ simplectic and $W\subseteq V$ Lagrangian (of dimension $2k$), the symplectic basis of $W$, $\{e_i\}_{i=1}^k\cup \{f_i\}_{i=1}^k$, extends to a symplectic basis of $V$. 

> **Proof** See Gram-Schmidt procedure.

**Proposition** For $(V,\Omega)$ simplectic and $W\subseteq V$​ Lagrangian, we have the following symplectic isomorphism
$$
(V,\Omega)\to (Y\oplus Y^\ast,\Omega_0),\quad \Omega_0((u, \alpha),(v,\beta)):= \beta(u)-\alpha(v).
$$

> **Proof** Take the dual basis of $Y$ and consider the matrix form. 

**Example** For any vector space $V$ and its dual space $V^\ast$, there is a canonical symplectic form
$$
\Omega:(V\oplus V^\ast)\times (V\oplus V^\ast)\to \mathbb R,\quad ((u,\alpha),(v,\beta))\mapsto \beta(u)-\alpha(v).
$$
If the axiom of choice is assumed, then we take $\{e_\lambda\}_{\lambda\in \Lambda}$ the basis of $V$ and $\{f_\lambda\}_{\lambda}$ the dual basis. The symplectic basis of $V\oplus V^\ast$ writes 
$$
\{(e_\lambda,0)\}_{\lambda\in \Lambda}\cup\{(0,f_\lambda)\}_{\lambda\in \Lambda}.
$$
**Definition** (Morphisms for the category of symplectic spaces) Say $\varphi: (V,\Omega)\to (V^\prime,\Omega^\prime)$ is a symplectomorphism, if $\varphi :V\to V'$ is  linear map, and 
$$
\Omega(u,v)=\Omega(\varphi (u),\varphi(v))\quad (\forall u,v\in V).
$$

## Symplectic manifolds

**Definition** (Symplectic form) Say $\omega\in A^2(M)$ is simplectic, whenever $\operatorname d\omega =0$ and $\omega_p:T_pM\times T_pM\to \mathbb R$ is a symplectic bilinear form. 

**Example** Take $M=S^2$ the unit sphere with its usual coordination in $\mathbb R^3$. We define the simplectic form as follows: 
$$
\omega_p(u,v):=\langle p,u\times v\rangle\quad (u,v\in T_pS^2=\{p\}^\perp).
$$
Such symplectic form is non-degenerated, since
$$
\langle p,u\times (u\times p)\rangle=\|u\|^2\quad (\forall u\neq 0).
$$
**Definition** (Symplectomorphisms between manifolds) Say $\varphi :(M_1,\omega_1)\to (M_2,\omega_2)$ is a symplectomorphism, if $\varphi :M_1\to M_2$ is diffeomorphism and $\varphi ^\ast \omega_2=\omega_1$. Here
$$
(\varphi^\ast \omega_2)_p(u_p,v_p)=(\omega_2)_{\varphi(p)}(\operatorname d\varphi_p(u_p),\operatorname d\varphi_p(v_p))\quad (\forall u_p,v_p\in T_pM_1).
$$
**Theorem** (Darboux) The simplectic manifold $(M^{2n},\omega)$ has a local coordinate chart $U(x^1,\ldots ,x^n,y^1,\ldots,y^n)$ such that 
$$
\omega|_U =\sum_{i=1}^n\operatorname dx^i\wedge \operatorname dy^i.
$$
In other words, every symplectic manifold is locally symplectomorphic to trivial symplectic manifolds. 

> The proof requires *Morse's trick*. 