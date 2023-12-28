---
title: 辛几何 III
date: 2023-11-08 22:00
category: 
- 学科笔记
- 博一(秋)
- 辛几何
tags: 
- 笔记
- 微分几何
mathjax: true
---

## Lagrangian sub-manifolds

**Definition** Say $X$ is a Lagrangian sub-manifold of $(M,\omega)$, whenever the inclusion $i:X\to M$ is duces the inclusion of Lagrangian sub-spaces (maximal isotropic), i.e., 
$$
\operatorname di_p:T_pX\to T_pM,\quad v\mapsto v.
$$
**Proposition** $X$ is a Lagrangian submanifold of $(M,\omega)$, whenever $2\dim X=\dim M$ and $i^\ast \omega =0$ ($i:X\to M$ is the inclusion map). 

> **Proof** $\Rightarrow$ It is straightforward from the definition that $\dim M=2\dim X$. By definition of isotropic subspace, 
> $$
> i^\ast \omega (u,v)=\omega (i_\ast u,i_\ast v)=0\quad (\forall u,v\in T X).
> $$
> Hence, $i^\ast \omega =0$. 
>
> $\Leftarrow$ Conversely, if $i^\ast (u,v)=\omega (i_\ast u,i_\ast v)=0$ for $u,v\in TX$ and 
> $$
> \dim X=\dim T_pX=\frac{1}{2}\dim T_pM=\frac{1}{2}\dim M,
> $$
> then $i_\ast (T_pX)$ is an $n$-dimensional isotropic subspace of $T_{i(p)}M$ for every $p$. It coincides the definition of Lagrangian sub-manifolds.

**Example** The zero section of $T^\ast X$, the vector bundle over $X$, is a Lagrangian sub-manifolds. Here 
$$
X_0:=\{(x,\eta_x)\in T^\ast M:\eta_x=0_x\in T^\ast_xX\}
$$
is the zero section. For inclusion $i_0:X_0\hookrightarrow T^\ast X$, we claim that $i_0^\ast \alpha $. In fact, for $v\in TX$, we have that 
$$
i^\ast _0\alpha(v)=\sum_{i=1}^n\eta_i\operatorname dx^i(v)=0.
$$
Hence, $i_0^\ast \omega =i^\ast _0(-\operatorname d\alpha)=0$. 

**Proposition** For any section of $T^\ast$ over $X$, e.g., $X_\eta:=\{(x,\eta_x):\eta_x\in T_x^\ast X\}$, $X_\eta$ is a Lagrangian sub-manifold whenever $\operatorname d\eta=0$, that is, $\eta$ is closed as a $1$-form. 

> **Proof** We see that $X\cong X_\eta$ is indeed an isomorphism. Hence, 
> $$
> \left[s_\eta:X\hookrightarrow T^\ast X,x\mapsto (x,\eta_x)\right]\cong \left[i:X_\eta\hookrightarrow  X^\ast ,(x,\eta_x)\mapsto (x,\eta_x)\right].
> $$
> Then, $X_\eta$ is Lagrangian, whenever $i^\ast\operatorname d\alpha=0$, whenever $s_\eta^\ast \operatorname d\alpha=0$, whenever $s_\eta^\ast \alpha$ is closed. We know that the tautological form is such that $s_\eta^\ast \alpha=\eta$. Hence, $X_\eta$ is Lagrangian whenever $\operatorname d\eta=0$. 

**Example** When $X$ is simply connected, then every closed $1$-form is exact. Therefore, all Lagrangian sub-manifolds of $(T^\ast X,\omega)$ is induced by some $f\in C^\infty(M)$, i.e., the section $X_{\operatorname df}$. 

**Definition** (Co-normal bundle) Let $S$ be an $k$-dimensional sub-manifold of $X$​. Then we define the co-normal space
$$
N_x^\ast S:=\{\xi\in T_x^\ast X:[\xi:T_xS\to 0]\}.
$$
The co-normal bundle is defined as 
$$
N^\ast S:=\bigcup_{x\in S}N^\ast S.
$$

