---
title: 辛几何 III
date: 2023-10-31 22:00
category: 
- 学科笔记
- 博一(秋)
- 辛几何
tags: 
- 笔记
- 微分几何
mathjax: true
---

## Liouville forms

**Definition** ($\pi$-maps) define
$$
\pi:T^\ast M\to M,\quad \omega_p\mapsto p.
$$
**Proposition** $\pi$ is differentiable. 

**Proposition** The Liouville $1$-form equals $\alpha_p=(\operatorname d\pi_p)^\ast\eta_x$ at each $p=(x,\eta)$. 

> **Proof** Here the pull back is is functorially given by 
> $$
> (\operatorname df_p)^\ast:\left[T_{f(p)}N\overset g\to \mathbb R\right]\mapsto \left[T_pM\overset {\operatorname df_p}\longrightarrow T_{f(p)}N\overset g\to \mathbb R\right].
> $$
> For $(\operatorname d\pi_p)^\ast$, we take any local coordinate system $U(x^1,\ldots, x^n,\eta_1,\ldots ,\eta_n)$ with $x(p)=0$. Then
> $$
> \begin{align*}
> \alpha_p(\partial_{x^i})_p&=\eta_x(\operatorname d\pi_p (\partial _{x^i})_p)=\eta_x(\partial _{x^i})_x=\eta_i,\\[6pt]
> \alpha_p(\partial_{\eta_i})_p&=\eta_x(\operatorname d\pi_p (\partial _{\eta_i})_p)=\eta_x0_x=0.
> \end{align*}
> $$
> Therefore, 
> $$
> \alpha=\sum_{i=1}^n\eta _i\cdot \operatorname dx^i.
> $$

**Proposition** $\alpha$ is a Liouville $1$-form, whenever $\mu^\ast \alpha=\mu$ for arbitrary $\mu:X\to T^\ast X$. 

> **Proof** If $\alpha$ is a Liouville one form, then for arbitrary $x\in X$​ we have that 
> $$
> (\mu^\ast \alpha)_x=\alpha_{\mu(x)}\circ \operatorname d \mu_x=\eta_x\circ (\operatorname d\pi_{\mu(x)}\circ \operatorname d \mu_x).
> $$
> Here $\mu$ induce the map $x\mapsto (x,\mu_x)$, and thus $\eta_x=\mu_x$. Since 
> $$
> \operatorname d\pi_{\mu(x)}\circ \operatorname d\mu_x=\operatorname d(\pi_{\mu(x)}\circ \mu_x)=\operatorname d 1_x,
> $$
> we see that $\mu^\ast \alpha =\mu$. 
>
> For uniqueness, whenever $\mu^\ast \beta =0$ for any $\mu:X\to T^\ast X$, we have that 
> $$
> 0=(\mu^\ast \beta) (v)=\beta (\operatorname d\mu (v))\quad (\forall v).
> $$
> Since $\operatorname d\mu(v)$ spans $T(T^\ast X)$ for $v\in TX$ and $\mu\in T^\ast X$, we have that $\beta =0$. 

**Proposition** The diffeomorphism $f:X_1\to X_2$​ lifts to the diffeomorphism $f_\sharp$, i.e., 
$$
\begin{matrix}
\eta  & \in  & T_{x}^{\ast } X_{1} & \xleftarrow{\left(\operatorname{d} f_{p}\right)^{\ast }} & T_{f( x)}^{\ast } X_{2} & \ni  & \operatorname{} \theta \\
( x,\eta ) & \in  & T^{\ast } X_{1} & \xrightarrow{f_{\sharp }} & T^{\ast } X_{2} & \ni  & ( f( x) ,\theta )\\
 & \pi _{1} & \downarrow  & \circlearrowleft  & \downarrow  & \pi _{2} & \\
x & \in  & X_{1} & \xrightarrow[f]{} & X_{2} & \ni  & f( x)&.
\end{matrix}
$$

> **Proof** The commutive diagram is clear. It remains to show that both $f_\sharp$ and $f_\sharp^{-1}$ are bijective and differentiable. The bijection is given by the inverse pullback. 
> $$
> (\operatorname d f^{-1}_{f(p)})^\ast :T_x^\ast X_1\to T_{f(x)}^\ast X_2,\quad \eta\mapsto \theta.
> $$
> To see that $f_\sharp $ is differentiable, we take the small coordinate system $U$ with the origin $(x,\eta)\in T^\ast X_1$ and $V$ with the origin $(f(x),\theta)$, such that there exists a diffeomorphism 
> $$
> \begin{align*}
> \varphi &:\bigcup_{x\in U}T_x^\ast U\cong U\times \mathbb R^n,\quad (x,\eta)\mapsto (x,\varphi_p=(\eta_1,\ldots, \eta_n));\\[6pt]
> \psi &:\bigcup_{y\in V}T_y^\ast V\cong V\times \mathbb R^n,\quad (q,\eta)\mapsto (q,\psi_q=(\theta_1,\ldots, \theta_n)).
> \end{align*}
> $$
> Clearly, $\operatorname d f_p$ is differentiable in $p$, and so is $\operatorname d f^{-1}_{f(p)}$. 

**Proposition** $f:X_1\to X_2$ gives the pullback of tautological forms, i.e., 
$$
(\operatorname d f_\sharp)^\ast_p(\alpha_2)_{f(p)}=(\alpha_1)_p.
$$

> **Proof** Consider 
> $$
> \begin{align*}
> (\operatorname d f_\sharp)^\ast_p(\alpha_2)_{f(p)}&=(\operatorname d f_\sharp)^\ast_p(\operatorname d \pi_2)_{f(p)}^\ast \eta_2\\[6pt]
> &=(\operatorname d \pi_2\circ \operatorname d f_\sharp)^\ast_{p} \eta_2\\[6pt]
> &=(\operatorname d f\circ \operatorname d \pi_1)^\ast_{p} \eta_2\\[6pt]
> &=(\operatorname d \pi_1)^\ast_{p}(\operatorname d f)^\ast_{x} \eta_2\\[6pt]
> &=(\operatorname d \pi_1)^\ast_{p} \eta_1\\[6pt]
> &=(\alpha_1)_p.
> \end{align*}
> $$

**Proposition** The pullback of $f_\sharp$ also induce the simplectomorphism
$$
(\operatorname d f_\sharp)^\ast_p(-\operatorname d\alpha_2)_{f(p)}=-\operatorname d\left[(\operatorname d f_\sharp)^\ast_p(\alpha_2)_{f(p)}\right]=-\operatorname d(\alpha_1)_p.
$$

## Symplectic volume

**Definition** (Exterior algebra of dual space) Given a vector space $V$, we define
$$
\bigwedge ^\ast (V^\ast)=\bigoplus_{k=0}^{\dim V}\bigwedge ^k(V^\ast ). 
$$
 Here $\bigwedge ^k (V^\ast)$ consists of linear maps $\alpha :\prod_kV\to \mathbb R$ s.t. 
$$
\alpha(v_{\pi(1)},\ldots,v_{\pi(n)})=(-1)^{\pi}\alpha(v_1,\ldots,v_n)\quad (\forall \pi\in S_n).
$$
**Proposition** (Darboux for linear space) Any skew symmetric form $\Omega\in \bigwedge ^2V^\ast$ is of the form 
$$
\Omega=\sum_{i=1}^ne_i^\ast \wedge f_i^\ast.
$$
Here $\{u_j\}_{j=1}^k\cup \{e_i,f_i\}_{i=1}^n$ is the basis of $V$ and such that $\dim V=2n+k$. 

> **Proof** It is clear that $\Omega$ is a linear combination of $x_i\wedge y_j$'s ($x,y,z\in \{e,f,u\}$). Since 
> $$
> \Omega(e_i,e_j)=\Omega(f_i,f_j)=\Omega(u_i,u_j)=\Omega(f_i,u_j)=\Omega(e_i,u_j)=0,
> $$
> $\Omega$ is the linear combination of $e_i^\ast \wedge f_j^\ast $'s, i.e., $\Omega=\sum_{1\leq i\leq j\leq n}c_{i,j}e_i^\ast\wedge f^\ast_j$. We notice that 
> $$
> \delta_{i,j} =\Omega(e_i,f_j)=c_{i,j},
> $$
> thus $\Omega=\sum_{i=1}^ne_i^\ast \wedge f_i^\ast$. 

**Definition** (Volume form) Say $\omega$ is a volume form on the manifold $M$, if $\omega$ is non-vanishing and of the top degree. 

**Example** For $\Omega$ the symplectic $2$-form on $2m$-dimensional $V$, we have the volume form
$$
\bigwedge ^m\Omega =m!\cdot (e_1^\ast \wedge f_1^\ast )\wedge \cdots \wedge (e_m^\ast \wedge f_m^\ast) .
$$
**Proposition** For $\Omega \in \bigwedge ^2(V^\ast)$, then $\Omega$ is symplectic whenever $\Omega^m$ is nonzero ($2m=\dim V$). 

> **Proof** If not, then assume that $\Omega$ is degenerate, i.e., there exists non zero $u\in V$ s.t. $\Omega(u,-)$ is a zero map. Therefore, we extend $u$ to a basis of $V$ and find that 
> $$
> \Omega^n(u,v_2,\ldots, v_{2m})=0.
> $$
> Hence, $\Omega^m =0$, a contradiction. 

**Proposition** If $M$ is compact $n$-dimensional simplectic manifold and $\omega^n$ is a volume form, then $[\omega ^n]\neq 0$ in the group $H^{2n}(M;\mathbb R)$. 

> **Proof** It is clear that $\omega^n$ is closed. It is sufficient to show that $\omega ^n$ is not the image of some $\eta$ under $\operatorname d$. If not, then we assume that $\omega^n =\operatorname d\eta$ for some $(2n-1)$-form $\eta$. By Stocks' theorem, 
> $$
> 0\neq \int_M\omega ^n=\int_M\operatorname d\eta =\int_{\partial M}\eta=0,
> $$
> a contradiction. 

**Proposition** There are no simplectic structures on the sphere $S^{2n}$ for $n\geq 2$.

> **Proof** Since $H^2(S^{2n};\mathbb R)$ is trivial, every $2$-forms on $S^{2n}$ is exact. However, any simplectic form is non-exact, otherwise the volume form is exact. 
