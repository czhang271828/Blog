---
title: 辛几何 II
date: 2023-10-25 18:00
category: 
- 学科笔记
- 博一(秋)
- 辛几何
tags: 
- 笔记
- 微分几何
mathjax: true
---

## Symplectic manifolds

**Definition** (Symplectic form) Say $\omega\in \bigwedge ^2(T^\ast M)$ is simplectic, whenever $\operatorname d\omega =0$ and $\omega_p:T_pM\times T_pM\to \mathbb R$ is a symplectic bilinear form. 

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

**Theorem** The cotangent bundle $T^\ast M$ is a $2n$-dimensional manifold for $M^n$. 

> **Proof** Let $\{(U_\alpha,\varphi_\alpha)\}_{\alpha\in I}$ be an open cover of $M^n$. We consider the coordinate at one point,  
> $$
> \varphi:T^\ast M\to \mathbb R^{2n},\quad \left(\sum_{i=1}^n\eta_i\operatorname d x^i\right)\mapsto (x^1,\ldots, x^n,\eta_1,\ldots, \eta_n).
> $$
> Here if we fix a $1$-form $\omega$, then the coefficients of $\omega$ is locally differentiable. WLOG, we consider $\{(U_\alpha\times \mathbb R^n,\varphi _\alpha\oplus (\psi_\alpha)|_{\varphi_\alpha})\}$. If $U_\lambda\cap U_\mu\neq \varnothing$, then 
> $$
> (\varphi_\mu\oplus \psi_\mu)\circ(\varphi_\lambda\oplus \psi_\lambda)=(\varphi_\mu\circ \varphi_\lambda^{-1})\oplus (\psi_\mu\circ \psi_\lambda^{-1}).
> $$
> We define $(\psi_{\lambda,\mu})_q:=\psi_\mu^{-1}\circ \psi_\lambda$ at $\{q\}\times \mathbb R^n$. Then
> $$
> (\varphi_{\lambda,\mu}):(U_\lambda\cap U_\mu)\to GL(n,\mathbb R). 
> $$
> Let $U_\lambda(x^1_\lambda,\ldots, x^n_\lambda)$ and $U_\mu(x^1_\mu,\ldots,x^n_\mu)$ be two coordinate system on $U_\lambda\cap U_\mu$. The change of coordinates writes
> $$
> \omega=\sum_{i=1}^n\eta_i^\lambda(\operatorname dx_\lambda^i)=\sum_{i,j=1}^n\eta_i^\lambda \frac{\partial x_\lambda^i}{\partial x_\mu^j}(\operatorname dx_\mu^j).
> $$
> Therefore, 
> $$
> \psi_{\lambda,\mu}: (\eta_i^\lambda)_{i=1}^n\mapsto \left(\sum_{j=1}^n\eta_j^\lambda\cdot \frac{\partial x_\lambda^j}{\partial x_\mu^i}\right)_{i=1}^n.
> $$

**Definition** (Tautological and canonical form) Define the canonical symplectic form $\omega\in \bigwedge^2(T^\ast (T^\ast M))$ as 
$$
\omega:=\sum_{i=1}^n\operatorname dx^i\wedge \operatorname d \eta_i.
$$
The tautological form or Liouville $1$-form is defined as
$$
\alpha=\sum_{i=1}^n\eta_i\operatorname dx^i.
$$
Here $\omega+\operatorname d\alpha=0$. 

**Proposition** $\alpha$ is intrinsically defined and so is $\omega$. 

> **Proof** Consider the change of coordinates, 
> $$
> \sum_{i=1}^n\eta_i^\lambda(\operatorname dx_\lambda^i)=\sum_{i,j=1}^n\eta_i^\lambda \frac{\partial x_\lambda^i}{\partial x_\mu^j}(\operatorname dx_\mu^j)=\sum_{j=1}^n\eta_j^\mu(\operatorname dx_\mu^j).
> $$

## Proof of Darboux's theorem

**Theorem** (Darboux) The simplectic manifold $(M^{2n},\omega)$ has a local coordinate chart $U(x^1,\ldots ,x^n,y^1,\ldots,y^n)$ such that 
$$
\omega|_U =\sum_{i=1}^n\operatorname dx^i\wedge \operatorname dy^i.
$$
In other words, every symplectic manifold is locally symplectomorphic to trivial symplectic manifolds. 

**Proposition** (Cartan's magic formula) Given manifold $M$, exterior differential form $\omega$ and smooth vector field $v$, we have that
$$
\mathscr L_v\omega =\operatorname d (i_v\omega) +i_v (\operatorname d \omega).
$$

> **Proof** If $v_p=0$ for some $p\in M$, then the formula writes $0=0$. Now we suppose that $v_p\neq 0$ for some $p\in M$. By basic theorem in ODE, we assume $v=\frac{\partial }{\partial x^1}|$ in the vicinity of $p$. The summand of $\omega$ is on the following two forms:
>
> 1. $f\operatorname d x^1\wedge \operatorname dx^{i_1}\wedge \cdots \wedge \operatorname dx^{i_{k-1}}$ where $i_t\neq 1$ for each $t$; 
> 2. $g\operatorname d x^{j_1}\wedge\cdots \wedge \operatorname d x^{j_k}$ where $j_s\neq 1$ for each $s$.
>
> We denote the summand $\omega_i:=f_i\operatorname d x^{I_i}$ for $i=1,2$. For case 1., 
>
> * $\operatorname d (i_v \omega_1)=\sum_\alpha \frac{\partial f_1}{\partial x^\alpha}\operatorname d x^\alpha\wedge \operatorname dx^{i_1}\wedge \cdots \wedge \operatorname d x^{i_{k-1}}$;
> * $i_v(\operatorname d\omega_1)=-\sum_{\alpha\neq 1}\frac{\partial f_1}{\partial x^\alpha}\operatorname d x^\alpha\wedge \operatorname d x^{i_1}\wedge \cdots \wedge \operatorname d x^{i_{k-1}}$; 
> * $\mathscr L_v\omega_1=\lim_{t\to 0}\frac{f_1(x^1+t,x^2,\ldots ,x^n)\operatorname d (x^1+t)\wedge \operatorname d x^{i_2}\wedge \cdots \wedge \operatorname dx^{i_{k-1}}-f_1(x)\operatorname dx^{I_1}}t=\frac{\partial f_1}{\partial x^1}\operatorname d x^1\wedge \operatorname d x^{I_1}$.
>
> Hence, the formula holds. For case 2., 
>
> * $\operatorname d(i_v\omega_2)=0$;
> * $i_v(\operatorname d \omega_2)=\frac{\partial f_2}{\partial x^1}\cdot \operatorname dx^{I_2}$;
> * $\mathscr L_v\omega_2=\lim_{t\to 0}\frac{f_2(x^1+t,x^2,\ldots ,x^n)\operatorname dx^{I_2}-f(x)\operatorname dx^{I_2}}{t}=\frac{\partial f_2}{\partial x^1}\cdot \operatorname d x^{I_2}$. 

**Proposition** (Moser's trick) Let $\{\omega_t\}_{t\in [0,1]}$ be a collection of symplectic forms differentiable in $t$. Then for each $p$ in the domain, there exists a open neighbourhood $U_p$ with compact support in $V$, such that there is
$$
\{g_t:U\to V\}_{t\in [0,1]}\text{ differentiable in }t,\quad g_0^\ast =\mathrm{Id},\quad g_t^\ast \omega _t=\omega_0.
$$

> **Proof** Here $g_t$ is the desired one-parameter group of locally diffeomorphisms, given by some collection of the vector fields $\{X_t\}_{t\in [0,1]}$ such that 
> $$
> \frac{\operatorname d}{\operatorname d t}g_t(p)=X_t(g_t(p)),\quad g_0(p)=p.
> $$
> If such collection $\{X_t\}$ exists, then we have 
> $$
> 0=\frac{\operatorname d}{\operatorname dt}(g^\ast_t\omega_t)=g_t^\ast \left(\frac{\operatorname d \omega_t}{\operatorname d t}\right)+g_t^\ast \left(\mathscr L_{X_t}\omega_t\right)=g^\ast _t\left(\frac{\operatorname d \omega_t}{\operatorname d t}+\operatorname di_{X_t}\omega_t\right).
> $$
>
> * The first equality is by definition $g_t^\ast \omega_t=\omega_0$.
>
> * The second equation is N-L law, here
>   $$
>   \frac{\operatorname d }{\operatorname d t}(g_t^\ast \omega)=\lim_{s\to 0}\frac{g_{t+s}^\ast \omega-g^\ast _s\omega}{s}=g_t^\ast \mathscr L_{X_t}\omega.
>   $$
>
> * The third equation is given by Cartan's magic formula
>   $$
>   \mathscr L_{X_t}\omega_t =\operatorname d (i_{X_t}\omega_t) +i_{X_t} (\operatorname d \omega_t),
>   $$
>   where the simplectic form $\omega_t$ is closed. 
>
> By Poincare lemma, we assume that $\frac{\operatorname d}{\operatorname dt}(\omega_t)=\operatorname d\eta_t$ in $U_p$. Now one only need to determine
> $$
> \eta_t+i_{X_t}\omega_t=0.
> $$
> The equation above is solvable for $t\in (-\varepsilon,\varepsilon)$ since $\omega_t$'s are non-degenerate. We assume
> $$
> \eta_t=\sum _{k=1}^{2n}\eta_t^k\operatorname dx^k,\quad X_t=\sum_{k=1}^{2n}X_t^k\frac{\partial}{\partial x^k},\quad \omega_t=\sum_{1\leq k<l\leq 2n}\omega_t^{k,l}\operatorname dx^k\wedge \operatorname d x^l.
> $$
> Now the equation $\eta_t+i_{X_t}\omega_t=0$ writes in coordinates that
> $$
> \eta_t^k+2\sum_{l=1}^{2n}\omega_t^{k,l}X_t^l=0\quad (\forall k).
> $$
> Hence, the proposition is proven. 

**Theorem** (Darboux) The simplectic manifold $(M^{2n},\omega)$ has a local coordinate chart $U(x^1,\ldots ,x^n,y^1,\ldots,y^n)$ such that 
$$
\omega|_U =\sum_{i=1}^n\operatorname dx^i\wedge \operatorname dy^i.
$$
In other words, every symplectic manifold is locally symplectomorphic to trivial symplectic manifolds. 

> **Proof** Take $\omega_t$ such that $\omega_0=\sum_{k=1}^n \operatorname dx^k\wedge \operatorname dx^{n+k}$ and  $\omega(p)=\omega_0(p)$. Then we define and $\omega_t=\omega+t(\omega_0-\omega)$ for $t\in [0,1]$. For each $t\in [0,1]$, there exists a neighbourhood of $\omega_t$ such that $\omega_t$ is non-degenerate. Since $\omega_t$ is continuous in $t$, $\{\omega_t\}_{t\in [0,1]}$ is non-degenerate on some $U$. 
>
> By Moser's trick, we can find $g_t:U\to U$ s.t. $g_0^\ast$ and $g_t^\ast \omega_t=\omega_0$. Since $\omega_t$ are non-degenerated, $g^\ast_1$ give the local diffeomorphism. 