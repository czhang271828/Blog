---
title: Model structure
category: 
- 学科笔记
- Zhang 组会
tags: 
- 模型范畴
mathjax: true
---

## Exact category

**Notation** $\mathscr A$ is an additive category. 

**Definition** (Exact pair) We say $(i,d)$ is an exact pair if there exists an exact sequence, i.e., 
$$
0\to X\overset i\to Y\overset p\to Z\to 0
$$
Where $i=\operatorname{ker} p$ and $p=\operatorname{coker} i$. 
> An morphism $f\in \mathsf{Mor}(\mathscr A)$ **may have neither kernels nor cokernels**; exists iff the corresponding universal properties are satisfied. 

**Definition** (Coflation, inflation, deflation)And exact pair $(i,d)$ is also called a coflation, here $i$ and $d$ are called inflation ($\rightarrowtail$) and deflation ($\twoheadrightarrow$), respectively. 

**Definition** (Exact categories) For $\mathscr A$ an additive category and $\mathscr E$ the collection of some exact pairs, we say $(\mathscr A, \mathscr E)$ is an exact category whenever the following are satisfied. 
* [E0] $\mathscr E$ is closed under isomorphisms. $\operatorname{id}_0$ is always a deflation. 
* [E1] Deflations are closed under compositions. 
* [E1]$^{\mathrm{op},\ast}$ Inflations are closed under compositions. 
* [E2] The pullbacks of deflations always exists, which are also pullbacks. 
* [E2]$^\mathrm{op}$ The pushforwards of inflations always exists, which are also pushforwards. 
* [E3]$^\ast$ $\forall X,Y, X\oplus Y\in \mathsf{Ob}(\mathscr A)$, we have the the following coflation
$$
X\overset{\binom 10}{\longrightarrow}X\oplus Y\overset{(0,1)}{\longrightarrow}Y.
$$
* [E4]$^\ast$ $d$ has a kernel whenever there exists $e$ such that $de$ is a deflation. 
* [E4]$^{\operatorname{op},\ast}$ $i$ has a cokernel whenever there exists $k$ such that $ki$ is a deflation. 

**Proposition** In the above defition of exact categories, [E0], [E1], [E2], [E2]$^{\operatorname{op}}$ implies the others. We omit the proof. 

